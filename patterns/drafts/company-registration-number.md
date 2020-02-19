# Company Registration Number

This pattern was last updated 18/02/2020, this is version 0.1

Pattern Created: 18/02/2020.

Experimental
{: .label .label-yellow }

## Description

A Company Reference Number is the identifier assigned to companies which are registered with [Companies House](https://www.gov.uk/government/organisations/companies-house).

At the FSA, it is most frequently

## Field formats, data types, and patterns

Telephone number should be stored as a string entry in a single field, in order to preserve leading zeros and potential special characters used for international dialling codes and formatting (eg +, (), -).

A field length of 20 would allow for the following examples plus other international variants and spaces (guidelines within E.146 - International Telephone Formats would restrict to 15 characters for international numbers, 3 for country code and 12 for subscriber number, with all spaces and special characters removed (excluding '+' symbol for country code)).

-   01xxx xxxxxx
-   01xx xxx xxxx
-   020 xxxx xxxx
-   01xx xx xxxxx
-   +44 xxxx xxxx xxxx

## Notes

FSA use telephone numbers primarily to send alerts using the gov.uk Notify service.  Please see the relevant API documentation available through the reference below.

### References

-   [International standards for telephone number formats](https://en.wikipedia.org/wiki/E.164)
-   [International guidelines for presentation of telephone numbers](https://en.wikipedia.org/wiki/E.123)
-   [UK telephone numbers](https://en.wikipedia.org/wiki/Telephone_numbers_in_the_United_Kingdom)
-   [International Trunk Prefix](https://en.wikipedia.org/wiki/Trunk_prefix)
-   [Gov.UK.Notify service](https://www.notifications.service.gov.uk/features)

### Further reading

-   [GDS guidance re telephone numbers (currently experimental)](https://design-system.service.gov.uk/patterns/telephone-numbers/), this includes information on validation of telephone numbers
-   [Guidance regarding autocompletion of fields](https://www.w3.org/WAI/WCAG21/Understanding/identify-input-purpose.html)
-   [MojoLingo - Handling Phone Numbers: Best Practices for Developers](https://mojolingo.com/blog/2015/best-practices-handling-phone-numbers/)
-   [What data type would you use to store a phone number](https://teamtreehouse.com/community/what-data-type-would-you-use-to-store-a-phone-number)