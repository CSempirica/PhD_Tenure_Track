# PhD_Tenure_Track
An AI model to predict the average duration of a PhD candidate to reach a long-term lecturer position.
Final project for the Building AI course

## Summary

An AI model considering CVs of PhD candidates to develop a prediction of the years it will take to reach a long-term lecturer position. The model is applicable to PhD candidates from all fields of study. The model is trained on CVs from PhDs with a permanent lecturer position. Outcome is an estimate amount of years it might take a PhD candidate from any field to reach a permanent professorship.


## Background

Many PhD candidates work in precarious employment situations withing university, characterised by a long string of limited contracts, mismatch between contractually agreed and actually worked hours, positions linked to limited research projects and low pay. In Germany, 92% of all academic employees under 45 have a limited contract without a professorship. Resulting problems include:

* lack of security for personal life planning
* lack of competitiveness of academia compared to employment in industry
* brain drain from academia to industry


## How is it used?

The model can predict the number of years it will take a PhD candidate at a European university to reach an unlimited, full-time professorship. Input is their LinkedIn CV. 


## Data sources and AI methods
CVs from persons holding a permanent professorhsip position at universities within the EU. These CVs will be obtained through LinkedIn, considering those profiles that are set to "public". A web crawling tool like Phantombuster will be employed to extract data. The parameters will be fed into a linear regression model. Possible parameters are:

* name of university of (post-) graduation
* number of years to complete (post-) graduation
* names of positions held
* number of months spent at universities abroad
* number of internships in industry
* number of published articles (as mentioned on LinkedIn)
* etc.
Using a training data corpus of at least 1000 CVs, the algortihm will be tested with test data. Test data will be prepared in a way to hide the information that the individual has already obtained an unlimited lecturer position.

## Challenges

The model will not solve the precarious situation of PhD candidates itself, but will give those pondering to pursue this career path a realistic idea of the duration of their "tenure track" until getting in an unlimited lecturer position.
Also, in methodological terms, it will be very cumbersome to prepare the training and test data. One challenging issue will be the different naming of academic positions in different EU countries. Also, a long duration to obtain a certain degree does not necessarily indicate that this pattern will replicate itself in the future, so there might be bias against students with multiple challenges - such as single parents, students from less financially stable backgrounds etc.


## What next?

The model could also inform legislation and policy on the topic of European university employment.

## Acknowledgments

* https://www.budrich-journals.de/index.php/debatte/article/view/38701/32940
* https://ec.europa.eu/info/funding-tenders/opportunities/portal/screen/opportunities/topic-search;callCode=HORIZON-WIDERA-2022-ERA-01;freeTextSearchKeyword=;matchWholeText=true;typeCodes=1;statusCodes=31094501,31094502,31094503;programmePeriod=null;programCcm2Id=null;programDivisionCode=null;focusAreaCode=null;destination=null;mission=null;geographicalZonesCode=null;programmeDivisionProspect=null;startDateLte=null;startDateGte=null;crossCuttingPriorityCode=null;cpvCode=null;performanceOfDelivery=null;sortQuery=sortStatus;orderBy=asc;onlyTenders=false;topicListKey=callTopicSearchTableState
