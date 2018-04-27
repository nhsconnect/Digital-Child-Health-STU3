---
title: Professional Comment Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_professional_comment.html
summary: "The FHIR profiles used for the Professional Comment Event Message Bundle"
---

The following FHIR profiles are used to form the Professional Comment Event Message Bundle:

- [DCH-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-Bundle-1)
- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display elements for the event type are fixed to 'CH026 - Professional Comment'
- [CareConnect-DCH-Organization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-DCH-Location-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Location-1)
- [CareConnect-DCH-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Practitioner-1)
- [CareConnect-DCH-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PractitionerRole-1)
- [DCH-ProfessionalComment-Communication-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-ProfessionalComment-Communication-1)
- [DCH-RelatedPerson-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-RelatedPerson-1)


### Professional Comment Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

|| DCH Data Item     | FHIR resource element                                               | Mandatory/Required/Optional |
|-------------------|---------------------------------------------------------------------|-----------------------------|
| Date              | DCH-ProfessionalComment-Communication-1.sent                            | Mandatory                   |
| ODS Site Code     | CareConnect-DCH-Location-1.identifier (ODS Site Code)               | Mandatory                   |
| SDS Job Role Name | CareConnect-DCH-PractitionerRole-1.code (SDS Job Role Name)         | Mandatory                   |
| Professional Name | CareConnect-DCH-Practitioner.name                                   | Mandatory                   |
| Comment Type      | DCH-ProfessionalComment-Communication-1.category                    | Mandatory                   |
| Comment           | DCH-ProfessionalComment-Communication-1.payload.contentString       | Required                    |
| Recipient         | DCH-RelatedPerson-1.relationship                                    | Optional                    |
| Encounter Type    | CareConnect-DCH-Encounter-1.type (childHealthEncounterType)                                     | Mandatory                   |
