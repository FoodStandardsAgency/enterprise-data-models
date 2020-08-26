---
layout: default
title: Premises
nav_order: 7
has_children: false
parent: Entities
categories: entity
---

# Premises
This model was last updated on **21/02/2020**, this is version **0.3**

Experimental
{: .label .label-yellow }

### Model created
13/01/2020

## Description
Premises is a fundamental concept related to food businesses. All food businesses have a premises, either a location from where they trade or the location where the business is registered with the FSA or other Competent Authorities.

### Related entities
[Establishment](/enterprise-data-models/entities/establishment.html) is a parent entity of premises, but not all premises will relate to an establishment.

[Operator](/enterprise-data-models/entities/operator.html) is the sibling of premises, and when they are combined create an establishment, but not all operators are associated with a premises.

### Entity diagram
![premises](/enterprise-data-models/entities/diagrams/premises.png)

### Synonyms
-   Location
-   Address

### What it is not
Not all address or geospatial data refers to premises.

## Properties, identifiers and reference data

### Key Properties
`Address` is a complex but key pattern for this entity. Please read the pattern carefully as different stages of development may call for different implementations of the address pattern.

### Contextual Properties
There may be scenarios where recording the premises reference number from another competent authorities' data is desirable. We should be very careful about doing this and designs which include this data expect robust challenge. It is always preferable to use a more universal identifier, such a UPRN.

### Unique Identifiers
There are a number of identifiers for premises, including the postal address. The preferred unique identifier for premises in the FSA is the [Unique Property Reference Number](https://www.ordnancesurvey.co.uk/business-government/tools-support/uprn).

## External sources and further reading
Premises is also the [singular of premises](https://en.wikipedia.org/wiki/Premises), not premise. At some point you are going to be tempted to refer to it in this way, resist that temptation. 😁
