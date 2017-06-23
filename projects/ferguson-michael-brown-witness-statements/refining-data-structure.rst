Rethinking how to structure the data of the Michael Brown witness testimonies
=============================================================================


Columnar structure
------------------

Witnesses and their interviews
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Split into two columns:

- Witness
- Interview number


Date field
^^^^^^^^^^

Change to ISO format YYYY-MM-DD


Number of shots fired
^^^^^^^^^^^^^^^^^^^^^

Split into multiple columns:

Have a boolean column of "Heard shots?". This column is meant to be as simple an interface to the question of whether the witness testified to hearing any shots. So "Multiple", "8", and "at least 3" would all evaluate to `TRUE`. `NA` would still be NA. And `-` would be `FALSE`.

Because witnesses claimed to hear a range, we could create 2 new columns, e.g. "Min. shots fired" and "Max. shots fired".

Or, create a new column that is just the lower bound, e.g. "At least this many shots". One reason for this framing is that none of the ranges have a high deviation, e.g. a difference of `1` between `9 or 10` and `5 or 6`.

The "Heard shots?" may be *too* simple of a metric. After all, there's a big difference between a witness who heard `4` shots and one who heard `10 or 11`. So let's make a column in which these values are *bucketed*/*binned*:

"Heard at least this many shots"

  - 4
  - 7
  - 10
  - Blank


Or even simpler:

"Heard at least 5 shots"



