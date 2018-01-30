---
title: Clinical Risk Factors Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_clinical_risk_factors.html
summary: "The FHIR profiles used for the Clinical Risk Factors Event Message Bundle"
---
{% include custom/under.construction.html content="Please check back later for any updates to this page" %}

{% include important.html content="The links below will refer to the StructureDefinition url applied to the FHIR profile, which are not yet active. For queries please refer to the Help and Support section." %} 

The following FHIR profiles are used to form the Clinical Risk Factors Event Message Bundle:

- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1.xml) - where the coding and display elements for the 'event' type are fixed to 'Clinical Risk Factors'
- [CareConnect-DCH-Organization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Organization-1.xml)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1.xml)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1.xml)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1.xml)
- [CareConnect-DCH-Location-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Location-1.xml)
- [DCH-ClinicalRiskFactor-RiskAssessment-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-RiskAssessment-1.xml)
- [CareConnect-DCH-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Practitioner-1.xml)
- [CareConnect-DCH-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PractitionerRole-1.xml)


### Clinical Risk Factors event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item          | FHIR resource element                                                 | Mandatory/Required/Optional |
|------------------------|-----------------------------------------------------------------------|-----------------------------|
| Date                   | DCH-ClinicalRiskFactor-RiskAssessment-1.occurrenceDateTime                                            | Mandatory                   |
| ODS Site   Code        | CareConnect-DCH-Location-1.identifier (ODS Site Code)                 | Mandatory                   |
| SDS Job   Role Name    | CareConnect-DCH-PractitionerRole-1.code (SDS Job Role Name) | Mandatory                   |
| Professional   Name    | CareConnect-DCH-Practitioner-1.name                                   | Mandatory                   |
| Relevant Clinical Risk Factor | DCH-ClinicalRiskFactor-RiskAssessment-1.prediction.outcome                             | Required                   |
| Clinical Risk Assessment      | DCH-ClinicalRiskFactor-RiskAssessment-1.method                                           | Required                 |
| Risk Mitigation      | DCH-ClinicalRiskFactor-RiskAssessment-1.mitigation                                       | Required                  |