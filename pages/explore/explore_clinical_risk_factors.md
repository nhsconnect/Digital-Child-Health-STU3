---
title: Clinical Risk Factors Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_clinical_risk_factors.html
summary: "The FHIR profiles used for the Clinical Risk Factors Event Message Bundle"
---
{% include custom/under.construction.html content="Please check back later for any updates to this page" %}

The following FHIR profiles are used to form the Clinical Risk Factors Event Message Bundle:

- DCH-MessageHeader-1 - where the coding and display elements for the 'event' type are fixed to 'Clinical Risk Factors'
- CareConnect-DCH-Organization-1
- DCH-HealthcareService-1
- CareConnect-DCH-Patient-1
- CareConnect-DCH-Encounter-1
- DCH-ClinicalRiskFactor-RiskAssessment-1
- CareConnect-DCH-Practitioner-1
- CareConnect-DCH-PractitionerRole-1
- CareConnect-DCH-Location-1

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