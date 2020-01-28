---
title: "Using SQL to Reduce Demand Driven Acquisition Duplications"
collection: presentations
type: "Presentations"
permalink: /presentations/2020ERLposter
venue: "ATT Austin, TX"
date: 2020-03-09
location: "Austin, TX"
---

![Using SQL reduced time spent on removing duplicate records by 75%](https://github.com/KyleneKristine/KyleneKristine.github.io/blob/master/_presentations/2020posterheader.jpg?raw=true "Using SQL reduced time spent on removing duplicate records by 75%")

The Problem ![](/images/problem.png)
---
Brown University uses the Demand Driven Acquisitions plans from JSTOR and GOBI Sciences, it also has an e-book plan with EBSCO. JSTOR and EBSCO were originally being delivered through OCLC onto a single bib record with two different 856 links. There was a lot of overlap between JSTOR, GOBI, and EBSCO which resulted in a lot of time cleaning up records via the Sierra Heading's Report which unfortunately was unable to limit to just these three plans.

Sierra's Headings Report resulted in more irrelevant results than relevant - a couple hundred results would have less than 10 relevant bibs. Staff was spending up to 4 hours a week sorting through these results which included duplications between print and electronic resources that were deliberate. Further complicating this was the fact that several of our eresource loads were temporary resources from EBSCO and Serials Solutions whose availability changed over time. As these resources were not purchases, and would eventually leave our catalog, duplications between them and our DDA plans were not a concern.


The Solution ![](/images/code.png)
---
We began by separating our EBSCO and JSTOR DDA records onto separate bibs, which required a lot of clean up and reloading of records into the catalog upwards of 100k. Then we decided on a prioritization between the DDA plans.

Since purchase loads could take a while to become available to download, there was a risk of creating duplication by deleting the purchased's bib record in our catalog in preference of a new bib before the purchased bib could be updated. Therefore, it was decided that if a non-purchased DDA file resulted in duplications, priority would be given to the file already in the system.

Once vendor prioritization was decided, a SQL query was developed to look for more than one bib number linked to a single isbn. DDA records were separated from other eresources and print resources by using a local 910 tag. 

2020posterimage.png

Once the query was successful, it was made into an executable program using python. The executable program would take several minutes to run before resulting in a text file containing a list of isbns and how many bib records were linked to them.

The Results ![](/images/solved.png)
---
After uploading 227 jstor dda records: SQL returned 16 results while SIERRA returned 126 records - only 16 were relevant.

Both Sierra and SQL methods were used side by side for over a month, with SQL consistently returning concise and equal amounts of relevant results to Sierra. The executable program took longer to run, averaging 6 minutes, but could run in the background and reduced overall time spent on cleanup.

Staff went from spending 1-4 hours reviewing records to less than 30 minutes. This averaged 50%-88% reduction in time spent each week on this process, with an overall average of 75% reduction of time spent each week.

The Resources ![](/images/research.png)
---
#### [Codecademy.com](https://www.codecademy.com/learn/learn-sql)
Learn SQL and PYTHON for free.

#### [Github.com](http://github.com)
Repositories of code, including librarian made code. Download and edit for use or look for examples to learn from.

#### [Deduplication Repository](https://github.com/KyleneKristine/deduplicator)
My python files that run the SQL query. In the DDA file: You will need to edit line 9 with your Sierra host information, and change the v.field and v.content field in the SQL to whatever local field you use to indicate a DDA. In the Physical file: You will just need to edit line 9. Only the Physical.py file currently saves a text file.

#### [Sierra DNA](https://techdocs.iii.com/sierradna/)
This requires a Sierra login. Contains all the tables and fields used in Sierra's sql which can help you build your own sql query.

#### [PGAdmin](https://www.pgadmin.org/)
Sierra suggests using this postgresql application for your sql queries. Alternatively, new comers may find MS Access as an easy introduction to SQL, but the connection process is unfortunately more complicated.

#### [My Sierra SQL repository](https://github.com/KyleneKristine/Sierra-SQL/wiki/Sierra-Direct)
This is a list of SQL I've used and recorded on my github repository. Feel free to use and edit as needed.

#### [Public Library of Cincinnati & Hamilton County sierra-sql Wiki](https://github.com/plch/sierra-sql/wiki)
PLCH github repository full of ideas for SQL queries.

#### [UNC Chapel Hill Libraries Sierra SQL repository](https://github.com/UNC-Libraries/III-Sierra-SQL/wiki)
UNC github repository full of ideas for SQL queries.

#### [Jeremy Goldstein Sierra SQL repository](https://github.com/jmgold/SQL-Queries/wiki)
Jeremy Goldstein's github repository full of ideas for SQL queries.
