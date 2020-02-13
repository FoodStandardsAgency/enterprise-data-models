---
layout: default
title: Awarding-Body
nav_order: xx
has_children: false
---

This model was last updated on **04/02/2020**, this is version **0.2**

Experimental
{: .label .label-yellow }

##### Model created
07/01/2020

## Description
An Awarding Body is an organisation that developed and supports a scheme.  Businesses and Establishments wishing to partake in the scheme must provide evidence that the guidelines outlaid in the scheme are adheard to, to the awarding body for their membership to be valid.

### Related entities
Awarding Bodies sponsor their `scheme`.

Awarding Body is a property of `enrolments`.

`scheme` and associated `activities` happen at an `establishment`.


## Unique Identifiers
The preferred unique identifier for in the FSA is the scheme number which will include the name of the Awarding Body.

## What it is not
This Enterprise Data Model is not intended to provide a total description of the responsibilities of the Awarding Body.

## Synonyms
*   Registering Body
*   Registered Scheme
*   Scheme

## Key Properties
*   Scheme (URI from registry to be used)
*   FSA Region (England, Wales, NI, UK Wide)

## Reference data
[Awarding Body register](https://data.food.gov.uk/codes/)
[Schemes](schemes.md)

## Further Information
Start and End dates would be recorded on the registry entry and would be used to record creation and cessation of an Awarding Body.  
