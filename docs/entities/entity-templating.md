---
layout: default
title: Entity Templating
nav_order: 2
has_children: false
categories: templating
---
---
layout: default
title: Entity Templating
nav_order: 2
has_children: false
categories: templating
---
# Entity Templating
We template entities , but not all entities use all properties.

## Last updated, version and status
Our models start with the date they were last updated and the version number. We number stable entities from 1.0, and experimental models from 0.0.

In our models, a major revision (i.e. 1.0 to 2.0) means we've split or merged models to create new distinct entities. We will link out to new models when this happens.

> This entity was last updated on **01/01/2020**. This is version **1.0**

We state if the entity is experimental or stable. Sometimes an entity needs significant drafting and discussion before we nail it down. We would like to do that in the open to encourage collaboration.

We use the following labels to show the status of a model.

Experimental
{: .label .label-yellow }

or

Stable
{: .label .label-green }

### Model created
We record the date the model was first created to help us track versions.

---

## Description
This is the largest section, and the only one we recommend everyone reads in full. Here we try to explain, in plain English, what they entity is within the context of FSA business.

Some concepts are fundamental to our business and need a detailed explanation.

### Related entities and synonyms
Some entities have strong relationships, for example;

1.  The `establishment` entity cannot exist without a `premises` entity. Where this occurs we will have models for each entity for you to explore.
2.  Some entities appear distinct but they are the same with different names.

Related entities and synonyms for entities are presented separately.

### What it is not
Sometimes entities get confused with others so much we need to call out what the entity is not.

---

## Properties, identifiers and reference data
This section includes most of the detail about how to implement the model in services. It details properties that are mandatory, those which are only used in specific cases, and where to use controlled vocabularies and reference data (registers).

### Key properties
These are the properties that are fundamental to the entity. They create links to other data sets and harmonise joins.

Some key properties will have patterns, some will use controlled vocabularies, and some will use registers.

### Contextual properties
This section covers properties used for specific implementations of an entity. This often means linking to code lists and vocabularies from a specific sub-domain.

Where the contextual implementation of an entity is significant, we provide child entities.

### Unique identifiers
Some entities specify a field or pattern for their unique identifier that you must use when implementing the entity. You must always use it even if it is not presented in the service to ensure interoperability.

### Reference data
Some properties will use formal registers to control their content, we link to them here.

## External sources and further reading
Sometimes we use external entities, properties, controlled vocabularies, or reference data. We link to them when we do.

Further reading may include links to policy or legislative documentation used as the basis for defining the model.
