---
layout: default
title: Intervention
nav_order:
has_children: True
---

This model was last updated on **10/02/2020**, this is version **0.1**

Experimental {: .label .label-yellow }

##### Model created
10/02/2020

## Description

In the context of food and feed an intervention is the action of embedding practices and reporting on complience within establishments, in order to improve working practices or prevent it from getting worse.  There are several intervention types that are routinely carried out on establishments to help identify poor practice and encourage compliance.

*   Sampling visits
*   Inspections and audits
*   Verification and surveillance
*   Advice and education visits
*   Information/intelligence gathering

### Related entities
-   Intervention is a child entity of `action`.
-   Intervention can be take out on an `establishment`.
-   Intervention can be taken due to non compliance of a `scheme`.
-   Intervention can be taken due to non compliance of a `activity`.
-   Intervention may have many `activities`.
-   Intervention is managed by one or multiple `Competent Authority`.
-   `Intervention Type` is a child of `Intervention`

## Unique Identifiers
Each Intervention will relate to an establishment and it will be the responsibility of the Competent Authority to document and to use their own unique identifier.

## What it is not
This is not a comprehensive database of Interventions.

## Synonyms
*   Audit
*   Sampling
*   Inspections
*   Surveillance
*   Educational visits

## Key Properties
*   The Unique identifier (UID) that identifies the intervention.
*   The date the intervention was taken.
*   Type of intervention taken.
*   The establishment intervention was applied to.

## Reference data
[Intervention Type](https://data.food.gov.uk/codes/enforcement-monitoring/_intervention-type)

## Further Information
