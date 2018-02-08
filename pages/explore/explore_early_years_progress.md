---
title: Early Years Progress Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_early_years_progress.html
summary: "The FHIR profiles used for the Early Years Progress Event Message Bundle"
---
{% include custom/under.construction.html content="Please check back later for any updates to this page" %}

{% include important.html content="The links below will refer to the StructureDefinition url applied to the FHIR profile, which are not yet active. For queries please refer to the Help and Support section." %} 

The following FHIR profiles are used to form the Early Years Progress Event Message Bundle:

- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1.xml) - where the coding and display for the event element is fixed to 'Early Years Progress'
- [CareConnect-DCH-Organization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Organization-1.xml)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1.xml)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1.xml)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1.xml)
- [CareConnect-DCH-Location-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Location-1.xml)
- [CareConnect-DCH-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Practitioner-1.xml)
- [CareConnect-DCH-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PractitionerRole-1.xml)
- [CareConnect-DCH-ParentalConsent-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-ParentalConsent-Observation-1)
- [CareConnect-DCH-EarlyYears-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-EarlyYears-Observation-1)

### Early Years Progress event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item                              | FHIR Resource element                                               | Mandatory/Required/Optional |
|--------------------------------------------|---------------------------------------------------------------------|-----------------------------|
| Date                                       | CareConnect-DCH-Encounter-1.period.start                            | Mandatory                   |
| Site Code                                  | CareConnect-DCH-Location-1.identifier                               | Mandatory                   |
| Professional Type                          | CareConnect-DCH-PractitionerRole-1.code (SDS Job Role Name) | Mandatory                   |
| Professional Name                          | CareConnect-DCH-Practitioner.name                                   | Mandatory                   |
| Parental Consent                           | CareConnect-DCH-ParentalConsent-Observation-1.valueCoding                        | Required                    |
| Communication and Language                 | CareConnect-DCH-EarlyYears-Observation-1.valueString                    | Required                    |
| Physical Development                       | CareConnect-DCH-EarlyYears-Observation-1.valueString                    | Required                    |
| Personal, Social and Emotional Development | CareConnect-DCH-EarlyYears-Observation-1.valueString                    | Required                    |
| Any Areas of Concern                       | CareConnect-DCH-EarlyYears-Observation-1.valueString                    | Required                    |
| Type of Support Requested/Provided         | CareConnect-DCH-EarlyYears-Observation-1.valueString                    | Required                    |
| Encounter Type                             | CareConnect-DCH-Encounter-1.type (childHealthEncounterType)  (childHealthEncounterType)         | Mandatory                   |