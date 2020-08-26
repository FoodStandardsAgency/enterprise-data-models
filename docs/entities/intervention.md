---
layout: default
title: Intervention
nav_order: 5
has_children: false
parent: Entities
categories: entity
---
# Intervention

This model was last updated on **25/02/2020**, this is version **0.2**

Experimental
{: .label .label-yellow }

### Model created
10/02/2020

## Description
An intervention is used by a [Competent Authority](/enterprise-data-models/entities/competent-authority.html) to monitor and record the compliance of an establishments within a [scheme](/enterprise-data-models/entities/scheme.html).

Often, the available interventions under the scope of a scheme will be laid out in the legislation or policy documentation.

Some examples of interventions include;
*   Sampling visits
*   Inspections and audits
*   Verification and surveillance
*   Advice and education visits
*   Information/intelligence gathering

As types of intervention are frequently common across schemes, i.e., an inspection, therefore it is important to try to use a common list of interventions and also record the scheme under which they were taken.

### Related entities
Interventions form part of a [scheme](/enterprise-data-models/entities/scheme.html).

An intervention happens to an [establishment](/enterprise-data-models/entities/establishment.html), [premises](/enterprise-data-models/entities/premises.html), [operator](/enterprise-data-models/entities/operator.html) or a `person` depending on the specific intervention action.

### Entity diagram
![intervention](/enterprise-data-models/entities/diagrams/Intervention.png)

### Synonyms
*   Audit
*   Sampling
*   Inspections
*   Surveillance
*   Educational visits

### What it is not
An intervention is not an [enforcement](/enterprise-data-models/entities/enforcement.html) although like an enforcement it forms part of the regulation of a scheme.  Neither is it an [activity](/enterprise-data-models/entities/activity.html), but all are associated with a [scheme](/enterprise-data-models/entities/scheme.html).

## Properties, identifiers and reference data

## Key Properties
*   The URI of the registry entry for the intervention action
*   Name of the intervention

## Contextual Property
When applying Intervention actions it is important to record the following;

The name of the [establishment](/enterprise-data-models/entities/establishment.html) the intervention was applied to. This will help build up a picture of how the establishment is performing and help schedule future interventions and possibly impact on possible enforcements.

Recording the reason for the intervention along with the [Competent Authority](/enterprise-data-models/entities/competent-authority.html) that carried out the intervention will help build a wider picture, identify trends, and allow Competent Authorities to focus on areas for further interventions, or build a case for [enforcement](/enterprise-data-models/entities/enforcement.html) action.

The name of the [Competent Authority](/enterprise-data-models/entities/competent-authority.html) that implemented the enforcement, because the establishment may have intervention action taken by multiple competent authorities for the same reason and or same period.  It also gives other Competent Authorities a place to go to for further information for future interventions and enforcements.

It is important that the [`start-date`](/enterprise-data-models/patterns/date-and-time.html#start-date) of the enforcement is recorded as it can determine [`end date`](/enterprise-data-models/patterns/date-and-time.html#end-date) of an enforcement action. It can also help identify cases of production during a period of time when the business shouldn't have been operating, and by having start and end dates of enforcement actions makes the task of identifying produce processed within these dates easier.

A history of interventions and enforcements occurring within an [establishment](/enterprise-data-models/entities/establishment.html) will help build a picture and could impact on the severity of future enforcements by looking at the establishment's history and looking for trends.

### Unique Identifiers
Where possible, lists of interactions should be modelled as registers within the scope of a scheme and a code list created. The unique identifier should be the URI of the registry entry.

### Reference data
[Intervention Type](https://data.food.gov.uk/codes/enforcement-monitoring/_intervention-type)
