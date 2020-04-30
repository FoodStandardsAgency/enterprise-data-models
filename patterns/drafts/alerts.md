---
layout: default
title: Alerts
nav_order: ##
has_children: false
parent: Patterns
categories: pattern
---

# Alerts

This model was last updated on **30/04/2020**, this is version **0.1**

Experimental
{: .label .label-yellow }


### Pattern created

30/04/2020

## Description
Alerts are the formal process for official communications and approved actions as a result from a food or feed incident.  This can take one of three forms:

*   Allergen Alerts - informing consumers that a food item could contain ingredients that are not listed on the allergen label
*   Product recall information notice - such as a product recall for businesses, and consumers to check a product and not to consume if it falls within certain parameters
*   Food Alert for Action - where a competent authority has the powers to seize described items or carry out a prescribed action.

## Field formats, data types, and patterns
Alerts reference number is dependent on the type of alert that is issued but follow the following 15-17 character format.

*   FSA (Issuing Authority abbreviation)
*   Hyphen
*   Type of alert abbreviation Listed below
*   Hyphen
*   NNN Three digit numbers, this is sequential and resets each year
*   Hyphen
*   YYYY - Year the alert was issued displayed as a four character number

###Type of Alerts and example of format

*   **Allergen Alerts (AA)** would follow the following pattern **FSA-AA-NNN-YYYY**
*   **Product recall information notice (PRIN)** would follow the following pattern **FSA-PRIN-NNN-YYYY**
*   **Food Alert for Action (FAFA)** would follow the following pattern **FSA-FAFA-NNN-YYYY**


### Additional information
*   [Alert Entity Model](/enterprise-data-models/entities/alert.md)
*   [Summary of Incident Notifications received by the Food Standards Agency](https://data.food.gov.uk/catalog/datasets/f0db1a56-1088-4199-9e42-ddcde2546237)
*   [Annual Incident Reports (Historic Reports ends 2016/17)](https://data.food.gov.uk/catalog/datasets/77647fe3-5c51-43a5-82ce-1fcaf64479c2)
*   [Audit of Local Authority Service Delivery Controls for Incidents and Alerts](https://data.food.gov.uk/catalog/datasets/a32956fb-6039-4c63-9c98-68a641e89cb6)
*   [Quarterly Incident Reports (Alerts Only)](https://data.food.gov.uk/catalog/datasets/168f0873-4c1c-4bcf-8033-03342ed236e9)
