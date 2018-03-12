---
title: Plan and Requested Actions Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_plan_and_requested_actions.html
summary: "The FHIR profiles used for the Plan and Requested Actions Event Message Bundle"
---

{% include important.html content="The links below will refer to the StructureDefinition url applied to the FHIR profile, which are not yet active. For queries please refer to the Help and Support section." %} 

The following FHIR profiles are used to form the Plan and Requested Actions Event Message Bundle:

- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display for the event element is fixed to 'Plan and Requested Actions'
- [CareConnect-DCH-Organization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-DCH-Location-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Location-1)
- [DCH-ChildHealth-CarePlan-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-ChildHealth-CarePlan-1)
- [DCH-RelatedPerson-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-RelatedPerson-1)
- [CareConnect-DCH-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Practitioner-1)
- [CareConnect-DCH-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PractitionerRole-1)


### Plan and Requested Actions event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item     | FHIR resource element                           | Mandatory/Required/Optional |
|-------------------|-------------------------------------------------|-----------------------------|
| Date              | CareConnect-DCH-Encounter-1.period.start        | Mandatory                   |
| ODS Site Code     | CareConnect-DCH-Location-1.identifier           | Mandatory                   |
| SDS Job Role Name | CareConnect-DCH-PractitionerRole-1.code         | Mandatory                   |
| Professional Name | CareConnect-DCH-Practitioner-1.name             | Mandatory                   |
| Actions           | DCH-ChildHealth-CarePlan-1.description          | Mandatory                   |
| Recipient         | DCH-RelatedPerson-1.relationship                | Optional                    |
| Encounter Type    | CareConnect-DCH-Encounter-1.type (childHealthEncounterType)                 | Mandatory                   |

