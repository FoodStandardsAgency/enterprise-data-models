---

layout: default
title: Address
nav_order: xx
has_children: false

---

Experimental
{: .label .label-yellow }

# address-uk

This pattern was last updated 02//032020, this is version 0.5

Pattern Created: 24/01/2020.  This pattern is experimental.

An address is one of the most if not the most complex artifacts that we store at the FSA, the way that we expect to read them, record them and store them is all different depending on the context. They are also highly resilient to inaccuracy for their original use: going to a place or sending an item to a place. This resilience, is in large part, due to the processes for their use being highly manual. A postman/ postwoman knows their route, and with part of an address, or a mostly accurate address can deliver to that address successfully, the same is true when traveling to an address, if the address is accurate enough people can find a location using context when they arrive. However as the world becomes more automated good enough, will no longer be good enough. A self driving car or drone needs exact information, it cannot use human intuition. The first time I went to the [york foss house office](https://goo.gl/maps/k1P6RtJ1jRWwXzV89) I ended up walking to a nearby block of flats, also called [Foss House](https://goo.gl/maps/86EmNP4RWA4Lu6X37) because google maps did not know which foss house, York I had been referring to.

Due to addresses high resilience to inaccuracy, for their original use at least, they way that people record their address varies, do you include the postcode, should the house name/ number be on the same line as the road, what about a block of flats that share a house number i.e. `P Sherman, Flat 1, 42 wallaby way, Sydney`.

Due to this complexity there are three versions of the address pattern:
-   Display
    -   The Display version of the pattern is how we would display an address to our users. This version of the pattern matches what you would expect an address to look like and is the most human friendly.
-   Simple
    -   The simple version of the pattern is how an address should be stored when the additional address information captured in the Extended version is not required. This address pattern is not user friendly
-   Extended
    -   The extended version of the pattern is used when we want to record as much information about the address as possible. All addresses stored in the extended pattern must have been checked for accuracy. This address pattern is not user friendly and an address should not be shown to our users in this format.

It is recommended that an address matching service is used when capturing address data from our users in order to ensure the information we are recording is accurate. For more information about what address matching service should be used, and how to use it please contact the TDA.

For the patterns in this document, it is assumed that the address matching service used is ViaEuropa, If an alternate service has been used please modify the patterns, as detailed in each section, to match your address matching service.

### Display Format

The display address consists of five lines as follows.  This pattern covers the standard UK address pattern.  For delivery of mail the minimum requirements would be the addressee, town or city and postcode. This pattern is designed to be user friendly, but not very machine readable.

| Line No | Description  | Required | Can be NULL |
|:--------|:-------------|:---------|:------------|
| Line 1  | Building and Street | Required | No |
| Line 2  |              | Optional | Yes |
| Line 3  | Town or City | Required | No |
| Line 4  | County       | Optional | Yes |
| Line 5  | Postcode     | Required | No |

#### Notes
-   **Lines 1 and 2** - Street names should not be abbreviated eg Road, Lane, Street, Avenue should not be abbreviated to Rd, Ln, St or Ave.  (use of address matching service would cater for this).

-   **Line 2** is used if there is additional street or locale information eg

    Flat 3\
    15 Sycamore Avenue

    or

    Heron House\
    345 London Road

-   **Line 3** is used for the town or city (or locale, see example below), regardless of whether Line 2 has been populated.
In the example below, Lines 1 and 2 have been used for the house name and street, followed by a locale on line 3, with the Town or City on line 4


    Red Bank Farm\
    The Shore\
    Bolton Le Sands\
    CARNFORTH\
    LA5 8JR

-   **Line 4** - is used for the County, however, it is not actually required for mail delivery but is commonly included as part of the address.  Gov.uk shows line 4 as County in their address pattern (see reference below). It is possible for County to be missing from an address as in the above example.

-   **Minimum requirements** are that lines 1, 3 and 5 are populated.

### Simple Format

The simple format is how an address should be stored within a database. This format is designed to be machine readable not user friendly. So whilst information is stored in the simple format it should be presented to users in the display format detailed above.

| Field Name | Description  | Required | Can be NULL |
|:-----------|:-------------|:---------|:------------|
| UPRN | The UPRN is the unique property refernece number for an address, more information can be found in the UPRN pattern | No | Yes |
| Building name | The name of a building | Yes | Yes |
| Building number | The number of a building | Yes | Yes |
| Dependent Thoroughfare | A dependent thoroughfare, are named thoroughfares within another named thoroughfare. | No | Yes |
| Thoroughfare | A thoroughfare is the name of the road/ street/ etc used within the address | Yes | No |
| Post Town | The town or the city within the address | Yes | No |
| Dependent locality | A dependent locality defined an area within a post town i.e. Shirley, Southampton where Shirley is the dependent locality, and Southampton is the post town | No | Yes |
| postcode | The postcode for an address | Yes | Yes |

#### Notes
The fields used above are directly taken from the Delivery point address dataset within Addressbase, Which is the data behind the ViaEuropa API. These are the minimum fields which need to be captured in order to store an address in a machine readable Format

-   While building name and building number can be NULL, they cannot both be NULL

#### SQL
the SQL to generate the simple pattern can be found here. this SQL has been written for postgres so conversion may be necessary to another format:
```
CREATE TABLE IF NOT EXISTS simple
(
  UPRN                                 FLOAT8,
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

The extended pattern for an address is the complete list of fields used within the addressbase Delivery point address dataset. A full list can be found in the [addressbase technical specification here](https://www.ordnancesurvey.co.uk/documents/addressbase-technical-specification.pdf) The field list starts on page 11 and continues to page 17.

#### SQL
the SQL to generate the extended pattern can be found here. this SQL has been written for postgres so conversion may be necessary to another format Please note this SQL was accurate as of 02/03/2019 and any changes to the pattern since that date will not be present:

```
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
