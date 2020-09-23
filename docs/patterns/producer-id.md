---
layout: default
title: Producer ID
nav_order: 8
has_children: false
parent: Patterns
categories: pattern
---

# Producer ID

This pattern was last updated **17/03/2020**, this is version **1.0**

Stable
{: .label .label-green }

### Pattern created

13/03/2020

## Description
The Producer ID is allocated to a registered Dairy Food Business Operator (FBO) once dairy activities have been registered. The Producer Id is used to record activities and interventions associated with the FBO eg Inspection outcomes. The ID is used for Internal reference only, external communications with Dairy FBOs use the 'County Parish Holding' number.

## Field formats, data types, and patterns

The format for new Producer ID is 5 numerical digits, however, older references may have fewer digits eg `12345`, `2212`, `742`.

### Notes

### SQL snippet
```sql
CREATE TABLE IF NOT EXISTS producer (
  producerID integer(5) NOT NULL UNIQUE
);
```

### Additional information
[County Parish Holding Number](docs/patterns/county-parish-holding.md)
