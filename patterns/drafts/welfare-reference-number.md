---
layout: default
title: Welfare Reference Number
nav_order: xx
has_children: false
parent: Patterns
categories: pattern
---

# Welfare Reference Number

This pattern was last updated **28/04/2020**, this is version **0.1**

Experimental
{: .label .label-yellow }

### Pattern created

23/04/2020

## Description

The Welfare Reference number is used as a unique identifier for animal welfare incidents.  The reference number is used by the APHA when investigating incidents relating to animal welfare.  The reference number is constructed by the OV at the time of the incident and it is not uncommon for there to be several incidents on the same date.

These incidents are also recorded on Chronos which generates a common Chronos incident number, however the APHA use the OV generated reference number for their investigations and for communications back to the FSA.

## Field formats, data types, and patterns
The Welfare Reference Number is made up of three parts separated by forward slashes with no spaces.  A four digit [Plant Approval Number](https://github.com/FoodStandardsAgency/enterprise-data-models/blob/master/docs/patterns/plant-approval-number.md), followed by a numeric representation of the date in format ddmmyy, followed by 4 numerical digits representing the time of the incident - NNNN/ddmmyy/NNNN eg 3456/280420/0830.

### Regex validation

`([0-9]{4}\/[0-9]{6}\/[0-9]{4})`

### SQL snippet
```sql
CREATE TABLE welfareReferenceNumber (
  welfare-reference-number    VARCHAR(16)
);
```
