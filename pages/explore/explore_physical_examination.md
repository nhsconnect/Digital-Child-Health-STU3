---
title: Physical Examination Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_physical_examination.html
summary: "The FHIR profiles used for the Physical Examination Event Message Bundle"
---
{% include custom/under.construction.html content="Please check back later for any updates to this page" %}

{% include important.html content="The links below will refer to the StructureDefinition url applied to the FHIR profile, which are not yet active. For queries please refer to the Help and Support section." %} 

The following FHIR profiles are used to form the Physical Examination Event Message Bundle:

- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1.xml) - where the coding and display for the event element is fixed to 'Physical Examination'
- [CareConnect-DCH-Organization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Organization-1.xml)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1.xml)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1.xml)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1.xml)
- [CareConnect-DCH-Location-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Location-1.xml)
- [CareConnect-DCH-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Practitioner-1.xml)
- [CareConnect-DCH-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PractitionerRole-1.xml)
- [CareConnect-DCH-PhysicalExaminationHips-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PhysicalExaminationHips-Procedure-1)
- [CareConnect-DCH-PhysicalExaminationEyes-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PhysicalExaminationEyes-Procedure-1)
- [CareConnect-DCH-PhysicalExaminationTestes-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PhysicalExaminationTestes-Procedure-1)
- [CareConnect-DCH-PhysicalExaminationHeart-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PhysicalExaminationHeart-Procedure-1)

### Physical Examination Details event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:
                                                                                                   
| DCH Data Item         | FHIR resource element                                               | Mandatory/Required/Optional |
|-----------------------|---------------------------------------------------------------------|-----------------------------|
| Date/Time             | CareConnect-DCH-Encounter-1.period.start                       | Mandatory                    |
| ODS Site Code         | CareConnect-DCH-Location-1.identifier (ODS Site Code)               | Mandatory                   |
| Professional Name     | CareConnect-DCH-Practitioner-1.name                                 | Mandatory                   |
| SDS Job Role Name     | CareConnect-DCH-PractitionerRole-1.code (SDS Job Role Name) | Mandatory                   |
| Outcome Status Hips   | CareConnect-DCH-PhysicalExaminationHips-Procedure-1.outcome         | Mandatory                   |
| Outcome Status Eyes   | CareConnect-DCH-PhysicalExaminationEyes-Procedure-1.outcome         | Mandatory                   |
| Outcome Status Testes | CareConnect-DCH-PhysicalExaminationTestes-Procedure-1.outcome       | Mandatory                   |
| Outcome Status Heart  | CareConnect-DCH-PhysicalExaminationHeart-Procedure-1.outcome        | Mandatory                   |
| Encounter Type        | CareConnect-DCH-Encounter-1.type (childHealthEncounterType)                                     | Mandatory                   |