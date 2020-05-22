---
layout: default
title: Wine Standards Board Reference Number
nav_order: 8
has_children: false
parent: Patterns
categories: pattern
---

# `Wine Standards Board Reference Number`

This pattern was last updated **22/05/2020**, this is version **0.2**

Stable
{: .label .label-green }

### Pattern created

13/03/2020

## Description
The Wine Standards Board (WSB) reference number is allocated to an [Establishment](docs/entities/establishment.md) once wine activities have been registered.  The WSB Reference Number is used to record activities and interventions associated with the wine establishment eg used to record Inspection outcomes.

## Field formats, data types, and patterns
The format for the WSB reference number is 5 numerical digits, however, older references may have fewer digits eg `73752`, `4462`, `753`.  Leading zeros are not used to pad out the number.

### SQL snippet
```sql
CREATE TABLE IF NOT EXISTS wsb-ref (
  wsb-reference-number integer(5) NOT NULL
);
```
