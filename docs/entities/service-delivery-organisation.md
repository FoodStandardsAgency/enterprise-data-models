---
layout: default
title: Service Delivery Organisation
nav_order: 10
has_children: false
parent: Entities
categories: entity
---

# Service Delivery Organisation
This model was last updated on **24/08/2020**, this is version **0.5**

Experimental
{: .label .label-yellow }

### Model created
08/03/2020

## Description
A Service Delivery Organisation bridges the gap between what is legislatively correct, and the organisation(s) that deliver official controls or other schemes. It has been created for the purpose of mitigating some of the problems we have representing these entities in services and data when the concept is not formally reocgnised in legislation or policy.

A Service Delivery Organisation delivers the functions, or some of the functions of a scheme on behalf of a Competent Authority.

A Service Delivery Organisation most often appears as a shared service Organisation, commonly providing services for one or more Local Authorities. It can only discharge the duties assigned to it by the Competent Authorities that create or sponsor it, within the scope of the scheme(s) it is assigned. Most enforcement action must still be carried out by a recognised Competent Authority, but this is determined by the scheme.

### Related entities
Service Delivery Entities must be associated with at least one [Competent Authority](/enterprise-data-models/entities/competent-authority.html), but often two or more.

Service Delivery Entities undertake a range of [interventions](/enterprise-data-models/entities/intervention.html) on behalf of Competent Authorities, these interventions form part of a [scheme](enterprise-data-models/entities/scheme.html).

Service Delivery Entities frequently operate within [Service Delivery Areas](/enterprise-data-models/entities/service-delivery-area.html) which cover one or more geographic areas associated with Competent Authorities, parts of those areas, or another custom geographic area.

### Entity diagram
![SDP](/enterprise-data-models/entities/diagrams/SDP.png)

### Synonyms
-   Shared service

### What it is not
A Service Delivery Organisation is not, and can never be a Competent Authority. The root of a Competent Authority's powers and duties are legislative, and no Service Delivery Organisation is recognised in legislation, if it were, it would be a Competent Authority.

## Properties, identifiers and reference data

### Key properties
A Service Delivery Organisation will be handled in the same way as Competent Authorities within the FSA data ecosystem, with a register.

For this reason the majority of properties can be retrieved and cached by services as they are needed, but we would recommend storing the following as a reference table in legacy services and relational databases;

-   Name of the organisation
-   The code (notation) of the organisation
-   The full URI of the organisation in the registry

### Contextual properties
Any other property of a Service Delivery Organisation which is available from the registry can be used in various contexts. The most common properties will be start and end dates for the existence or powers of the Service Delivery Organisation, if they are time limited.

### Unique identifiers
The unique identifier for a Service Delivery Organisation is the URI of it's registry entry. Though this can be shortened to the notation property when the preceding part of the URI is treated as a namespace.

### Reference data
A register for this entity is currently in development.
