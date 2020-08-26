---
layout: default
title: Enrolment
nav_order: xx
has_children: false
---

This model was last updated on **04/02/2020**, this is version **0.2**

Experimental
{: .label .label-yellow }

##### Model created
07/01/2020

### Description
Enrolment is an FSA record of an Establishment to register or seek approval to perform a specified activity or be part of a recognised scheme.  

### Unique Identifiers
The preferred unique identifier for Enrolment in the FSA is the enrolment reference number

### Entity diagram
![enrolement](/enterprise-data-models/entities/diagrams/Enrolement.png)


### What it is not
Not all reference numbers relate to activities or schemes.

### Synonyms
*   Register number
*   Enrolment number
*   Activity Registration
*   Scheme Registration

## Key Properties
*   Reference No (Enrolment reference number that will link to appropriate documentation Approval / Registration / RafB.
*   Enrolment status
*   [Activity](https://data.food.gov.uk/codes/organisation/_activities)
*   Start Date
*   End Date

## Reference data
*   [activities register](https://data.food.gov.uk/codes/organisation/_activities)
*   [Enrolment](link to enrolment Status)

## Further Information
*   Enrolments are concurrent and consecutive.  They have a start and end date and cannot be modified. If an establishment is removed from a scheme the status will be changed appropriately and an end date will be recorded.  Establishments can request to re-enroll provided they meet the criteria.  New enrollment documentation will be required and a new UID will be generated.
*   Link to the [FHRS scheme](https://ratings.food.gov.uk/)
*   Link to the [shellfish classification scheme](https://www.food.gov.uk/business-guidance/shellfish-classification).

## Entity model



### Owner
Food Standards Agency
