---
layout: default
title: Enforcement
nav_order: 3
has_children: false
parent: Entities
categories: entity
---
# Enforcement
This model was last updated on **20/02/2020**, this is version **0.3**

Experimental
{: .label .label-yellow }

### Model created
10/02/2020

## Description
Enforcement is the term for the available actions to a [Competent Authority](/enterprise-data-models/entities/competent-authority.html) to make establishments obey food or feed law, regulations, or policy which falls within a [scheme](/enterprise-data-models/entities/scheme.html).

some examples include making the establishment change the way they operate in order to comply or removing the ability for the establishment to carry out activities until the changes are made.  This can also take the form of litigation, removal of services, suspension of licensing, and fines.

### Related entities
Enforcement is part of a [scheme](/enterprise-data-models/entities/scheme.html). It represents the actions available to the [Competent Authorities](/enterprise-data-models/entities/competent-authority.html) who own or run the scheme. Often, the available enforcement actions under the scope of a scheme will be laid out in the legislation or policy documentation.

Enforcement can happen to an [establishment](/enterprise-data-models/entities/establishment.html), [premises](/enterprise-data-models/entities/premises.html), [operator](/enterprise-data-models/entities/operator.html) or an person depending on the specific enforcement action.

Enforcement action is often the result of unsuccessful [interventions](/enterprise-data-models/entities/intervention.html), but not always.

### Entity diagram
![enforcement](/enterprise-data-models/entities/diagrams/Enforcement.png)


### Synonyms
*   litigation
*   prosecution
*   enforcement actions

### What it is not
An enforcement is not an [intervention](/enterprise-data-models/entities/intervention.html) although like an [intervention](/enterprise-data-models/entities/intervention.html) it forms part of the regulation of a scheme.  Neither is it an [activity](/enterprise-data-models/entities/activity.html), but all are associated with a [scheme](/enterprise-data-models/entities/scheme.html).

## Properties, identifiers and reference data

### Key properties
The URI of the registry entry for the enforcement action, the name (label), and notation for each item represents the minimum properties

### Contextual properties
When creating records of enforcement actions the following properties will all have uses.

It is important that the [`start-date`](/enterprise-data-models/patterns/date-and-time.html#start-date) and [`end date`](/enterprise-data-models/patterns/date-and-time.html#end-date) of the enforcement is recorded. It is worth noting that sometimes the [`end date`](/enterprise-data-models/patterns/date-and-time.html#end-date) can be blank, determined or a fixed point in time from the start date depending on the rules around the enforcement action. It can also help identify cases of production during a period of time when the business shouldn't have been operating, and by having start and end dates of enforcement actions makes the task of identifying this easier.

By recording the reason for the Enforcement actions it gives [Competent Authorities](/enterprise-data-models/entities/competent-authority.html) the ability to look for trends and focus on areas for further interventions, or build a case for stronger enforcement.

The identifier of the [Competent Authority](/enterprise-data-models/entities/competent-authority.html) that undertook the enforcement, because the establishment may have enforcement action taken by multiple authorities.

### Unique identifiers
Where possible, lists of enforcements should be modelled as registers within the scope of a scheme and a code list created. The unique identifier should be the URI of the registry entry.

### Reference data
*   [Enforcement Actions](https://data.food.gov.uk/codes/enforcement-monitoring/_enforcement-actions)

## External sources and further reading
