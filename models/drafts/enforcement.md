---
layout: default
title: Enforcement
nav_order:
has_children: True
---

This model was last updated on **10/02/2020**, this is version **0.1**

Experimental {: .label .label-yellow }

##### Model created
10/02/2020

## Description

Enforcement is the process of making establishments obey food or feed law and regulations or adhere to the criteria set out within a food or feed related scheme. This can be done by making the establishment change the way they operate in order to comply or removing the ability for the establishment to carry out activities until the changes are made.  This can also take the form of litigation, removal of services, suspension of licensing and fines.

### Related entities
-   Enforcement is a child entity of `action`.
-   Enforcement can be taken due to non compliance of a `scheme`.
-   Enforcement can be take out on an `establishment`.
-   Enforcement can be taken due to non compliance of a `activity`.
-   Enforcement may have many `activities`.
-   Enforcement can be the result of unsuccessful `Interventions`
-   Enforcement is managed by one or multiple `Competent Authority`.
-   `Enforcement Type` is a child of `Enforcement`

## Unique Identifiers
Each Enforcement will relate to an establishment and it will be the responsibility of the Competent Authority to document and to use their own unique identifier.

## What it is not
This is not a legal database of enforcement types.

## Synonyms
*   litigation
*   prosecution
*   enforcement actions

## Key Properties
*   The Unique identifier (UID) that identifies the activity.
*   The date the action was taken
*   Reason for the action being taken
*   The establishment action was taken against
*   Type of enforcement taken

## Reference data
[Enforcement Actions](https://data.food.gov.uk/codes/enforcement-monitoring/_enforcement-actions)

## Further Information
