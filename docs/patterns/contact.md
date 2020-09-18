---
layout: default
title: Contact
nav_order: 2
has_children: false
parent: Patterns
categories: pattern
---

# Contact

This pattern was last updated **18/09/2020**, this is version **0.1**

Experimental
{: .label .label-yellow }

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

Other optional elements such as Title, Address, Organisation, Job Role may be added if required.

###Notes
Email validation is actually broken down into the two elements before and after the `@` sign.  The first element is restricted to 64 characters and the second element 255 characters, however in practise most email address are less than 40 characters.  

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