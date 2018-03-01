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

- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1.xml) - where the coding and display elements for the 'event' type are fixed to 'Conditions or Diagnoses'
- [CareConnect-DCH-Organization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Organization-1.xml)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1.xml)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1.xml)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1.xml)
- [CareConnect-DCH-Location-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Location-1.xml)
- [CareConnect-DCH-Condition-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Condition-1.xml)
- [CareConnect-DCH-FetalDiagnosis-Condition-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-FetalDiagnosis-Condition-1.xml)

### Conditions or Diagnoses event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item        | FHIR resource element                     | Mandatory/Required/Optional |
|----------------------|-------------------------------------------|-----------------------------|
| Condition            | CareConnect-DCH-Condition-1.code          | Mandatory                   |
| Condition category   | CareConnect-DCH-Condition-1.category      | Mandatory                   |
| Stage of Disease     | CareConnect-DCH-Condition-1.stage.summary.coding.text         | Optional                    |
| Condition onset Date | CareConnect-DCH-Condition-1.onsetDateTime or onsetString | Required                    |
| Fetal Diagnosis      | CareConnect-DCH-FetalDiagnosis-Condition-1 | Optional                    |
