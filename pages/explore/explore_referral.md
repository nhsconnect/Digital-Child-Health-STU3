---
title: Referral Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_referral.html
summary: "The FHIR profiles used for the Referral Event Message Bundle"
---
{% include custom/under.construction.html content="Please check back later for any updates to this page" %}

{% include important.html content="The links below will refer to the StructureDefinition url applied to the FHIR profile, which are not yet active. For queries please refer to the Help and Support section." %} 

The following FHIR profiles are used to form the Referral Event Message Bundle:

- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1.xml) - where the coding and display elements for the 'event' type are fixed to 'Referral' 
- [CareConnect-DCH-Organization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Organization-1.xml)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1.xml)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1.xml)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1.xml)
- [CareConnect-DCH-Location-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Location-1.xml)
- [CareConnect-DCH-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Practitioner-1.xml)
- [CareConnect-DCH-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PractitionerRole-1.xml)
- - [DCH-ReferralRequest-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-ReferralRequest-1.xml)


### Referral event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below.
                                                                                                   
| DCH Data Item                | FHIR resource element                                               | Mandatory/Required/Optional |
|------------------------------|---------------------------------------------------------------------|-----------------------------|
| Date of Referral             | DCH-ReferralRequest-1.dateSent                                      | Mandatory                   |
| ODS Site Code                | CareConnect-DCH-Location-1.identifier (ODS Site Code)               | Mandatory                   |
| Professional Name            | CareConnect-DCH-Practitioner-1.name                                 | Mandatory                   |
| SDS Job Role Name            | CareConnect-DCH-PractitionerRole-1.code (SDS Job Role Name)         | Mandatory                   |
| Encounter Type               | CareConnect-DCH-Encounter-1.type (childHealthEncounterType)  (childHealthEncounterType)         | Mandatory                   |
| Referred to                  | DCH-ReferralRequest-1.specialty                                     | Mandatory                   |
| Referral Method              | DCH-ReferralRequest-1.referralMethod (extension)                    | Required                    |
| Speciality referred from     | DCH-ReferralRequest-1.sourceOfReferral (extension)                  | Required                    |
| Urgency                      | DCH-ReferralRequest-1.priority                                      | Required                    |
| Reason for Referral          | DCH-ReferralRequest-1.reason                                        | Mandatory                   | 