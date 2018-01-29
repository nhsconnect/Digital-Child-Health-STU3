---
title: Conditions / Diagnoses Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_conditions_diagnoses.html
summary: "The FHIR profiles used for the Conditions / Diagnoses Event Message Bundle"
---
{% include custom/under.construction.html content="Please check back later for any updates to this page" %}

The following FHIR profiles are used to form the Conditions / Diagnoses Event Message Bundle:

- DCH-MessageHeader-1 - where the coding and display elements for the 'event' type are fixed to 'Conditions or Diagnoses'
- CareConnect-DCH-Organization-1
- DCH-HealthcareService-1
- CareConnect-DCH-Patient-1
- CareConnect-DCH-Encounter-1
- CareConnect-DCH-Condition-1
- CareConnect-DCH-Location-1


### Conditions or Diagnoses event data item mapping to FHIR profiles ###
----------
The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item        | FHIR resource element                     | Mandatory/Required/Optional |
|----------------------|-------------------------------------------|-----------------------------|
| Condition            | CareConnect-DCH-Condition-1.code          | Mandatory                   |
| Condition category   | CareConnect-DCH-Condition-1.category      | Mandatory                   |
| Stage of Disease     | CareConnect-DCH-Condition-1.stage         | Optional                    |
| Condition onset Date | CareConnect-DCH-Condition-1.onsetDateTime | Required                    |
