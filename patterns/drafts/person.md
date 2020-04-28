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
The fields and data types required will be dependent on the system and the relationship the person has with the FSA.

### FSA Staff
By putting an email address through Delv, you can retrieve the relevant information for staff members including name, role, line manager and contact details.  Many systems built from O365 tools should be able to retrieve any additional information using this piece of information.  Indeed this could be automated to the point so that when a user navigates to a page or app that their Microsoft credentials are automatically captured and used to login.

| Field | Field Type |
|--------------|--------|
| FSA E-mail | firstname.lastname@food.gov.uk |

### Contractors / Competent Authority Representative
If the contractors have an FSA account you can just record their FSA email address.  If the contractors doesn't have an FSA email address the following will be required

| Field | Field Type |
|--------------|--------|
| Prefix | Lookup |
| First name | Text |
| Sir name | Text |
| Organisation | Text |
| Phone number | Number |
| Email address | Text |

### Stakeholders
| Field | Field Type |
|--------------|--------|
| Prefix | Lookup |
| First name | Text |
| Sir name | Text |
| Organisation | Text |
| Phone number | Number |
| Email address | Text |

### Public
| Field | Field Type |
|--------------|--------|
| Prefix | Lookup |
| First name | Text |
| Sir name | Text |
| Email address | Text |

## Notes
Some systems will require more fields, the information that is captured is defendant on the system and the person involved.
