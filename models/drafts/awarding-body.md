[](This entity model may be entirely unrequired, Not going to move to the docs until discussed whether we want this, or as adam suggested we skip straight to competent authority)

---
layout: default
title: Awarding-Body
nav_order: 1
has_children: false
parent: Entities
categories: entity
---

This model was last updated on **19/02/2020**, this is version **0.2**

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
There is not yet a preferred unique identifier for Awarding bodies in the FSA. Often the scheme number itself is used which will include the name of the Awarding Body. It is also acceptable to use the Competent authority code where relevant. If a register of awarding bodies is created this guidance will be updated to advise its use.

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
[Awarding Body register -Not yet built](https://data.food.gov.uk/codes/)
[Schemes](schemes.md)
