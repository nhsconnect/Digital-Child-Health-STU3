---
title: Observations Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_measurements.html
summary: "The FHIR profiles used for the Observations Event Message Bundle"
---

The following FHIR profiles are used to form the Observations Event Message Bundle:

- [DCH-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-Bundle-1)
- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display for the event element is fixed to 'CH018 - Measurements'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [CareConnect-DCH-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Practitioner-1)
- [CareConnect-DCH-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PractitionerRole-1) 
- [CareConnect-DCH-HeadCircumference-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-HeadCircumference-Observation-1)
- [CareConnect-DCH-Weight-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Weight-Observation-1)
- [CareConnect-DCH-Height-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Height-Observation-1)
- [CareConnect-DCH-Length-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Length-Observation-1)
- [CareConnect-DCH-BMICentile-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-BMICentile-Observation-1)
- [CareConnect-DCH-NCMPWithdrawal-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-NCMPWithdrawal-Observation-1)

### Observations Event data item mapping to FHIR profiles ###

This Mapping table defines the FHIR elements that SHALL be used to encode the Healthy Child Event Specification data items for each DCH Event Message payload.  
Some common data item mappings, such as patient, publisher or Date/Time of event information, are defined within the [Header mapping table](../explore_event_header_design.html) and SHALL be considered in parallel with the payload mapping.

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below.
                                                                                                   
| DCH Data Item            | FHIR resource element                                         | Mandatory/Required/Optional | Note                               |
|--------------------------|---------------------------------------------------------------|-----------------------------|------------------------------------|
| Date                     | CareConnect-DCH-Encounter-1.period.start                      | Mandatory                   |                                    |
| ODS Site Code            | CareConnect-Location-1.identifier (ODS Site Code)             | Mandatory                   |                                    |
| Professional Name        | CareConnect-DCH-Practitioner-1.name                           | Mandatory                   |                                    |
| SDS Job Role Name        | CareConnect-DCH-PractitionerRole-1.code (SDS Job Role Name)   | Mandatory                   |                                    |
| Birth Weight             | CareConnect-DCH-Weight-Observation-1.valueQuantity            | Required                    | Observation.code uses SNOMED CT '364589006 - Birth weight' |
| Birth head circumference | CareConnect-DCH-HeadCircumference-Observation-1.valueQuantity | Required                    | Observation.code uses SNOMED CT '169876006 - Birth head circumference'  |
| Head Circumference       | CareConnect-DCH-HeadCircumference-Observation-1.valueQuantity | Required                    | Observation.code uses SNOMED CT '363812007 - Head circumference'  |
| Weight                   | CareConnect-DCH-Weight-Observation-1.valueQuantity            | Required                    | Observation.code uses SNOMED CT '27113001 - Body weight'  |
| Height                   | CareConnect-DCH-Height-Observation-1.valueQuantity            | Required                    |                                    |
| Length                   | CareConnect-DCH-Length-Observation-1.valueQuantity            | Required                    |                                    |
| BMI centile              | CareConnect-DCH-BMICentile-Observation-1.valueQuantity        | Required                    |                                    |
| Encounter Type           | CareConnect-DCH-Encounter-1.type (childHealthEncounterType)   | Mandatory                   |                                    |
| NCMP Withdrawal Reason   | CareConnect-DCH-NCMPWithdrawal-Observation-1.valueCoding      | Required                    |                                    |                                                                                                                                                    
### Reference Linkage Diagram ###

This Linkage diagram defines the required references that SHALL be made between resources within the DCH Event Message bundle. It includes both Header and Payload resources (but omits the DCH-Bundle-1 wrapper).

<img src="images/explore/BirthDetails1.png">

### Examples ###

<script src="https://gist.github.com/IOPS-DEV/20d86f149c4bf1abae4ec53bbd60b883.js"></script>

<script src="https://gist.github.com/IOPS-DEV/113951f86f8db0eae46433cdfe46481e.js"></script>