---
layout: default
title: Enforcement
nav_order:
has_children: True
---
# Enforcement
This model was last updated on **20/02/2020**, this is version **0.2**

Experimental
{: .label .label-yellow }

### Model created
10/02/2020
## Description
Enforcement is the term for the available actions to a `Competent Authority` to make establishments obey food or feed law, regulations, or policy which falls within a `scheme`.

Some examples include making the establishment change the way they operate in order to comply or removing the ability for the establishment to carry out activities until the changes are made.  This can also take the form of litigation, removal of services, suspension of licensing and fines.

### Related entities
Enforcement is part of a `scheme`. It represents the actions available to the `Competent Authorities` who own or run the scheme. Often, the available enforcement actions under the scope of a scheme will be laid out in the legislation or policy documentation.

Enforcement can happen to an `establishment`, `premises`, `operator` or an person depending on the specific enforcement action.

Enforcement action is often the result of unsuccessful `interventions`, but not always.

## Unique Identifiers
Where possible, lists of enforcements should be modelled as registers within the scope of a scheme and a code list created. The unique identifier should be the URI of the registry entry.

## What it is not
An enforcement is not an `intervention` although like an `intervention` it forms part of the regulation of a scheme.  Neither is it an `activity`, but all are associated with a `scheme`.

## Synonyms
*   litigation
*   prosecution
*   enforcement actions

## Key Properties
*   The URI of the registry entry for the enforcement action

## Contextual Property
When applying Enforcement actions it is important that the following is record;

The name of the `establishment` the enforcement was applied to. This will help build up a picture of how the `establishment` is performing and help schedule future `interventions` and possibly impact on future enforcements.

By recording the `Reason` for the Enforcement actions it gives `Competent Authorities` the ability to look for trends and focus on area's for further `interventions`, or build a case for stronger enforcement.

The name of the `Competent Authority` that implemented the enforcement, because the establishment may have enforcement action taken by multiple `competent authorities` for the same `reason` and or same period.  It also gives other Competent Authorities a place to go to for further information for future interventions and enforcements.

It is important that the `start-date` of the enforcement is recorded as it can determine `end-date` of an enforcement action. It can also help identify cases of production during a period of time when the business shouldn't have been operating, and by having start and end dates of enforcement actions makes the task of identifying produce processed within these dates easier.

A history of `interventions` and enforcements occurring within an `Establishment`. This will help build a picture and could impact on the severity of future enforcements by looking at the `establishments` history and looking for trends.


## Reference data
[Enforcement Actions](https://data.food.gov.uk/codes/enforcement-monitoring/_enforcement-actions)
