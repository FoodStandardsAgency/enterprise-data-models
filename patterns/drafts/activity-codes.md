---
layout: default
title: Activity Code
nav_order: 1
has_children: false
---

# Activity Codes
This pattern was last updated 05/02/2020, this is version 0.1

Pattern Created: 05/02/2020.

Experimental {: .label .label-yellow }

## Description
In the FSA business context an activity is something that happens within the food and feed sector or the regulation of that sector by the FSA or other `Competent Authority` that needs to be recorded. Not all things that happen are an activity.

The activity code identifies an activity carried out by one or more of the following;

-   The FSA or another competent authority
-   Awarding body for scheme or activity
-   Food business operator
-   Establishment

### Format
When working with activity codes in the FSA our preferred pattern to split the Activity code in to two separate fields;
1. A numeric field of two digits in the format `00`, this is the number associated with activity type
2. A numeric field of three digits in the format `000`, this is the number associated with a activity within the activity type.

## Reference data
 [activities register](https://data.food.gov.uk/codes/organisation/_activities)


#### Notes
The reference number found in the Activity Code will be a five digit code that comprises of the two components listed above.  This pattern outlines how the activity codes are created.  There is no need for users to manually amalgamate the two reference numbers once the Activity Code has been created.

#### Additional Information
