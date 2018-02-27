---
title: Developmental Skills Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_developmental_skills.html
summary: "The FHIR profiles used for the Developmental Skills Event Message Bundle"
---

{% include important.html content="The links below will refer to the StructureDefinition url applied to the FHIR profile, which are not yet active. For queries please refer to the Help and Support section." %} 

The following FHIR profiles are used to form the Developmental Skills Event Message Bundle:

- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1.xml) - where the coding and display for the event element is fixed to 'Developmental Skills'
- [CareConnect-DCH-Organization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Organization-1.xml)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1.xml)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1.xml)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1.xml)
- [CareConnect-DCH-Location-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Location-1.xml)
- [CareConnect-DCH-DevelopmentalSkill-Condition-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-DevelopmentalSkill-Condition-1)

### Developmental Skills event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item     | FHIR resource element                                       | Mandatory/Required/Optional |
|-------------------|-------------------------------------------------------------|-----------------------------|
| Date first achieved     | CareConnect-DCH-DevelopmentalSkill-Condition-1.onsetDateTime                 | Required                    |
| Date of observation     | CareConnect-DCH-DevelopmentalSkill-Condition-1.assertedDate          | Required                    |
| Date of enquiry             | CareConnect-DCH-Encounter-1.period.start                    | Required                   |
| Developmental Skill    | CareConnect-DCH-DevelopmentalSkill-Condition-1.code                  | Mandatory                   |
| Result of observation/enquiry  | CareConnect-DCH-DevelopmentalSkill-Condition-1.stage.summary         | Mandatory                   |
| Encounter Type    | CareConnect-DCH-Encounter-1.type (childHealthEncounterType)    | Mandatory                   |