---
title: Information and Advice Given Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_information_and_advice_given.html
summary: "The FHIR profiles used for the Information and Advice Given Event Message Bundle"
---

The following FHIR profiles are used to form the Information and Advice Given Event Message Bundle:

- [DCH-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-Bundle-1)
- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display elements for the 'event' type are fixed to 'CH017 - Information And Advice Given'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [CareConnect-DCH-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Practitioner-1)
- [CareConnect-DCH-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PractitionerRole-1)
- [DCH-InformationAndAdviceGiven-Communication-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-InformationAndAdviceGiven-Communication-1)
- [DCH-RelatedPerson-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-RelatedPerson-1)


### Information and Advice Given Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item               | FHIR resource element                                               | Mandatory/Required/Optional |
|-----------------------------|---------------------------------------------------------------------|-----------------------------|
| Date/Time                        | DCH-InformationAndAdviceGiven-Communication-1.sent                            | Mandatory                   |
| ODS/ORD Site Code              | CareConnect-Location-1.identifier (ODS Site Code)               | Required
| Performing Professional          | CareConnect-DCH-Practitioner-1.name                                 | Required                   |
| SDS Job Role Name           | CareConnect-DCH-PractitionerRole-1.code (SDS Job Role Name) 		| Required                   |
| Information Or Advice Given | DCH-InformationAndAdviceGiven-Communication-1.payload.contentString  | Required                    |
| Recipient                   | DCH-RelatedPerson-1.relationship                                    | Required                    |

### Reference Linkage Diagram ###

<img src="LINK TO FOLLOW">

### Problem List Bundle XML Example ###

<script src="LINK TO FOLLOW"></script>

### Problem List Bundle JSON Example ###

<script src="LINK TO FOLLOW"></script>