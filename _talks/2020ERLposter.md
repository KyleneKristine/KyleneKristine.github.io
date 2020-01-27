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

The Problem <img src="https://github.com/KyleneKristine/KyleneKristine.github.io/blob/master/_presentations/problem.png" width="30" height="30">
---
Use of multiple demand driven acquisitions plans resulted in overlap of titles being purchased.

Sierra Headings Report resulted in more irrelevant results than relevant. Staff was spending up to 4 hours a week sorting through these results.

The Solution <img src="https://github.com/KyleneKristine/KyleneKristine.github.io/blob/master/_presentations/code.png" width="30" height="30">
---
Once vendor prioritization was decided, a SQL query was developed to look for more than one bib number linked to a single isbn. DDA records were separated from other eresources and print resources by using a local 910 tag. 

2020posterimage.png

Once the query was successful, it was made into an executable program using python.

The Results <img src="https://github.com/KyleneKristine/KyleneKristine.github.io/blob/master/_presentations/solved.png" width="30" height="30">
---
After uploading 227 jstor dda records, SQL returned 16 results. while SIERRA returned 126 records, only 16 were relevant.

Staff went from spending 1-4 hours reviewing records to less than 30 minutes.

The Resources <img src="https://github.com/KyleneKristine/KyleneKristine.github.io/blob/master/_presentations/book.png" width="30" height="30">
---
#### Codecademy.com
Learn SQL and PYTHON for free.

#### GITHUB.com
Repositories of code, including librarian made code. Download and edit for use or look for examples to learn from.

