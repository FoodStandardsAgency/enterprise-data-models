---
layout: default
title: Vehicle Registration Number
nav_order: xx
has_children: false
parent: Patterns
categories: pattern
---

# `Vehicle Registration Number`

This pattern was last updated **06/05/2020**, this is version **0.1**

Stable
{: .label .label-green }

### Pattern created

09/04/2020

## Description

Vehicle Registration Numbers are primarily used by the FSA when details are passed to the Animal Plant Health Authority in connection with transportation incidents.

## Field formats, data types, and patterns

There are two systems of registration, one for Great Britain and one for Northern Ireland

Formats have only been provided for current registration formats. However there may be instances of private registrations or older registrations.  A string limit of 8 characters would be sufficient to cater for the standard and private variations based on both the formats below and regardless of whether the space delimeter is recorded.

### Great Britain

The standard format for Great Britain is 2 alpha characters signifying an area code, followed by 2 numeric characters to signify an age identifier, a space and then 3 random alpha characters - `AANN AAA`, eg `BD51 SMR`

### Northern Ireland

The standard format for Northern Ireland is 3 alpha characters where the last two characters represent an area, followed by a space and then 4 numeric characters - `AAA NNNN`, eg `BDZ 6357`

### SQL snippet
```sql
CREATE TABLE IF NOT EXISTS veh-reg-number (
  vehicle-reg VARCHAR(8)
);
```

### Additional information
-   [Great Britain vehicle registraions](https://en.wikipedia.org/wiki/Vehicle_registration_plates_of_the_United_Kingdom)
-   [Northern Ireland vehicle registrations](https://en.wikipedia.org/wiki/Vehicle_registration_plates_of_Northern_Ireland)
