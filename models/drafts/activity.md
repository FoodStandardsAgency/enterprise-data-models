---
layout: default
title: Activity
nav_order: xx
has_children: false
---

This model was last updated on **04/02/2020**, this is version **0.2**

Experimental
{: .label .label-yellow }

##### Model created
07/01/2020

## Description
Activity is one of the most complex entities within our data ecosystem.

In the FSA business context an activity is something that happens within the food and feed sector or the regulation of that sector by the FSA or other `Competent Authority` that needs to be recorded. Not all things that happen are an activity.

Some examples of activities which form part of the sector include;

*   The list of activities which fall under the legislation of [approved food establishments](https://data.food.gov.uk/codes/organisation/_activities)
*   The list of activities which fall under the regulations for [animal feed](https://data.food.gov.uk/codes/business/animal-feed-establishments/_feed-activities)

Some examples of activities which form part of the regulation of the sector include;

*   The inspection of an establishment prior to gaining approval to undertake an approved activity
*   Taking food samples from food establishments

### Related entities
Most activities are categorised as part of the `scheme` they belong to.

Activities most frequently happen at an `establishment`.

Activities are a fundamental property of `enrolments`.

Some activities will be entities in their own right.  For example, inspections are an activity, and there are key properties that are the same across all inspections, but there are also many different types of inspection which have their own unique properties, i.e., an inspection under the food hygiene ratings scheme looks for different things than one within the scope of meat hygiene but both are carried out at a premises which has an address

## Unique Identifiers
Where possible, lists of activities should be modelled as registers within the scope of a scheme and a code list created. The unique identifier should be the URI of the registry entry.

## What it is not
An activity is not a scheme but a scheme can have multiple activities.

## Synonyms
*   Approved activities
*   Administrative activities
*   Regulatory activities

## Key Properties
*   The Unique identifier (UID) that identifies the activity.
*   Links to the appropriate official controls where appropriate.

It is important to recognise that, ownership and administration of activities can span different competent authorities. See further information for examples.  

## Reference data
*   [activities register](https://data.food.gov.uk/codes/organisation/_activities)

## Further Information

Enrolments in activities are concurrent and consecutive.  They have a start and end date and cannot be modified. If an establishment is removed from or no longer wishes to carry out a registered business activity, the status will be changed appropriately and an end date will be recorded.  Establishments can request to re-enroll provided they meet the criteria.  New enrollment documentation will be required and a new UID will be generated.  

An example of an activity; A slaughter house would require approvals to slaughter different types of animals.  If that slaughter house then wanted to process the carcasses they would require approval to carry out cutting activity, and if they wanted to have in house cold storage they would require further approval to carry out those activities too.

Examples of Enrolment for official controls include;
*   Approvals including, slaughter, cutting, storage of food produce
*   Registrations
*   Register a Food Business (RaFB)
*   Shellfish Farming and Harvesting
