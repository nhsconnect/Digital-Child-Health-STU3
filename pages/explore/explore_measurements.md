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

- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display for the event element is fixed to 'Measurements'
- [CareConnect-DCH-Organization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-DCH-Location-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Location-1)
- [CareConnect-DCH-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Practitioner-1)
- [CareConnect-DCH-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PractitionerRole-1) 
- [CareConnect-DCH-Measurement-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Measurement-Observation-1)
- [CareConnect-DCH-NCMPWithdrawal-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-NCMPWithdrawal-Observation-1)

### Measurement event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below.
                                                                                                   
| DCH Data Item            | FHIR resource element                                        | Mandatory/Required/Optional | Note                                                                                                                                                     |
|--------------------------|--------------------------------------------------------------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Date                     | CareConnect-DCH-Encounter-1.period.start                     | Mandatory                   |                                                                                                                                                          |
| ODS Site Code            | CareConnect-DCH-Location-1.identifier (ODS Site Code)        | Mandatory                   |                                                                                                                                                          |
| Professional Name        | CareConnect-DCH-Practitioner-1.name                          | Mandatory                   |                                                                                                                                                          |
| SDS Job Role Name        | CareConnect-DCH-PractitionerRole-1.code (SDS Job Role Name)  | Mandatory                   |                                                                                                                                                          |
| Birth Weight             | CareConnect-DCH-Measurement-Observation-1.valueQuantity      | Mandatory                   | SNOMED CT representation: 364589006 with preferred term 'Birth weight'                                                                                   |
| Birth head circumference | CareConnect-DCH-Measurement-Observation-1.valueQuantity      | Required                    | SNOMED CT representation: 169876006 with preferred term 'Birth head circumference'                                                                       |
| Head Circumference       | CareConnect-DCH-Measurement-Observation-1.valueQuantity      | Required                    | SNOMED CT representation: 363812007 with preferred term 'Head circumference'                                                                             |
| Weight                   | CareConnect-DCH-Measurement-Observation-1.valueQuantity      | Required                    | SNOMED CT representation: 27113001 with preferred term 'Body weight'                                                                                     |
| Height/Length            | CareConnect-DCH-Measurement-Observation-1.valueQuantity      | Required                    | SNOMED CT representation: 50373000 with preferred term 'Body height measure' OR SNOMED CT representation: 248334005 with preferred term 'Length of body' |
| BMI centile              | CareConnect-DCH-Measurement-Observation-1.valueQuantity      | Required                    | SNOMED CT representation: 896691000000102 with preferred term 'Child body mass index centile'                                                            |
| Encounter Type           | CareConnect-DCH-Encounter-1.type (childHealthEncounterType)  | Mandatory                   |                                                                                                                                                          |
| NCMP Withdrawal Reason   | CareConnect-DCH-NCMPWithdrawal-Observation-1.valueCoding     | Required                    |                                                                                                                                                          |