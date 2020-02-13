---
layout: default
title: Entities
nav_order: xx
has_children: false
---

This entity was last updated on **03/02/2020**. This is version **0.1**

Experimental
{: .label .label-yellow }

### Model created
09/01/2020

### Description
A Competent Authority is defined as a body with a regulatory or supervisory role over the provision of a service, such as a professional body; for example, the Institute of Actuaries or a central or local government authority.

Competent Authorities deliver food and Feed official controls.  The FSA is the Central Competent Authority responsible for oversight and assurance that the food and feed regulatory system is effective.  For example, the FSA works with other Competent Authorities to ensure the Food Health Rating Scheme is delivered as it should be.

### Related entities and synonyms
(Often a business entity will be known by different names. There are two distinct ways in which this happens;

1.  One entity is a child or sibling of another entity, for example;
  -  An `Approved Establishment` and a `Registered Establishment` are both child entities of `Establishment`, they share the core properties of the parent entity but also have properties distinct to their sub-domain. Where this occurs we will have models for each entity for you to explore
2.  They are the same entity but the names are different across business areas

Where there are related entities and synonyms, we will present them in their own lists.)

### What it is not
This Enterprise Date Model is not intended to provide a total description of the responsibilities of a Competent Authority

## Properties, identifiers and reference data
(This section includes most of the detail about how to implement the model in services. It includes information about properties that must be used across all implementations of a model, those which are only used in specific implementations and where we use and how we implement controlled vocabularies and reference data (registers).)

### Key properties
*   CA Reference (URI from registry to be used)
*   CA Official Name
*   CA Name (**DN which name to use needs to be agreed across FSA business but could populate this field with the Official Name in the absence of anything else and then use this field - this would be the 'label' on the register**)
*   [CA Type](patterns/drafts/competent-authority-type.md) (**This will need to be amended when pattern baselined**)
*   GEO area (**DN GSS codes/polygon files for Local authorities, CEFAS data for Shellfish areas etc - this would be the ideal but may not be achievable in the short term**) (**DN - Would we create a registry entry for this or maintain a list elsewhere?**)
*   FSA Region (England, Wales, NI) (**DN - Would we create a registry entry for this or maintain a list elsewhere?**)

#### Notes
Start and End dates would be recorded on the registry entry and would be used to record creation and cessation of a Competent Authority and also changes to the above fields.

### Contextual properties
(This section covers properties that are needed for specific implementations of an entity. Frequently, this will mean linking to code lists and vocabularies that are used within a specific sub-domain.

Where the contextual implementation of an entity are significant, we create child entities and link to them here.)

### Unique identifiers
(Some entities will specify a field or pattern for their unique identifier that should always be used when modelling the entity for a service. This must always be used even if it is not presented in the service to ensure interoperability.)

### Reference data
link to [Competent Authority register](https://data.food.gov.uk/codes/reference-number/_authority)

## External sources and further reading
(Sometimes we use externally defined entities, properties, controlled vocabularies or reference data. We will always link to them when we do.

Further reading may include links to policy or legislative documentation that was used as the basis for defining the model.)
