How PBS NewsHour Analyzed the Michael Brown Witness Statements
==============================================================

Before we dive into the details of the data collection process, let's look at the NewsHour's takeaways that were based on the data.

Visualization
-------------

The table was published as an image file; here's the top half of it:

.. image:: /files/images/pbs-newshour-michael-brown-witnesses-table.png

Here's how the NewsHour describes the chart:

    The chart above doesn’t reveal who was right or wrong about what happened that day, but it is a clear indication that perceptions and memories can vary dramatically.


Calculations
------------

- More than half (16 out of 29) of the witness statements asserted Brown had his hands up when Wilson shot him.
- More than half of the statements asserted Brown was running away from Wilson when shot.
- There was a rough 50/50 split on whether Wilson continued to shoot after Brown was incapacitated.
- Fewer than a fifth of the statements denied that Brown was running away.
- 6 statements asserted Brown was kneeling when shot.
- 5 statements asserted Brown had reached towards his own waist.


Data structure and management
-----------------------------

The columns
^^^^^^^^^^^

Dealing with blank/NA/? values
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

While the `NA` values make for a lot of noise in the charts, it's generally not a good idea to leave cells *blank* to represent NA, because the folks doing data entry don't know if a blank cell represents NA, or has simply not been done yet.

The use of a hyphen to express "the witness did not know the answer to a question" is too ambiguious for me. I prefer using something like "DNK" (did not know) or even a question mark.



The rows: i.e. witnesses and Statements
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Should we be counting number of assertions by witness, or by interviews? Using the latter measure gives greater weight to witnesses who were interviewed more times.



Extracting data from interviews
-------------------------------

How did NewsHour decide what the columns would be? Let's look at the witness who had a stated opinion on everything in NewsHour's rubric: Witness 14.

- http://www.documentcloud.org/documents/1370766-interview-po-darren-wilson.html
- http://www.documentcloud.org/documents/1370776-interview-witness-14-1.html
- http://www.documentcloud.org/documents/1376588-fed-int-witness-14.html




