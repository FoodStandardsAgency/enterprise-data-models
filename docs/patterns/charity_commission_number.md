---
layout: default
title: Charity Commission Number
nav_order: 2
has_children: false
parent: Patterns
categories: pattern
---

# Charity Commission Number

This pattern was last updated **23/09/2020**, this is version **1.0**

Stable
{: .label .label-green }

### Pattern created

18/09/2020

## Description

A Charity Commission Number is the identifier assigned to organisations which are registered with the Charity Commission for England and Wales or the Charity Commission Northern Ireland.

In the FSA, it is mostly used as a property of [operator](/enterprise-data-models/entities/operator.md), when the operator is a registered charity, similar to the [Company Registration Number](https://foodstandardsagency.github.io/enterprise-data-models/patterns/company-registration-number.html).

## Field formats, data types, and patterns

The pattern for storing Charity Commission Numbers in our services is to use an 8 character alphanumeric string.

From the Charity Commission Register for England and Wales, registration numbers are 7 numerical digits, rising to 8 numerical digits for more recent registrations. For Charity Commission Northern Ireland the registration numbers are 6 numerical digits. Eg `00000000` or `000000`.  Whilst these appear to be numerical, there is the possibility that the Northern Ireland numbers could have a suffix in the format `-0` to indicate that the charity is a sub charity, therefore the 8 digit alphanumeric string will also accommodate this.

### References
[Charity Commission for England and Wales](https://www.gov.uk/government/organisations/charity-commission).
[Charity Commission Northern Ireland](https://www.charitycommissionni.org.uk/)
