---
layout: default
title: Company Registration Number
nav_order: 3
has_children: false
parent: Patterns
categories: pattern
---

# Company Registration Number

This pattern was last updated **19/02/2020**, this is version **1.0**

Stable
{: .label .label-green }

### Pattern created

18/02/2020

## Description

A Company Reference Number is the identifier assigned to companies which are registered with [Companies House](https://www.gov.uk/government/organisations/companies-house).

At the FSA, it is most frequently used as a property of [operator](/enterprise-data-models/entities/operator.md), when the operator is a limited company.

## Field formats, data types, and patterns

The pattern for storing company registrations in our services is to use an 8 character alphanumeric string.

Company registrations numbers can be a little inconsistent, but for the most part they are 8 characters and mostly numeric.

In England and Wales they take the format `00000000`.

In Scotland and Northern Ireland they are six numbers prefixed by `SC` or `NI` respectively. Their pattern is `SC000000` or `NI000000`.

Companies registered with the [Charity Commission](https://www.gov.uk/government/organisations/charity-commission) or the [Financial Conduct Authority](https://register.fca.org.uk/ShPo_HomePage) can have a registration number in a different format, but all of them should fit within an 8 character string.

### References
[This gist](https://gist.github.com/drkane/ef0c41aa19275a6c7cf1f3fff00356e6) will be of use if you want to know more about the possible patterns for company registration numbers and their meaning.
