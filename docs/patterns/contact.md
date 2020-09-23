---
layout: default
title: Contact
nav_order: 4
has_children: false
parent: Patterns
categories: pattern
---

# Contact

This pattern was last updated **23/09/2020**, this is version **1.0**

Stable
{: .label .label-green }

### Pattern created

18/09/2020

## Description

A Contact is a set of information to record the name and contact details of an individual to facilitate communication.  The information recorded could vary depending on the context and business need.

At the FSA, common usage could be for the recording of stakeholders.

## Field formats, data types, and patterns

As a minimum a contact record will be made up of the following:

First name
Last name
Telephone number
Email address

Other optional elements may be added if required, these could include the following:

Title
Address
Organisation
Job Role
Notes
Communication preferences


###Notes
Email validation is actually broken down into the two elements before and after the `@` sign.  The first element is restricted to 64 characters and the second element 255 characters, however in practise most email address are less than 50 characters.  

It is recommended that contact information is reviewed periodically to ensure that personal information is relevant and up to date.  This may also necessitate the addition of other fields such as start and end dates or review dates

### SQL snippet
```sql
CREATE TABLE IF NOT EXISTS contacts (
  First_name          VARCHAR(35),
  Last_name           VARCHAR(35)
  Telephone_number    VARCHAR(20)
  Email               VARCHAR(320)
);
```

### References
[Dublin Core name guidance](https://www.dublincore.org/specifications/dublin-core/name-representation/)
[Telephone Number pattern](https://foodstandardsagency.github.io/enterprise-data-models/patterns/telephone-number.html)
