---
layout: default
title: County Parish Holding
nav_order: 5
has_children: false
parent: Patterns
categories: pattern
---

# County Parish Holding Number

This pattern was last updated **20/02/2020**, this is version **2.0**

Stable
{: .label .label-green }

### Pattern created

10/01/2020

## Description
The County Parish Holding number identifies one or more parcels of land, which when grouped together form a holding.

In the FSA it is used for the purposes of linking with data from external sources, including (but not limited to);
-   Animal and Plant Health Agency
-   Red Tractor Farm Assurance
-   Environment Agency
-   Public Health England

The County Parish Holding Number is the reference number used when communicating with Dairy Food Business Operators. The FSA allocated [Producer ID](/enterprise-data-models/patterns/producer-id.html) associated with registered Dairy FBOs is only used internally.

## Field formats, data types, and patterns
When working with the CPHN in the FSA our preferred pattern to split the CPHN in to three separate fields;
1. A numeric field of two digits in the format `00`, this is the number associated with a county, with the field name `cph-county`.
2. A numeric field of three digits in the format `000`, this is the number associated with a parish, with the field name `cph-parish`.
3. A numeric field of four digits in the format `0000`, this is the number associated with a holding, with the field name `cph-holding`.

Often the CPHN will be provided as an alphanumeric string, in the format `01/234/5678`. This will need to be parsed to be stored correctly.

### Notes
Sometimes a CPHN can include a herd number, which is an additional two digits after the holding number, we do not use these.

### SQL snippet
```sql
CREATE TABLE "CountyParishHolding" (
  "cph-county" NUMERIC(2) NOT NULL,
  "cph-parish" NUMERIC(3) NOT NULL,
  "cph-holding" NUMERIC(4) NOT NULL
);
```

### Additional information
*   [gov.uk guidance on County Parish Holdings](https://www.gov.uk/guidance/register-land-you-use-to-keep-livestock)
