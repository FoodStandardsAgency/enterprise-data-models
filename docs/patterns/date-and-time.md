---
layout: default
title: Date and Time
nav_order: 6
has_children: false
parent: Patterns
categories: pattern
---

# Date and Time

This pattern was last updated 21/02/2020, this is version 1.0

Stable
{: .label .label-green }

### Pattern Created
21/01/2020

## Description

While date is a fundamental data type, and used in the FSA in the same way as other organisations, we have a set of styles and best practices when working with dates in data for development teams to follow.

## Field formats, data types and patterns

At the FSA we only use the international standard for recording date and time, ISO 8601. You should use the extended format, including separators, to make dates more readable for users working with the database tables.

### Format for dates

When recording a date only, the format is `YYYY-MM-DD`.

For example, 14 January 2020 is `2020-01-14`.

### Format for a date and times

When we need to record a time as well as a date, we should always record the coordinated universal time (UTC). This might be different from the local time, including Greenwich Mean Time or British Summer Time.

The format for recording date and time is `<date>T<time>Z`, where `<date>` is formatted as `YYYY-MM-DD` and `<time>` is formatted as `hh:mm:ss` or `hh:mm:ss.sss` where fractions of second are required.

The separating `T` character and suffix `Z` character are required in all cases where time and date are recorded.

For example, 13:01 on the 1 January 2020 is formatted as; `2020-01-01T13:01:00Z` or `2020-01-01T13:01:00.000Z`

We may not always receive date and time data from third-parties to ISO 8601 standards. Where possible we must specify this standard as part of any data sharing agreement or contractual arrangements. Where this is not possible, we must validate dates and convert to the standard as part of ingestion.

### Notes, references and further reading
The most common use for dates and times in our services is to record the beginning and end of when an event happens or a change occurs.

Services can handle most needs by using the following:

-   xxxx-start-date
-   xxxx-end-date
-   xxxx-change-date

Where xxxx describes the thing or event that the start date represents, if it's necessary to use more than one word to describe the thing, then each word should be seperated by a hyphen. This is required to help identify different types of dates that will need to be recorded and used accross platforms. This is also necessary for linked data purposes where we need to identify what set of dates are being referred to.

### Start date
At the FSA, we use start date. When used as a field name it should be recorded as xxxx-start-date, other names for the start of an event or record are unacceptable even when the business term is different.

#### Example start dates
-   food-business-start-date
-   building-start-date

Your service can and should present the field by it's accepted domain name if that term is so well-established in the legislation or policy of that domain, but field conventions need to remain consistent across services.

### End date
We use end date to signify the end of an event. When used as a field name it should be recorded as xxxx-end-date.

Like start date, your service can present the field by it's accepted domain name if that term is canonical.

#### Example end dates
-   food-business-end-date
-   building-end-date

### Change date

We use change date to signify a change to an event or record that does not change the nature of the item enough to justify giving the item an end date and creating a new item. For example if an entry for a school has an update to the head teacher field, it is still the same school thus the same item. However we needed to record a change to the item and the date the change occurred. When used as a field name it should be recorded as xxxx-change-date, other names for this field are unacceptable

#### Example change dates
-   food-business-change-date
-   building-change-date

### Recording point in time data effectively and when to use change date

It is best practice to signify changes to a record using only start date and end date, with a new row for each material change. For example, we moved offices from Aviation House to Clive House in January 2018, which should be recorded in a service like this;

| organisation | office | Capacity | building-start-date | building-end-date | building-change-date |
|--------------|--------|----------|------------|----------|-------------|
| FSA | Aviation House | 1000 | 2010-04-01 | 2017-12-31 ||
| FSA | Clive House | 1200 | 2018-01-01 |||

This format means that current status and point in time reporting are supported easily by using the correct query technique.

However, some changes do not constitute a material change. In the above example lets change the capacity of clive house from 1200 to 1170 on the 1st of April 2020. This could be for many reasons. However it is still the same office. In this instance we would use the change date to show that the record has been updated.

| organisation | office | Capacity | building-start-date | building-end-date | building-change-date |
|--------------|--------|----------|------------|----------|-------------|
| FSA | Aviation House | 1000 | 2010-04-01 | 2017-12-31 ||
| FSA | Clive House | 1200 | 2018-01-01 |||
| FSA | Clive House | 1170 | 2018-01-01 || 2020-04-01 |
