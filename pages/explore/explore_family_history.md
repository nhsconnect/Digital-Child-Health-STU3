---
title: Family History Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_family_history.html
summary: "The FHIR profiles used for the Family History Event Message Bundle"
---

The following FHIR profiles are used to form the Family History Event Message Bundle:

- [DCH-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-Bundle-1)
- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display for the event element is fixed to 'CH013 - Family History'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [CareConnect-DCH-FamilyMemberHistory-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-FamilyMemberHistory-1)
- [CareConnect-DCH-MaternalProblemsInPregnancy-FamilyMemberHistory-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-MaternalProblemsInPregnancy-FamilyMemberHistory-1)

### Family History Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item                  | FHIR resource element                                                            | Mandatory/Required/Optional |
|--------------------------------|----------------------------------------------------------------------------------|-----------------------------|
| Date                           | CareConnect-DCH-Encounter-1.period.start                                         | Mandatory                   |
| ODS Site Code                  | CareConnect-Location-1.identifier (ODS Site Code)                            | Mandatory                   |
| Family History                 | CareConnect-DCH-FamilyMemberHistory-1.condition.code                             | Mandatory                   |
| Person in the Family           | CareConnect-DCH-FamilyMemberHistory-1.relationship                               | Mandatory                   |
| Maternal Problems in Pregnancy | CareConnect-DCH-MaternalProblemsInPregnancy-FamilyMemberHistory-1.condition.code | Required                    |