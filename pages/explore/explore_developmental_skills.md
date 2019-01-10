---
title: Developmental Skills Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_developmental_skills.html
summary: "The FHIR profiles used for the Developmental Skills Event Message Bundle"
---

The following FHIR profiles are used to form the Developmental Skills Event Message Bundle:

- [DCH-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-Bundle-1)
- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display for the event element is fixed to 'CH020 - Developmental Skills'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [CareConnect-DCH-DevelopmentalSkill-Condition-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-DevelopmentalSkill-Condition-1)

### Developmental Skills Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item     | FHIR resource element                                       | Mandatory/Required/Optional |
|-------------------|-------------------------------------------------------------|-----------------------------|
| Date first achieved     | CareConnect-DCH-DevelopmentalSkill-Condition-1.onsetDateTime                 | Required                    |
| Date of observation     | CareConnect-DCH-DevelopmentalSkill-Condition-1.assertedDate          | Required                    |
| Date of enquiry             | CareConnect-DCH-Encounter-1.period.start                    | Required                   |
| Developmental Skill    | CareConnect-DCH-DevelopmentalSkill-Condition-1.code                  | Mandatory                   |
| Result of observation/enquiry  | CareConnect-DCH-DevelopmentalSkill-Condition-1.stage.summary         | Mandatory                   |
| Comments    | CareConnect-DCH-DevelopmentalSkill-Condition-1.note    | Optional                   |

### Linkage Diagram ###

<img src="images/explore/DevelopmentSkills.png">

### Development Skills XML Example ###

<script src="https://gist.github.com/IOPS-DEV/14ae03d15ae23d0721a63f13a5ae816f.js"></script>

### Development Skills JSON Example ###

<script src="https://gist.github.com/IOPS-DEV/647f1d989d1a30cbf2b87cb82e897663.js"></script>