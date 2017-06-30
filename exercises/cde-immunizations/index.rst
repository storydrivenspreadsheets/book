************************
California immunizations
************************


Vaccination rate jumps in California after tougher inoculation law
http://www.latimes.com/local/lanow/la-me-ln-california-vaccination-20170412-story.html

The vaccination rate for California’s kindergartners soared this fall from the previous year, fueled by a state law that made it significantly tougher for parents to exempt schoolchildren from shots.

It was the highest vaccination rate among kindergartners since at least 1998, and comes after a measles outbreak that began at Disneyland in 2014 focused new attention on the issue.

https://archive.cdph.ca.gov/programs/immunize/Documents/2016-17_CA_KindergartenSummaryReport.pdf

https://data.chhs.ca.gov/dataset/school-immunizations-in-kindergarten-by-academic-year

Palo Alto
=========

- Different cities/counties/districts

Lots of irrelevant data



PBE data
========

Description of the `Category` field:

    Kindergarten students with a Personal Belief Exemption (PBE) whereby a parent signs an affidavit requesting an exemption from the immunization requirements for school entry because all or some immunizations are contrary to the parent's beliefs. A new state law that went into effect in January 2014 now requires parents seeking an exemption for their Kindergarten students to document that they have received vaccine counseling from a qualified health care practitioner within the last 6 months ('Health Care Practitioner PBE') or that they have a religious objection to receiving  such counseling ('Religious PBE).  Students already enrolled in Kindergarten prior to January 2014 ('pre-Jan PBE') were not subject to the new requirement.  The number in this field represents the total PBE students as calculated by adding together the students in each of the PBE subcategories.




- Filter for the 2 most recently reported PBE columns
- In 2016-2017, the category is just (PBE)

    7381 2013-2014,HC  Practitioner Counseled PBE
    7381 2013-2014,Personal Beliefs Exemption (PBE)
    7381 2013-2014,Pre-Jan PBE
    7381 2013-2014,Religious PBE
    7464 2014-2015,HC  Practitioner Counseled PBE
    7464 2014-2015,Personal Beliefs Exemption (PBE)
    7464 2014-2015,Pre-Jan PBE
    7464 2014-2015,Religious PBE
    7422 2015-2016,HC Pratitioner Counseled PBE
    7422 2015-2016,Personal Beliefs Exemption (PBE)
    7422 2015-2016,Religious PBE
    8266 2016-2017,PBE

Wrangling
---------

Create a total_pbe column which checks for PBE for (2016-2017) or Personal Beliefs Exemption (PBE)



Questions:

Basic
-----

- Highest percentage of PBE
- Highest number of PBE
- Highest percentage of PBE with minimum number of students
- Number of schools with PBE beyond herd effect in latest year
- Number of schools with PBE beyond herd effect, with min. number of students, latest year
- Num of schools, grouped by year
- Avg PBE by year
- Private vs. Public


Complex
-------

- Schools with biggest drop from 2015 to 2016
- Schools that didn't change
- Aggregation by district



Joins
-----

Wealthy schools










