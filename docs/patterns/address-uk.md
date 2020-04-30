---
layout: default
title: Address (UK)
nav_order: 1
has_children: false
parent: Patterns
categories: pattern
---

# Address (UK)

This pattern was last updated 30/04/2020, this is version 0.7.

Very Experimental
{: .label .label-yellow }

### Pattern Created
24/01/2020

## Description

An address is one of the most complex pieces of data that we use. The way we expect to read them, record them, and store them are different depending on the context.

They are resilient to inaccuracy for their original use; going to a place or sending an item to a place. This resilience is because the processes in which they are commonly used are mostly manual. A postman knows their route, and with part of an address, or a mostly accurate address can deliver to that address successfully.

The same is true when travelling to an address, if the address is accurate enough people can find a location using context when they arrive. However as the world becomes more automated, good enough will no longer be good enough. A self driving car or drone needs exact information, it cannot use human intuition.

As an example, the first time one of the Data Team went to the [Foss House](https://goo.gl/maps/k1P6RtJ1jRWwXzV89) in York, they ended up walking to a nearby block of flats, also called [Foss House](https://goo.gl/maps/86EmNP4RWA4Lu6X37) because the mapping service being used did not know which Foss House was correct.

Another effect of resilience to inaccuracy is the in way that people record their address. Do you include the postcode? Should the house name or number be on the same line as the road? What about a block of flats that share a house number? For example;

>P Sherman, Flat 1, 42 Wallaby Way, Sydney  

Because of this complexity there are three versions of the address pattern;

#### Display
The Display version of the pattern is how we would display an address to our users. This version of the pattern matches what you would expect an address to look like and is the most human friendly.

#### Simple
The simple pattern is how an address should be stored when the additional information in the extended version is not required. This address pattern is not user friendly. Some of the fields used will only apply when referencing a business address i.e. Organisation name but should still be included even if no businesses are currently in the list to allow flexibility if this changes in the future.

#### Extended
The extended version of the pattern is used when we want to record as much information about the address as possible. All addresses stored in the extended pattern must be checked for accuracy. This address pattern is not user friendly and should not be shown to our users in this format.

It is recommended that an address matching service is used when capturing address data from our users in order to ensure the information we are recording is accurate. For more information about the address matching service to be used, and how to use it please contact the Technical Design Authority.

For the patterns in this document, it is assumed that the address matching service used is `TBD`, If an alternate service has been used please modify the patterns, as detailed in each section, to match the address matching service used.

### Display format

The display address consists of five lines as follows.  This pattern covers the standard UK address pattern. For delivering mail the minimum requirements would be the addressee, town or city and postcode. This pattern is designed to be user friendly, but not very machine readable.

| Line No | Description  | Required | Can be NULL |
|:--------|:-------------|:---------|:------------|
| Line 1  | Building and Street | Required | No |
| Line 2  |              | Optional | Yes |
| Line 3  | Town or City | Required | No |
| Line 4  | County       | Optional | Yes |
| Line 5  | Postcode     | Required | No |

#### Notes
**Lines 1 and 2** - Street names should not be abbreviated eg Road, Lane, Street, Avenue should not be abbreviated to Rd, Ln, St or Ave.  (use of address matching service would cater for this).

**Line 2** is used if there is additional street or locale information eg

>Flat 3  
>15 Sycamore Avenue  

or

>Heron House  
>345 London Road  

**Line 3** is used for the town or city (or locale, see example below), regardless of whether Line 2 has been populated.
In the example below, Lines 1 and 2 have been used for the house name and street, followed by a locale on line 3, with the Town or City on line 4

>Red Bank Farm  
>The Shore  
>Bolton Le Sands  
>CARNFORTH  
>LA5 8JR  

**Line 4** - is used for the County, however, it is not actually required for mail delivery but is commonly included as part of the address.  Gov.uk shows line 4 as County in their [address pattern](https://design-system.service.gov.uk/patterns/addresses/).

It is possible for County to be missing from an address.

Our minimum requirements are that lines 1, 3 and 5 are populated.

### Simple Format

The simple format is how an address should be stored within a database for prototyping and early iterations of services. This format is designed to be machine readable but is not user friendly. Address data stored in the simple format should be presented to users in the display format.

| Field Name | Description  | Required | Can be NULL |
|:-----------|:-------------|:---------|:------------|
| UPRN | The UPRN is the unique property reference number for an address, more information can be found in the UPRN pattern | No | Yes |
| Organisation Name | Organisation Name for the delivery point at an address | No | Yes |
| Department Name | Department name for an address, can only be used when organisation name is not null | No | Yes |
| Sub Building Name | the sub building name or number for a property | No | Yes |
| Building Name | The name of a building | Yes | Yes |
| Building Number | The number of a building | Yes | Yes |
| Dependent Thoroughfare | A dependent thoroughfare, are named thoroughfares within another named thoroughfare. | No | Yes |
| Thoroughfare | A thoroughfare is the name of the road/ street/ etc used within the address | Yes | No |
| Post Town | The town or the city within the address | Yes | No |
| Dependent Locality | A dependent locality defined an area within a post town i.e. Shirley, Southampton where Shirley is the dependent locality, and Southampton is the post town | No | Yes |
| Post Code | The postcode for an address | Yes | Yes |

#### Notes
**While building name and building number can be NULL, they cannot both be NULL.**

These fields are taken from the delivery point address dataset within [OS Addressbase](https://www.ordnancesurvey.co.uk/business-government/products/addressbase). It is the data behind most address matching services which include UPRN data. These are the minimum fields which need to be captured in order to store an address to our standards.

#### SQL
This SQL will generate the simple pattern, it has been written for Postgres so conversion may be necessary for other databases.

```sql
CREATE TABLE IF NOT EXISTS simple
(
  UPRN                                 FLOAT8,
  ORGANISATION_NAME               VARCHAR(60),
  DEPARTMENT_NAME                 VARCHAR(60),
  SUB_BUILDING_NAME               VARCHAR(30),
  BUILDING_NAME                   VARCHAR(50),
  BUILDING_NUMBER                 NUMERIC(4,0),
  DEPENDENT_THOROUGHFARE          VARCHAR(80),
  THOROUGHFARE                    VARCHAR(80),
  DEPENDENT_LOCALITY              VARCHAR(35),
  POST_TOWN                       VARCHAR(30),
  POSTCODE                         VARCHAR(8),
);
```

### Extended Format
The extended pattern for an address is the complete list of fields used within the AddressBase delivery point address dataset. A full list can be found in the [AddressBase technical specification.](https://www.ordnancesurvey.co.uk/documents/addressbase-technical-specification.pdf) The field list starts on page 11 and continues to page 17.

#### SQL
This SQL will generate the extended pattern, it has been written for Postgres so conversion may be necessary for other databases.

```sql
CREATE TABLE IF NOT EXISTS deliverypointaddress
(
  RECORD_IDENTIFIER                   INTEGER,
  CHANGE_TYPE                         CHAR(1),
  PRO_ORDER                           INTEGER,
  UPRN                                 FLOAT8,
  UDPRN                           NUMERIC(8,0),
  ORGANISATION_NAME               VARCHAR(60),
  DEPARTMENT_NAME                 VARCHAR(60),
  SUB_BUILDING_NAME               VARCHAR(30),
  BUILDING_NAME                   VARCHAR(50),
  BUILDING_NUMBER                 NUMERIC(4,0),
  DEPENDENT_THOROUGHFARE          VARCHAR(80),
  THOROUGHFARE                    VARCHAR(80),
  DOUBLE_DEPENDENT_LOCALITY       VARCHAR(35),
  DEPENDENT_LOCALITY              VARCHAR(35),
  POST_TOWN                       VARCHAR(30),
  POSTCODE                         VARCHAR(8),
  POSTCODE_TYPE                       CHAR(1),
  DELIVERY_POINT_SUFFIX               VARCHAR,
  WELSH_DEPENDENT_THOROUGHFARE        VARCHAR,
  WELSH_THOROUGHFARE                  VARCHAR,
  WELSH_DOUBLE_DEPENDENT_LOCALITY     VARCHAR,
  WELSH_DEPENDENT_LOCALITY            VARCHAR,
  WELSH_POST_TOWN                     VARCHAR,
  PO_BOX_NUMBER                    VARCHAR(6),
  PROCESS_DATE                        VARCHAR,
  START_DATE                         CHAR(10),
  END_DATE                           CHAR(10),
  LAST_UPDATE_DATE                   CHAR(10),
  ENTRY_DATE                         CHAR(10)
);
```

### References
-   [Royal Mail - How to address mail](https://www.postoffice.co.uk/mail/how-to-address-mail)
-   [Premises Entity Model](https://foodstandardsagency.github.io/enterprise-data-models/entities/premises.html)

### Further reading
-   [UPRN numbers](https://www.ordnancesurvey.co.uk/business-government/tools-support/uprn)
-   [AddressBase](https://www.ordnancesurvey.co.uk/business-government/products/addressbase)
-   [Understanding UK address referencing](http://www.restore.ac.uk/geo-refer/91221ctuks00y00000000.php)
