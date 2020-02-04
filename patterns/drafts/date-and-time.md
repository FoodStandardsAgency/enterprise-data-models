# Date and Time

This pattern was last updated 04/02/2020, this is version 1.0

Pattern Created: 21/01/2020

While date is a fundamental data type, and used in the FSA in the same way as other organisations, we have a set of styles and best practices when working with dates in data for development teams to follow.

### Format

At the FSA we only use the international standard for recording date and time, ISO 8601. You should use the extended format (which includes separators) to make dates more readable for users working with the database directly, this is the format which includes separators.

#### Format for date only

When recording a date only, the format is `YYYY-MM-DD`.

For example, 14 January 2020 is `2020-01-14`.

#### Format for a date and time

When we need to record a time as well as a date, we should always record the coordinated universal time (UTC). This might be different from the local time, including Greenwich Mean Time or British Summer Time.

The format for recording date and time is `<date>T<time>Z`, where `<date>` is formatted as `YYYY-MM-DD` and `<time>` is formatted as `hh:mm:ss` or `hh:mm:ss.sss` where fractions of second are required.

The separating `T` character and suffix `Z` character are required in all cases where time and date are recorded.

We may not always receive date and time data from third-parties to ISO 8601 standards. Where possible we must specify this standard as part of any data sharing agreement or contractual arrangements. Where this is not possible, we must validate dates and convert to the standard as part of ingestion.

### Patterns for implementing dates and times in services

The most common use for dates and times in our services is to record the beginning and end of when an activity applies to an establishment, or the existence of an item in a list.

There are multiple patterns for achieving this in services, generally you should be able to achieve most things where recording something over time using a combination of the following;

-   Start date
-   End date
-   Change date

## Start date

At the FSA, we use start date. When used as a field name it should be recorded as `start-date`, other names for the start of an event or record are unacceptable even when the business term is different.

Your service can and should present the field by it's accepted domain name if that term is so well-established as to be canonical or it is that way in legislation or defined that way in policy, but field conventions need to remain consistent across services.

## End date

We use end date to signify the end of an event or status. When used as a field name it should be recorded as `end-date`, other names for this field are unacceptable.

Like start date, your service can present the field by it's accepted domain name if that term is canonical.

## Change Date

We use change date to signify a change to an event or record that does not change the nature of the item enough to justify giving the item an end date and creating a new item. For example if an entry for a school has an update to the head teacher field, it is still the same school thus the same item. However we needed to record a change to the item and the date the change occurred. When used as a field name it should be recorded as `change-date`, other names for this field are unacceptable


## Recording point in time data effectively and when to use change date

It is best practice to signify changes to a record using only start date and end date, with a new row for each material change. For example, we moved offices from Aviation House to Clive House in January 2018, which should be recorded in a service like this;

| organisation | office | start-date | end-date |
|--------------|--------|------------|---------|
| FSA | Aviation House | 2010-04-01 | 2017-12-31 |
| FSA | Clive House | 2018-01-01 ||

This format means that current status and point in time reporting are supported easily by using the correct query technique.
