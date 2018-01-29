---
title: Referral Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_referral.html
summary: "The FHIR profiles used for the Referral Event Message Bundle"
---
{% include custom/under.construction.html content="Please check back later for any updates to this page" %}

The following FHIR profiles are used to form the Referral Event Message Bundle:

- DCH-MessageHeader-1 - where the coding and display elements for the 'event' type are fixed to 'Referral' 
- CareConnect-DCH-Organization-1
- DCH-HealthcareService-1
- CareConnect-DCH-Patient-1
- DCH-ReferralRequest-1
- CareConnect-DCH-Encounter-1
- CareConnect-DCH-Practitioner-1
- CareConnect-DCH-PractitionerRole-1
- CareConnect-DCH-Location-1

### Referral event data item mapping to FHIR profiles ###
----------
The Child Health Event data items are fulfilled by elements within the FHIR resources listed below.
                                                                                                   
| DCH Data Item                | FHIR resource element                                               | Mandatory/Required/Optional |
|------------------------------|---------------------------------------------------------------------|-----------------------------|
| Date of Referral             | DCH-ReferralRequest-1.dateSent                                      | Mandatory                   |
| ODS Site Code                | CareConnect-DCH-Location-1.identifier (ODS Site Code)               | Mandatory                   |
| Professional Name            | CareConnect-DCH-Practitioner-1.name                                 | Mandatory                   |
| SDS Job Role Name            | CareConnect-DCH-PractitionerRole-1.code (SDS Job Role Name)         | Mandatory                   |
| Encounter Type               | CareConnect-DCH-Encounter-1.type (childHealthEncounterType)         | Mandatory                   |
| Referred to                  | DCH-ReferralRequest-1.specialty                                     | Mandatory                   |
| Referral Method              | DCH-ReferralRequest-1.referralMethod (extension)                    | Required                    |
| Speciality referred from     | DCH-ReferralRequest-1.sourceOfReferral (extension)                  | Required                    |
| Urgency                      | DCH-ReferralRequest-1.priority                                      | Required                    |
| Reason for Referral          | DCH-ReferralRequest-1.reason                                        | Mandatory                   | 