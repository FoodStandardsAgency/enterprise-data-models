---
layout: default
title: Premises
nav_order: 4
has_children: false
parent: Entities
categories: entity
---

# Premises
This model was last updated on **13/02/2020**, this is version **0.2**

Experimental
{: .label .label-yellow }

### Model created
13/01/2020

## Description
Premises is a fundamental concept related to food businesses. All food businesses have a premises, either a location from where they trade or the location where the business is registered with the FSA or other `competent authorities`.

### Related entities
`Establishment` is a parent entity of Premises, but not all premises entities will be used in an establishment.

`Operator` is the sibling of Premises, and when they are combined create an `Establishment`, but not all operators are associated with a premises.

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
