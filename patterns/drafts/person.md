---
layout: default
title: Person
nav_order: xx
has_children: false
parent: Patterns
categories: pattern
---

# Person

This pattern was last updated **22/04/2020**, this is version **0.1**

Experimental
{: .label .label-yellow }

### Pattern created

22/04/2020

## Description
All systems at the FSA have a person involved at one stage or another, some are FSA staff, others are external stakeholders employed by the FSA to carry out tasks, others are interested parties.

When collating and storing information on people its important to ensure that there is a privacy impact assessment in place and if not one created, and that the appropriate amount of information is collected and that it is collated for a specific purpose.

## Field formats, data types, and patterns


### FSA Staff
By putting an email address through Delv, you can retrieve the relevant information for staff members including name, role, line manager and contact details.  Many systems built from O365 tools should be able to retrieve any additional information using this piece of information.  Indeed this could be automated to the point so that when a user navigates to a page or app that their Microsoft credentials are automatically captured and used to login.

*   FSA E-mail  

### Contractors
If the contractors have an FSA account you can just record their FSA email address.  If the contractors doesn't have an FSA email address the following will be required
*   Prefix
*   First name
*   Sir name
*   Organisation
*   Phone number
*   Email address


### Stakeholders
*   Prefix
*   First name
*   Sir name
*   Organisation
*   Phone numbers
*   Email address

### Public
*   Prefix
*   First name
*   Sir name
*   Organisation
*   Phone numbers
*   Email address

## Notes
Analysis of the Approved food Establishments dataset at January 2020 has highlighted that there are a number of different formats in use, particularly in respect of Local Authority approved establishments, the longest of which is 12 characters long.
