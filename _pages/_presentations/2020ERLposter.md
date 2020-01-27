---
title: "SQL DEDUPE"
collection: posters
type: "Presentations"
permalink: /presentations/2020ERLposter
venue: "ATT Austin, TX"
date: 2020-03-09
location: "Austin, TX"
---

Using SQL to Reduce Demand Driven Acquisition Duplications
====
Kylene Kristine Hutchinson  Metadata SLS | Brown University

![Using SQL reduced time spent on removing duplicate records by 75%](https://github.com/KyleneKristine/KyleneKristine.github.io/blob/master/_pages/_presentations/2020posterheader.jpg?raw=true "Using SQL reduced time spent on removing duplicate records by 75%")

The Problem
---
Use of multiple demand driven acquisitions plans resulted in overlap of titles being purchased.

Sierra Headings Report resulted in more irrelevant results than relevant. Staff was spending up to 4 hours a week sorting through these results.

The Solution
---
Once vendor prioritization was decided, a SQL query was developed to look for more than one bib number linked to a single isbn. DDA records were separated from other eresources and print resources by using a local 910 tag. 

2020posterimage.png

Once the query was successful, it was made into an executable program using python.

The Results
---
After uploading 227 jstor dda records, SQL returned 16 results. while SIERRA returned 126 records, only 16 were relevant.

Staff went from spending 1-4 hours reviewing records to less than 30 minutes.

The Resources
---
#### Codecademy.com
Learn SQL and PYTHON for free.

#### GITHUB.com
Repositories of code, including librarian made code. Download and edit for use or look for examples to learn from.

