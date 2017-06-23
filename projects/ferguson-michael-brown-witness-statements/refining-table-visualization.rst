Refining the visualization
==========================

How can we iterate on the PBS NewsHour chart without radically rethinking their data management approach or independently assessing the raw source of information?

Reword the claims
-----------------

There's more sides to this case than for or against Officer Wilson/the prosecution. In the end though, jurors had to make a binary decision: to indict or not indict Officer Wilson.

The columns in the NewsHour chart does a good job of classifying witness statements in a boolean way, e.g.

- Did Brown charge at Wilson?
- Was Brown kneeling when he was fired upon?

However, when it comes to judging Wilson for indictment, those two questions express opposite sentiments:

- Asserting that Brown charged at Wilson *weakens* the state's case.
- Asserting that Brown was kneeling *strengthens* the state's case.

This causes a visual clash in the NewsHour's chart. But this can be fixed by rewording the questions and reversing their boolean values.

- Brown did not charge at Wilson
- Brown was kneeling when Wilson opened fire

`Yes` to both of these questions would *strengthen* the state's case.

Or, you could reverse the sentiment of the questions so that `No` to either of them *stregthen's* the state's case:

- Brown charged at Wilson
- Brown was standing when Wilson opened fire


The reworded claims
-------------------

These claims are reworded so that Yes/No answers can be interpreted, respectively, as weakening/strengthening the state's case.


- Brown charged at Wilson
- Brown reached into Wilson's police car
- Wilson ceased shooting once Brown was incapacitated
- Brown reached towards his own waist
- When fired upon, Brown was facing Wilson
- When fired upon, Brown was not fleeing
- When fired upon, Brown was not kneeling
- When fired upon, Brown did not have his hands raised




Taxonomy of witness assertions
------------------------------

The chart's columns represent claims, but broadly speaking, these claims aren't necessary apples to apples. For example, a witness statement about number of shots fired is of a different nature than a statement claiming to see Wilson shooting Brown while Brown was kneeling.

Ignoring the metadata of the witnesses (their number, the date of the interview), I believe the columns can be clustered into 3 groups:


Wilson's use of deadly force
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- The number of shots fired
- Wilson ceased shooting once Brown was incapacitated


Wilson's justification for deadly force
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Brown charged at Wilson
- Brown reached into Wilson's police car
- Brown reached towards his own waist


How Brown's body was positioned when Wilson fired upon him
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Brown was facing Wilson
- Brown was not fleeing
- Brown was not kneeling
- Brown had his hands raised



Ordering the claims by estimated importance to jurors
-----------------------------------------------------

- The number of shots fired
- Wilson ceased shooting once Brown was incapacitated

- Brown charged at Wilson
- Brown reached into Wilson's police car
- Brown reached towards his own waist

- Brown was not fleeing
- Brown was not kneeling
- Brown had his hands raised
- Brown was facing Wilson

