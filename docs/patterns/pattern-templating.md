---
layout: default
title: Pattern Templating
nav_order: 2
has_children: false
categories: templating
---

# Pattern Templating
Our data patterns are small, repeatable designs for individual properties or fields.

They are our attempt to intentionally design our data so it is consistent across services. The ambition is to simplify the development process, particularly for logical data models.

They are not exhaustive, and developers should extend them where necessary but to support the adoption of the patterns across our estate we require patterns applied to all services.

The following section describes the formats we use for patterns, the latter section details the templating for them. Patterns are templated a little more loosely than our entities, but follow the same basic structure.

## Pattern structure
The majority of our patterns are simple. They describe what the pattern is, where is it most commonly used and describe how to create the pattern in a data system or service. It provides guidance for field name(s), formatting, and data types as well advice on how to present the pattern to the user where appropriate.

Some patterns are more complex. These happen when the domain the pattern forms a part of is complex or has multiple implementations across the business. These patterns can have up to three parts;

1.  Simple pattern
2.  Extended pattern
3.  Display pattern

In this example, let's consider the pattern for address data.

### Simple patterns
Simple patterns are the most basic implementation we can use and still have a functioning data model. Simple patterns are best used when prototyping or the early phases of development, they help you get up and running.

In our address example, a simple pattern might include the basic fields returned by our address matching service of choice that would allow you to store the equivalent of a basic postal address in a database, something like;

| house_number | street_name | postal_town | post_code |
|--------------|-------------|-------------|-----------|
| 1 | Varchar Avenue | Dataville | AB12 3DE |

### Extended patterns
Extended patterns are for use in live services. Utilising extended patterns will mean the data across services is interoperable now and in the future. They may include a number of fields that are of little immediate use to the service, but we feel the initial overhead to include them is small and that the long term payoff of complete interoperable data makes using them worthwhile.

In our address example, we may specify an address matching service which is the default for use in the FSA. We would point to the documentation for that service and say;

-   Either use every field returned by the service, irrespective of whether you use them all, or
-   Use a specific set if fields in all cases, and individual services can extend beyond this subset as needed

As we begin implementing these extended patterns, we would actively seek feedback from developers and users of the underlying data to make sure they have the correct level of detail to continue to be useful to the organisation and maintain interoperability with other data sets.

### Display patterns
Display patterns are only required when there is a significant difference between how the data is stored and common expectations of how it is presented. They are not designed to substitute for robust user research, but some patterns are so common that it is useful to use them as a consistent baseline, particularly when prototyping services.

These patterns are not designed to supersede or replace any in the FSA pattern library, and should be considered secondary to that product - but sometimes it is helpful to template them. Addresses are a good example;

> 1 Varchar Avenue  
> Dataville  
> AB12 3DE

---

## Last updated, version and status
Our patterns start with the date they were last updated and the version number. Stable patterns are numbered incrementally from 1.0, and experimental patterns incrementally from 0.0.

> This entity was last updated on **01/01/2020**. This is version **1.0**

We indicate if the pattern is experimental or stable. Sometimes a pattern needs significant drafting and discussion before we nail it down (looking at you address pattern), and we would like to do that in the open to encourage collaboration.

We use the following labels to indicate the status of a pattern.

Experimental
{: .label .label-yellow }

or

Stable
{: .label .label-green }

## Description
Here we try to describe what the pattern is and why it exists. Some patterns relate to very narrow concepts that could be considered very small entities, the `County Parish Holding` pattern is a good example of this. Other patterns are really templates for best practice, they either point to existing standards or implementations, or demonstrate our preferred architectural approaching for applying those standards, our patterns for handling `dates and times` is an example of this.

## Field formats, data types, and patterns
In this section we specifically provide the information needed to correctly store the data for the pattern. This can range from instructing a data type or field length, to providing templates for properly splitting a complex reference number into constituent fields.

## Notes, references, and further reading
Where others have developed good quality patterns which are open, we don't think twice about using them ourselves. It makes sense to re-use the work of others across government, this is where we will link out to those patterns. When using other patterns, the two preceding sections will be as small as possible and a link to the external pattern provided. Not everyone has all day to read this stuff.

Some of our patterns are a combination of existing implementation, best practice, folksy wisdom, and trial and error. Our patterns may be informed by multiple sources, including other patterns and standards. Our patterns will try to convey how we came to the design we have, but sometimes users may want a more nuanced understanding of how we came to that design, we will link to our sources.
