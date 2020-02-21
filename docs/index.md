---
title: Home
has_children: false
nav_order: 1
---

# FSA Data Entities and Patterns
This repository organises our enterprise data models and data patterns designed by the Data Team for use by anyone in the Agency (or outside if you like 👍)

These models and patterns are foundational to the architectural principle of data convergence to standards over time (aka "fixing the plumbing"). We aim to converge our data across services towards the definitions and entities used throughout the business. We do this by providing repeatable patterns and templating for data, this is a tangible first step towards developing a designs for data within the FSA.

## Entities
An entity data model captures the fundamental properties of a business entity so that we can try to harmonise the definition of that entity across services and the business.

They define how the entity exists within the scope of the business, explains the key properties, and gives guidance on implementing that entity in services. Key properties of an entity do not include all properties, only those that when absent would make the entity inoperable.

The creation of these models is an ongoing and evolutionary process so this repository does not contain a model for every entity used within the FSA.

You are welcome to take a look at our template for our entity models.

## Patterns
Data patterns are the smallest unit of best practice for data.

They are repeatable patterns for data components which often work at the field level or across multiple fields for elements that work better in that way.

Some of the patterns are industry best practice, put into context for the FSA, some are FSA specific, and some are cross-government or cross-sector and represent our view of working with those data elements within our domain.

Everyone who works on services for the FSA should be aware of the data patterns and use them. By doing this we begin to converge new and legacy services on established patterns which helps to reduce development time and increases data interoperability.
