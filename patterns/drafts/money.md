---
layout: default
title: Money
nav_order: 6
has_children: false
---
# Money

This pattern was last updated 05/02/2020, this is version 0.1

Pattern Created: 05/02/2020.

Stable {: .label .label-green }

## Description

The Food Standards Agency (FSA) use the same money pattern as [ONS](https://www.ons.gov.uk/aboutus/transparencyandgovernance/datastrategy/datastandards#money) or

The Food Standards Agency collects and stores information about money in many places and in various forms, such as cost, price and amount. A common standard for recording this information is important for maintaining data consistency and quality. This standard is primarily developed for operational charging data. This can be used while exchanging data with third parties and is also suitable for use in other domains.

### Format

We have decided to use a numeric format, allowing negative numbers with a minimum of two decimal places. A separate variable should be used to capture the currency code unless the value is in Great British Pounds. A separate but optional variable may also be used to indicate unit of quantity such as thousands or millions.  Justification of cells should be to the right.


| Description | Cost £ |
| ----------------------------| -----------:|
| One Pence  | 0.01 |
| Ten Pence | 0.10 |
| One Pound   | 1.00 |
| Ten Pound | 10.00 |    
| One Hundred Pound | 100.00 |
| One Thousand Pound | 1000.00 |
| Ten Thousand Pound | 10000.00 |
| One Hundred Thousand Pound | 100000.00 |
| One Million Pound | 1000000.00 |

For accounting purposes the FSA occasionally rounds to the nearest 1000 this usually has the following displayed in the column header as Cost (000).  For Example

| Cost £ | Display as | Description |
|-----------: |--------: |--------------------- |
| 123456.00 | 123 | Rounding to nearest thousand |
| 123689.00 | 124 | Rounding to nearest thousand |
| 12343256.00 | 12  | Rounding to nearest million |
| 12873256.00 | 13  | Rounding to nearest million |

Negative or minus figures can be displayed with a prefix of - please see table below for example.

| Loss | Display as |
|------------------ |-------------: |
| minus 123456.00 | -123456.00 |


### References
-   [Currency code ISO 4217](https://en.wikipedia.org/wiki/ISO_4217)

#### Further reading
-   [Pound sterling](https://en.wikipedia.org/wiki/Pound_sterling)
-   [Currency_symbol](https://en.wikipedia.org/wiki/Currency_symbol)
