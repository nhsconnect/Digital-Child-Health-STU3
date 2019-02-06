---
title: Clinical Risk Factors Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_clinical_risk_factors.html
summary: "The FHIR profiles used for the Clinical Risk Factors Event Message Bundle"
---

The following FHIR profiles are used to form the Clinical Risk Factors Event Message Bundle:

- [DCH-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-Bundle-1)
- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display elements for the 'event' type are fixed to 'CH007 - Clinical Risk Factors'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [CareConnect-DCH-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Practitioner-1)
- [CareConnect-DCH-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PractitionerRole-1)
- [DCH-ClinicalRiskFactor-RiskAssessment-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-ClinicalRiskFactor-RiskAssessment-1)

### Clinical Risk Factors Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item          | FHIR resource element                                                 | Mandatory/<br/>/Required<br/>/Optional | Note                    |
|------------------------|-----------------------------------------------------------------------|----------------------------------------|-------------------------|
| Date/Time              | DCH-ClinicalRiskFactor-RiskAssessment-1.occurrenceDateTime            | Mandatory                              |                         |
| ODS/ORD Site Code      | CareConnect-Location-1.identifier (ODS Site Code)                     | Required                               |                         |
| SDS Job Role Name      | CareConnect-DCH-PractitionerRole-1.code (SDS Job Role Name)           | Required                               |                         |
| Performing Professional   | CareConnect-DCH-Practitioner-1.name                                | Required                               |                         |
| Relevant Clinical Risk Factor | DCH-ClinicalRiskFactor-RiskAssessment-1.prediction.outcome     | Required                               | The free text field should be used if no coded text available, using code.text |
| Clinical Risk Assessment      | DCH-ClinicalRiskFactor-RiskAssessment-1.method                 | Required                               | The free text field for Clinical Risk Assessment should be entered using method.code.text |
| Risk Mitigation      | DCH-ClinicalRiskFactor-RiskAssessment-1.mitigation                      | Required                               |                         |