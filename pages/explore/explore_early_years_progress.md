---
title: Early Years Progress Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_early_years_progress.html
summary: "The FHIR profiles used for the Early Years Progress Event Message Bundle"
---

The following FHIR profiles are used to form the Early Years Progress Event Message Bundle:

- [DCH-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-Bundle-1)
- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display for the event element is fixed to 'CH010 - Early Years Progress'
- [CareConnect-DCH-Organization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-DCH-Location-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Location-1)
- [CareConnect-DCH-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Practitioner-1)
- [CareConnect-DCH-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PractitionerRole-1)
- [DCH-EarlyYearsProgress-QuestionnaireResponse-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-EarlyYearsProgress-QuestionnaireResponse-1)

### Early Years Progress Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item                              | FHIR Resource element                                               | Mandatory/Required/Optional |
|--------------------------------------------|---------------------------------------------------------------------|-----------------------------|
| Date                                       | CareConnect-DCH-Encounter-1.period.start                            | Mandatory                   |
| Site Code                                  | CareConnect-DCH-Location-1.identifier                               | Mandatory                   |
| Professional Type                          | CareConnect-DCH-PractitionerRole-1.code (SDS Job Role Name) | Mandatory                   |
| Professional Name                          | CareConnect-DCH-Practitioner.name                                   | Mandatory                   |
| Parental Consent                           | DCH-EarlyYearsProgress-QuestionnaireResponse-1.parentalConsent                        | Required                    |
| Communication and Language                 | DCH-EarlyYearsProgress-QuestionnaireResponse-1.communicationAndLanguage                    | Required                    |
| Physical Development                       | DCH-EarlyYearsProgress-QuestionnaireResponse-1.physicalDevelopment                    | Required                    |
| Personal, Social and Emotional Development | DCH-EarlyYearsProgress-QuestionnaireResponse-1.personalSocialEmotionalDevelopment                    | Required                    |
| Any Areas of Concern                       | DCH-EarlyYearsProgress-QuestionnaireResponse-1.areasOfConcern                    | Required                    |
| Type of Support Requested/Provided         | DCH-EarlyYearsProgress-QuestionnaireResponse-1.supportedRequestedOrProvided                    | Required                    |
| Encounter Type                             | CareConnect-DCH-Encounter-1.type (childHealthEncounterType)           | Mandatory                   |