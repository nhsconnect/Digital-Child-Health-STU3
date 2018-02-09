---
title: Measurements Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_measurements.html
summary: "The FHIR profiles used for the Measurements Event Message Bundle"
---

{% include important.html content="The links below will refer to the StructureDefinition url applied to the FHIR profile, which are not yet active. For queries please refer to the Help and Support section." %} 

The following FHIR profiles are used to form the Measurements Event Message Bundle:

- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1.xml) - where the coding and display for the event element is fixed to 'Measurements'
- [CareConnect-DCH-Organization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Organization-1.xml)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1.xml)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1.xml)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1.xml)
- [CareConnect-DCH-Location-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Location-1.xml)
- [CareConnect-DCH-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Practitioner-1.xml)
- [CareConnect-DCH-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PractitionerRole-1.xml) 
- [CareConnect-DCH-Measurement-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Measurement-Observation-1)
- [CareConnect-DCH-NCMP-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-NCMP-Procedure-1)

### Measurement event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below.
                                                                                                   
| DCH Data Item          | FHIR resource element                                               | Mandatory/Required/Optional |
|------------------------|---------------------------------------------------------------------|-----------------------------|
| Date                   | CareConnect-DCH-Encounter-1.period.start                            | Mandatory                   |
| ODS Site Code          | CareConnect-DCH-Location-1.identifier (ODS Site Code)               | Mandatory                   |
| Professional Name      | CareConnect-DCH-Practitioner-1.name                                 | Mandatory                   |
| SDS Job Role Name      | CareConnect-DCH-PractitionerRole-1.code (SDS Job Role Name)         | Mandatory                   |
| Birth Weight           | CareConnect-DCH-Measurement-Observation-1.valueQuantity             | Mandatory                   |
| Head Circumference     | CareConnect-DCH-Measurement-Observation-1.valueQuantity             | Required                    |
| Weight                 | CareConnect-DCH-Measurement-Observation-1.valueQuantity             | Required                    |
| Height/Length          | CareConnect-DCH-Measurement-Observation-1.valueQuantity             | Required                    |
| BMI centile            | CareConnect-DCH-Measurement-Observation-1.valueQuantity             | Required                    |
| Encounter Type         | CareConnect-DCH-Encounter-1.type (childHealthEncounterType)  (childHealthEncounterType)         | Mandatory                   |
| NCMP Withdrawal Reason | CareConnect-DCH-NCMP-Procedure-1.reasonNotPerformed                 | Required                    |