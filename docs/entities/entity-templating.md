---
layout: default
title: Entity Templating
nav_order: 2
has_children: false
categories: templating
---
# Entity Templating
We template entities consistently, but not all entities use all of the templated properties.

## Last updated, version and status
Our models start with the date they were last updated and the version number. Stable entities are numbered incrementally from 1.0, and experimental models incrementally from 0.0.

In our models, a major revision (i.e. 1.0 to 2.0) means we've split or merged models to create new distinct entities. We will link out to new models when this happens.

> This entity was last updated on **01/01/2020**. This is version **1.0**

We indicate if the entity is experimental or stable. Sometimes an entity needs significant drafting and discussion before we nail it down, and we would like to do that in the open to encourage collaboration.

We use the following labels to indicate the status of a model.

Experimental
{: .label .label-yellow }

or

Stable
{: .label .label-green }

### Model created
We record the date the model was first created to help us track versions.

---

## Description
This is frequently the largest section, and the only one we recommend everyone reads in full. Here we try to explain, in plain English, what they entity is within the context of FSA business. We try to keep it as concise as possible but some concepts are fundamental to our business and require a detailed explanation.

### Related entities and synonyms
Often a business entity will be known by different names. There are two distinct ways in which this happens;

1.  One entity is a child or sibling of another entity, for example;
  - An `Approved Establishment` and a `Registered Establishment` are both child entities of `Establishment`, they share the core properties of the parent entity but also have properties distinct to their sub-domain. Where this occurs we will have models for each entity for you to explore
2.  They are the same entity but the names are different across business areas

Where there are related entities and synonyms, we will present them in their own lists.

### What it is not
Sometimes entities are confused with other entities so often that in order to being to unpick those mental shortcuts we need to specifically call out what the entity is not.

---

## Properties, identifiers and reference data
This section includes most of the detail about how to implement the model in services. It includes information about properties that must be used across all implementations of a model, those which are only used in specific implementations and where we use and how we implement controlled vocabularies and reference data (registers).

### Key properties
This is where we call out the properties for the entity that we think are fundamental to the entity, and if were excluded from an implementation of the entity would render it functionally useless.

Part of this is understanding how entities are most frequently link to other data sets within and outside our ecosystem and harmonising joins by providing a consistent set of base properties.

Some key properties will have patterns which will be linked here, some will use controlled vocabularies which will also be listed or linked here.

### Contextual properties
This section covers properties that are needed for specific implementations of an entity. Frequently, this will mean linking to code lists and vocabularies that are used within a specific sub-domain.

Where the contextual implementation of an entity are significant, we create child entities and link to them here.

### Unique identifiers
Some entities will specify a field or pattern for their unique identifier that should always be used when modelling the entity for a service. This must always be used even if it is not presented in the service to ensure interoperability.

### Reference data
Some properties will use formal registers to control their content, we will link to them.

## External sources and further reading
Sometimes we use externally defined entities, properties, controlled vocabularies or reference data. We will always link to them when we do.

Further reading may include links to policy or legislative documentation that was used as the basis for defining the model.
