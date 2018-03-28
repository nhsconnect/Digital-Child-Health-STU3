---
title: Referral Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_referral.html
summary: "The FHIR profiles used for the Referral Event Message Bundle"
---

{% include important.html content="The links below will refer to the StructureDefinition url applied to the FHIR profile, which are not yet active. For queries please refer to the Help and Support section." %} 

The following FHIR profiles are used to form the Referral Event Message Bundle:

- [DCH-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-Bundle-1)
- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display elements for the 'event' type are fixed to 'CH028 - Referral' 
- [CareConnect-DCH-Organization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-DCH-Location-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Location-1)
- [CareConnect-DCH-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Practitioner-1)
- [CareConnect-DCH-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PractitionerRole-1)
- [DCH-ReferralRequest-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-ReferralRequest-1)


### Referral Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below.
                                                                                                   
| DCH Data Item                | FHIR resource element                                               | Mandatory/Required/Optional |
|------------------------------|---------------------------------------------------------------------|-----------------------------|
| Date of Referral             | DCH-ReferralRequest-1.authoredOn                                      | Mandatory                   |
| ODS Site Code                | CareConnect-DCH-Location-1.identifier (ODS Site Code)               | Mandatory                   |
| Professional Name            | CareConnect-DCH-Practitioner-1.name                                 | Mandatory                   |
| SDS Job Role Name            | CareConnect-DCH-PractitionerRole-1.code (SDS Job Role Name)         | Mandatory                   |
| Encounter Type               | CareConnect-DCH-Encounter-1.type (childHealthEncounterType)         | Mandatory                   |
| Specialty Referred to        | DCH-ReferralRequest-1.specialty                                     | Mandatory                   |
| Referral Method              | DCH-ReferralRequest-1.referralMethod (extension)                    | Required                    |
| Specialty referred from      | DCH-ReferralRequest-1.sourceOfReferral (extension)                  | Required                    |
| Urgency                      | DCH-ReferralRequest-1.priority                                     | Required                    |
| Reason for Referral          | DCH-ReferralRequest-1.reasonCode                                        | Mandatory                   | 