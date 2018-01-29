---
title: Professional Comment Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_professional_comment.html
summary: "The FHIR profiles used for the Professional Comment Event Message Bundle"
---
{% include custom/under.construction.html content="Please check back later for any updates to this page" %}

The following FHIR profiles are used to form the Professional Comment Event Message Bundle:

- DCH-MessageHeader-1 - where the coding and display elements for the event type are fixed to 'Professional Comment'
- CareConnect-DCH-Organization-1
- DCH-HealthcareService-1
- CareConnect-DCH-Patient-1
- CareConnect-DCH-Encounter-1
- DCH-ProfessionalComment-Communication-1
- DCH-RelatedPerson-1
- CareConnect-DCH-Practitioner-1
- CareConnect-DCH-PractitionerRole-1
- CareConnect-DCH-Location-1

### Professional Comment event data item mapping to FHIR profiles ###
----------
The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

|| DCH Data Item     | FHIR resource element                                               | Mandatory/Required/Optional |
|-------------------|---------------------------------------------------------------------|-----------------------------|
| Date              | CareConnect-DCH-Encounter-1.period.start                            | Mandatory                   |
| ODS Site Code     | CareConnect-DCH-Location-1.identifier (ODS Site Code)               | Mandatory                   |
| SDS Job Role Name | CareConnect-DCH-PractitionerRole-1.code (SDS Job Role Name)         | Mandatory                   |
| Professional Name | CareConnect-DCH-Practitioner.name                                   | Mandatory                   |
| Comment Type      | DCH-ProfessionalComment-Communication-1.category                    | Mandatory                   |
| Comment           | DCH-ProfessionalComment-Communication-1.payload.contentString       | Required                    |
| Recipient         | DCH-RelatedPerson-1.relationship                                    | Optional                    |
| Encounter Type    | CareConnect-DCH-Encounter-1.type                                    | Mandatory                   |
