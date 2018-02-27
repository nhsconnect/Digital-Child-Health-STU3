---
title: Newborn Hearing Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_newborn_hearing.html
summary: "The FHIR profiles used for the Newborn Hearing Event Message Bundle"
---

{% include important.html content="The links below will refer to the StructureDefinition url applied to the FHIR profile, which are not yet active. For queries please refer to the Help and Support section." %} 

The following FHIR profiles are used to form the Newborn Hearing Event Message Bundle:

- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1.xml) - where the coding and display for the event element is fixed to 'Newborn Hearing'
- [CareConnect-DCH-Organization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Organization-1.xml)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1.xml)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1.xml)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1.xml)
- [CareConnect-DCH-Location-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Location-1.xml)
- [CareConnect-DCH-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Practitioner-1.xml)
- [CareConnect-DCH-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PractitionerRole-1.xml) 
- [CareConnect-DCH-HearingTest-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-HearingTest-Procedure-1)
- [CareConnect-DCH-HearingScreening-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-HearingScreening-Procedure-1)


The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:
                                                                     
| DCH Data Item       | FHIR resource element                                       | Mandatory/Required/Optional | Note                                                                  |
|---------------------|-------------------------------------------------------------|-----------------------------|-----------------------------------------------------------------------|
| Date                | CareConnect-DCH-Encounter-1.period.start                    | Mandatory                   |                                                                       |
| ODS Site Code       | CareConnect-DCH-Location-1.identifier                       | Mandatory                   |                                                                       |
| Professional Name   | CareConnect-DCH-PractitionerRole-1.code (SDS Job Role Name) | Mandatory                   |                                                                       |
| SDS Job Role Name   | CareConnect-DCH-Practitioner-1.name                         | Mandatory                   |                                                                       |
| Hearing Test Result | CareConnect-DCH-HearingTest-Procedure-1.outcome             | Required                    | up to two occurrences of this resource are required, one for each ear |
| Summary Outcome     | CareConnect-DCH-HearingScreening-Procedure-1.outcome        | Mandatory                   |                                                                       |