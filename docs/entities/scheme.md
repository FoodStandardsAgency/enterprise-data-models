---
layout: default
title: Scheme
nav_order: 8
has_children: false
parent: Entities
categories: entity
---

# Scheme

This model was last updated on **26/02/2020**, this is version **0.3**

Experimental
{: .label .label-yellow }

### Model created
07/01/2020

## Description
A scheme is a way of classifying a piece of regulation, legislation, or policy that grants powers to and/or imposes obligations on those who are enrolled in it.

Schemes commonly occur within a single domain or sub-domain in order to bind the context of the actions available to the scheme. For example, the [Approved Establishments Scheme](https://www.food.gov.uk/business-guidance/approved-food-establishments) has a scope which is laid out by the piece of legislation that creates the scheme, which for now is [Regulation (EC) 853/2004](https://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2004:139:0055:0205:EN:PDF).

### Related entities
A scheme has one or more [activities](/enterprise-data-models/entities/activity.html), [interventions](/enterprise-data-models/entities/intervention.html) or [enforcements](/enterprise-data-models/entities/enforcement.html) associated with it. Every one of these actions must be associated with a scheme, but the same action can appear in multiple schemes.

An [establishment](/enterprise-data-models/entities/establishment.html) is enrolled in a scheme, not the individual premises or operator, although in some existing services the enrolment is associated with one of those entities.

An establishment can be enrolled in multiple schemes.

Schemes are owned, managed, or carried out by [Competent Authorities](/enterprise-data-models/entities/competent-authority.html). For example FHRS is owned by the FSA but carried out by Local Authorities.

### Entity diagram
![scheme](/enterprise-data-models/entities/diagrams/Scheme.png)

### Synonyms
*   Policy
*   Domain
*   Area

### What it is not
A scheme is not a single piece of legislation or policy, it only becomes a scheme when there are activities, interventions or enforcements within the scope of the scheme.

Some "schemes" run by trade bodies or other entities might be called a scheme, but they are not included for the purposes of defining the scheme entity. Some of these may even have an impact on policy areas, such as the frequency of some inspections can be affected by a producer being a member of the [Red Tractor Assurance Scheme](https://www.redtractor.org.uk/). Red Tractor is not a scheme in our model.

## Properties, identifiers and reference data

### Key properties
We want to make sure schemes are handled consistently in services and databases, for this reason we will develop a register of schemes and publish it on the [FSA Registry](data.food.gov.uk/codes). The key properties from that register when storing the information in a table will be;

*   The URI of the scheme
*   The name of the scheme
*   The code (notation) for the scheme

### Contextual properties
There are additional properties that may be useful in services but this is often on a scheme by scheme basis, these properties include;

*   Geographical jurisdiction of the scheme
*   Effective dates for the scheme to be active
*   Specific product groups or establishments that the scheme relates to

Schemes may also have their own specific entities which are activities, interventions or enforcements. For example, the FHRS inspection is a specific type of the inspection entity, and it's contextual properties are laid out in the documentation for the scheme. Where possible, these specific implementations of entities will be included in this documentation.

## Reference data
A link to the first version of the scheme register will be updated once the register is built.

## External references and further reading
*   [Regulation (EC) 853/2004](https://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2004:139:0055:0205:EN:PDF) known as the Approved Establishments Scheme
*   The [Food Hygiene Ratings Scheme](https://www.food.gov.uk/safety-hygiene/food-hygiene-rating-scheme)
*   The [Raw Cow's Drinking Milk](https://www.food.gov.uk/business-guidance/raw-cows-drinking-milk) policy
