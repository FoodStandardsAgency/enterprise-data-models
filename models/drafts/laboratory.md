---
layout: default
title: Laboratory
nav_order:
has_children: false
parent: Entities
categories: entity
---

# Premises
This model was last updated on **10/03/2020**, this is version **0.1**

Experimental
{: .label .label-yellow }

### Model created
10/03/2020

## Description
In the UK, official feed and food laboratories are Public and Agricultural Analyst and Microbiology laboratories (Food Examiners) that undertake work for Local Authorities or undertaking Official Controls in specified areas for the Food Standards Agency (FSA), and Local Authorities.

Official laboratories must employ staff who possess qualifications which are defined by national legislation. In addition, laboratories must have a Public / Agricultural Analyst (formally appointed by a Local Authority) or a qualified Food Examiner in order to be designated as an Official Control Laboratory.

### Related entities
[Establishment](/enterprise-data-models/entities/establishment.html) is the location a sample was taken from.

[Scheme](/enterprise-data-models/entities/scheme.html) [Sample type](), and [sample frequency]() is outlined in the relevant Scheme.

### Synonyms
-   Lab


### What it is not
Not all Laboratories are used for testing of food safety interventions or investigations.

## Properties, identifiers and reference data

### Key Properties
??

### Contextual Properties
Each set of test results will be linked back to the laboratory that carried out the tests.  It is important that this is recorded incase any follow up action is required or the results are queried.

### Unique Identifiers
Each approved Laboratory has it's own unique identifier with the prefix of LAB-**

## External sources and further reading
A list of [FSA Approved Laboratories](http://data.food.gov.uk/codes/controlled-establishments/laboratories/approved-laboratory)

[Laboratory Analyst Type](http://data.food.gov.uk/codes/controlled-establishments/laboratories/analyst-type)
