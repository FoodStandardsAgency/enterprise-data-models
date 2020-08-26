---
layout: default
title: Competent Authority
nav_order: 2
has_children: false
parent: Entities
categories: entity
---
# Competent Authority

This entity was last updated on **22/05/2020**. This is version **0.4**

Experimental
{: .label .label-yellow }

### Model created
09/01/2020

## Description
A Competent Authority is a body with regulatory or supervisory oversight of a [scheme](/enterprise-data-models/entities/scheme.html).

Competent Authorities deliver food and feed official controls. The FSA is the Central Competent Authority responsible for oversight and assurance that the food and feed regulatory system is effective.

### Related entities
A [scheme](/enterprise-data-models/entities/scheme.html) is owned and delivered by Competent Authorities, however schemes may be owned and delivered by different competent authorities i.e., FHRS.

### Entity diagram
![Competent Authority](/enterprise-data-models/entities/diagrams/CompetentAuthority.png)

### Synonyms
*   Local Authority
*   Port Health Authority
*   Central Competent Authority
*   Other government department

### What it is not
This entity refers only to competent authorities as defined by the Food Standards agency within the Competent authority register, found below.

## Properties, identifiers and reference data

### Key properties

*   Competent Authority URI (see reference data below)
*   Competent Authority Name (label)
*   Competent Authority Code (notation)

### Contextual properties
The key property fields are the minimum required for the Competent Authority entity, other fields may be added for implementation reasons eg type of authority but please avoid using other legacy fields such as additional reference numbers as this adds complexity.

### Unique identifiers
The unique identifier for a competent authority is the URI of the registry entry.

### Reference data
*   [Competent Authority register](https://data.food.gov.uk/codes/reference-number/_authority)

## External sources and further reading
This section is under construction

[](**DN - Consider ref to - 'The use of Competent Authority Identifiers in FSA datasets' document**)

[](Further reading may include links to policy or legislative documentation that was used as the basis for defining the model.
consider ref to CA doc)
