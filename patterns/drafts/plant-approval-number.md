---
layout: default
title: Plant Approval Number
nav_order: 6
has_children: false
parent: Patterns
categories: pattern
---

# Plant Approval Number

This pattern was last updated **18/03/2020**, this is version **1.0**

Stable
{: .label .label-green }

### Pattern created

27/02/2020

## Description
The Plant Approval Number is allocated to a registered Food Business Operator (FBO) once meat activities have been approved.  The Plant Approval Number is used to record activities and interventions associated with the FBO eg the Plant Approval Number is used to record inspection outcomes.

## Field formats, data types, and patterns
There are different formats of Plant Approval Number depending on the Approver eg FSA or Local Authority.

### FSA approved
FSA approval for Slaughterhouses and Cutting Plants using the following formats
-   4 digit numeric number in the format NNNN, or
-   9 digit reference consisting of two groups of 4 digit numbers separated by a hyphen in the format NNNN-NNNN.  This format is used for FBOs situated within a market, where the 1st part will refer to the market and the 2nd part will refer to the individual FBO.

### Local Authority approved
Local Authorities as Competent Authorities approve Cold Stores, Meat Processing Plants, Meat Producers etc using the following format
-   Two digit alpha characters, followed by a space and 3 numeric digits in the format AA NNN

### SQL snippet
```sql
CREATE TABLE "PlantApprovalNumber" (
  "plant-approval-number" VARCHAR(12) NOT NULL
);
```
## Notes
Analysis of the Approved food Establishments dataset at January 2020 has highlighted that there are a number of different formats in use, particularly in respect of Local Authority approved establishments, the longest of which is 12 characters long.
