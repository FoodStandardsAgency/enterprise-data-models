---
layout: default
title: Activity
nav_order: 1
has_children: false
parent: Entities
categories: entity
---

# Activity
This model was last updated on **20/02/2020**, this is version **0.3**

Experimental
{: .label .label-yellow }

### Model created
07/01/2020

## Description
An activity is an action or power granted to food or feed businesses through registration, approval, or compliance with a specific regulatory `scheme`.

Examples activities include;

*   The list of activities which fall under the legislation of [approved food establishments](https://data.food.gov.uk/codes/business/_approved-food-establishments)
*   The list of activities which fall under the regulations for [animal feed](https://data.food.gov.uk/codes/business/animal-feed-establishments/_feed-activities)

### Related entities
All activities belong to a `scheme`, but a `scheme` is not the parent entity as they do not share a set of key properties.

Activities should be joined to `establishments`, not `premises`.

An `establishment` which undertakes activities does so under a `scheme` which grants them approval to do them or registers them as doing them. The combination of `establishment` and `scheme` is known as an `enrolment`.

## Synonyms
*   Approved activity
*   Business activity
*   Registered activity

## What it is not
An activity is not an action which forms part of the regulatory environment that monitors or enforces compliance. Those entities are `enforcement` and `intervention`.

## Properties, identifiers and reference data

## Key properties
As we develop services around domains with recognised activities, they will be modelled as registers within the scope of a scheme and a code list created. In these instances it is important to use the code of the activity in your implementation.

For best practice handling of code lists in services, please see our `code list pattern`.

## Contextual properties
When implementing the activity entity in a service, you will need to record the time period during which the activity is effective for against the establishment it is associated with.

For best practice on implementing dates and times for this purpose in our services, please see our [date and time pattern](/enterprise-data-models/patterns/data-and-time.md)

## Unique identifiers
Where there is a code list, the unique identifier is the URI of the registry entry.

Where there is not a code list, please get in touch with the data team to model and create one rather than creating one yourself.

## Reference data
Current activity lists are modelled in the Unified Activity List, which is used in Unified View.

## Further Information
It is important to recognise that, ownership and administration of activities can span different competent authorities, this is most common with approved establishments. The majority of activities are approved by Local Authorities acting as the Competent Authority, but the most significant activities (slaughter house, cutting plant and cold store) require approval from the FSA.

Each enrolment must be recorded separately in our services. They can be concurrent and consecutive, they have a start and end date and cannot be modified.
