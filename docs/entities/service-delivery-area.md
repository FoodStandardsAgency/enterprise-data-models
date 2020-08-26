---
layout: default
title: Service Delivery Area
nav_order: 9
has_children: false
parent: Entities
categories: entity
---

# Service Delivery Area
This model was last updated on **21/08/2020**, this is version **0.2**

Experimental
{: .label .label-yellow }

### Model created
27/03/2020

## Description
A Service Delivery Area is a conceptual data entity used to express a geographical area that is not associated with an existing Competent Authority or other official geography.

It is most commonly used to show the geographical area covered by Service Delivery Entities, which frequently carry out the duties of multiple Competent Authorities across the total geographic area that those authorities cover.

We also use them to represent the geographical areas covered by FSA service areas, such as operational areas and dairy hygiene inspection areas.

### Related entities
Service Delivery Areas are associated with a [Competent Authority](/enterprise-data-models/entities/competent-authority.html), either directly, or through a Service Delivery Organisation. In the case of operational geographies, the competent authority is the FSA.

### Entity diagram
![SDA](/enterprise-data-models/entities/diagrams/sda.png)

### Synonyms
-   Operational area

### What it is not
A Service Delivery Area should not be confused with existing areas maintained as part of official geographies. Sufficient effort must be made to ensure that the geographical area is not already described elsewhere.

## Properties, identifiers and reference data

### Key properties
A Service Delivery Area must have a shapefile or suitable polygon. It must also be associated with a [Service Delivery Organisation](/enterprise-data-models/entities/service-delivery-organisation.html) or [Competent Authority](/enterprise-data-models/entities/competent-authority.html). Without one of these, there is no need for a Service Delivery Area.

### Contextual properties
Service Delivery Areas only use contextual properties when we are describing areas over which the FSA has sole responsibility. This is most common when describing the geogrpahy of our operations. For example, there is a hierarchical relationship between regions, areas, and clusters that is easiest to express through contextual properties within the Service Delivery Area rather than creating a [Service Delivery Organisation](/enterprise-data-models/entities/service-delivery-organisation.html) for each one.

### Unique identifiers
The URI of the register entry for the entity is sufficient.

### Reference data
Service Delivery Areas can frequently be the union of two or more existing geogrpahical areas. When this is the case please link to them.

## External sources and further reading
