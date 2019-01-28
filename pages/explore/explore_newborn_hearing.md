---
title: Newborn Hearing Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_newborn_hearing.html
summary: "The FHIR profiles used for the Newborn Hearing Event Message Bundle"
---

- [DCH-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-Bundle-1)
- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display for the event element is fixed to 'CH021 - Newborn Hearing'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [CareConnect-DCH-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Practitioner-1)
- [CareConnect-DCH-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PractitionerRole-1) 
- [CareConnect-DCH-AABRHearingTest-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-AABRHearingTest-Procedure-1)
- [CareConnect-DCH-AOAEHearingTest-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-AOAEHearingTest-Procedure-1)
- [CareConnect-DCH-HearingScreeningSummaryOutcome-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-HearingScreeningSummaryOutcome-Observation-1)
- [DCH-ProfessionalComment-Communication-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-ProfessionalComment-Communication-1) 

### Newborn Hearing Event data item mapping to FHIR profiles ###

This Mapping table defines the FHIR elements that SHALL be used to encode the Healthy Child Event Specification data items for each DCH Event Message payload.  
Some common data item mappings, such as patient, publisher or Date/Time of event information, are defined within the [Header mapping table](./explore_event_header_design.html) and SHALL be considered in parallel with the payload mapping.

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:
                                                                     
| DCH Data Item       | FHIR resource element                                       | Mandatory/Required/Optional | Note                                                                  |
|---------------------|-------------------------------------------------------------|-----------------------------|-----------------------------------------------------------------------|
| Date                | CareConnect-DCH-Encounter-1.period.start                    | Mandatory                   |                                                                       |
| ODS Site Code       | CareConnect-Location-1.identifier                           | Required                    |                                                                       |
| Professional Name   | CareConnect-DCH-Practitioner-1.name                         | Required                    |                                                                       |
| SDS Job Role Name   | CareConnect-DCH-PractitionerRole-1.code.text                | Required                    | This SHALL be submitted as part of an HL7 nullFlavor slice in PractitionerRole.code  
(see examples for detail). |
| Hearing Test Results (AABR) | CareConnect-DCH-AABRHearingTest-Procedure-1.outcome | Required         | two occurrences of this resource are required, one for each ear |
| Hearing Test Result (AOAE) | CareConnect-DCH-AOAEHearingTest-Procedure-1.outcome  |Required          | up to four occurrences of this resource are required, with two for each test performed |
| Summary Outcome     | CareConnect-DCH-HearingScreeningSummaryOutcome-Observation-1.valueCodeableConcept        | Mandatory                   |                                                                       |
| Comment                | DCH-ProfessionalComment-Communication-1                  | Optional                    |                                                                                        |

### Reference Linkage Diagram ###

This Linkage diagram defines the required references that SHALL be made between resources within the DCH Event Message bundle. It includes both Header and Payload resources (but omits the DCH-Bundle-1 wrapper).

<img src="images/explore/NewbornHearing1.png">

Allowed Child Health Observations are: 

<img src="images/explore/NewbornHearing2.png">

### Examples ###

<script src="https://gist.github.com/IOPS-DEV/b8f0d3a8da033037ad0dfbd60a662d93.js"></script>

<script src="https://gist.github.com/IOPS-DEV/d50001b1a618a5ae1f89394cfeaa7ae8.js"></script>
