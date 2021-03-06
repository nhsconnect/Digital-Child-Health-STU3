---
title: Plan and Requested Actions Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_plan_and_requested_actions.html
summary: "The FHIR profiles used for the Plan and Requested Actions Event Message Bundle"
---

The following FHIR profiles are used to form the Plan and Requested Actions Event Message Bundle:

- [DCH-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-Bundle-1)
- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display for the event element is fixed to 'CH025 - Plan and Requested Actions'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [DCH-PlanAndRequestedActions-CarePlan-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-PlanAndRequestedActions-CarePlan-1)
- [DCH-RelatedPerson-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-RelatedPerson-1)
- [CareConnect-DCH-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Practitioner-1)
- [CareConnect-DCH-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PractitionerRole-1)


### Plan and Requested Actions Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item     | FHIR resource element                           | Mandatory/Required/Optional |
|-------------------|-------------------------------------------------|-----------------------------|
| Date              | CareConnect-DCH-Encounter-1.period.start        | Mandatory                   |
| ODS Site Code     | CareConnect-Location-1.identifier           | Mandatory                   |
| SDS Job Role Name | CareConnect-DCH-PractitionerRole-1.code         | Mandatory                   |
| Professional Name | CareConnect-DCH-Practitioner-1.name             | Mandatory                   |
| Actions           | DCH-PlanAndRequestedActions-CarePlan-1.description          | Mandatory                   |
| Recipient         | DCH-RelatedPerson-1.relationship                | Optional                    |
| Encounter Type    | CareConnect-DCH-Encounter-1.type (childHealthEncounterType)                 | Mandatory                   |

