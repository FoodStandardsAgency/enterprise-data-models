---
layout: default
title: Charity Commission Number
nav_order: 2
has_children: false
parent: Patterns
categories: pattern
---

# Charity Commission Number

This pattern was last updated **18/09/2020**, this is version **0.1**

Experimental
{: .label .label-yellow }

### Pattern created

18/09/02

## Description

A Charity Commision Number is the identifier assigned to organisations which are registered with [The Charity Commission for England and Wales](https://www.gov.uk/government/organisations/charity-commission).

At the FSA, it is most frequently used as a property of [operator](/enterprise-data-models/entities/operator.md), when the operator is a registered charity.

## Field formats, data types, and patterns

The pattern for storing Charity Commission Numbers in our services is to use an 8 character alphanumeric string.

From examinig the Charity Commission Register, registration numbers are 7 numerical digits, rising to 8 numerical digits for more recent registrations.

In England and Wales they take the format `00000000`.

Charity Commission Northern Ireland






Companies registered with the [Charity Commission](https://www.gov.uk/government/organisations/charity-commission) or the [Financial Conduct Authority](https://register.fca.org.uk/ShPo_HomePage) can have a registration number in a different format, but all of them should fit within an 8 character string.

### References
[This gist](https://gist.github.com/drkane/ef0c41aa19275a6c7cf1f3fff00356e6) will be of use if you want to know more about the possible patterns for company registration numbers and their meaning.
