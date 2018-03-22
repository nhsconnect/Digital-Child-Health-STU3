---
title: Conditions / Diagnoses Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_conditions_diagnoses.html
summary: "The FHIR profiles used for the Conditions / Diagnoses Event Message Bundle"
---

{% include important.html content="The links below will refer to the StructureDefinition url applied to the FHIR profile, which are not yet active. For queries please refer to the Help and Support section." %} 

The following FHIR profiles are used to form the Conditions / Diagnoses Event Message Bundle:

- [DCH-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-Bundle-1)
- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display elements for the 'event' type are fixed to 'CH008 - Conditions or Diagnoses'
- [CareConnect-DCH-Organization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-DCH-Location-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Location-1)
- [CareConnect-DCH-Diagnosis-Condition-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Diagnosis-Condition-1)
- [CareConnect-DCH-Problem-Condition-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Problem-Condition-1)
- [CareConnect-DCH-FetalDiagnosis-Condition-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-FetalDiagnosis-Condition-1)

### Conditions or Diagnoses Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item        | FHIR resource element                                    | Mandatory/Required/Optional | Note                    |
|----------------------|----------------------------------------------------------|-----------------------------|-------------------------|
| Condition            | CareConnect-DCH-Diagnosis-Condition-1.code               | Mandatory                   |                         |
|                      | CareConnect-DCH-Problem-Condition-1.code                 | Mandatory                   |                         |
| Condition category   | CareConnect-DCH-Diagnosis-Condition-1.category           | Mandatory                   | fixed value 'diagnosis' |
|                      | CareConnect-DCH-Problem-Condition-1.category             | Mandatory                   | fixed value 'problem'   |
| Stage of Disease     | CareConnect-DCH-Condition-1.stage.summary.coding.text    | Optional                    |                         |
| Condition onset Date | CareConnect-DCH-Condition-1.onsetDateTime or onsetString | Required                    |                         |
| Fetal Diagnosis      | CareConnect-DCH-FetalDiagnosis-Condition-1               | Optional                    |                         |
