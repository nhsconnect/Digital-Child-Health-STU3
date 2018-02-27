---
title: Family History Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_family_history.html
summary: "The FHIR profiles used for the Family History Event Message Bundle"
---

{% include important.html content="The links below will refer to the StructureDefinition url applied to the FHIR profile, which are not yet active. For queries please refer to the Help and Support section." %} 

The following FHIR profiles are used to form the Family History Event Message Bundle:

- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1.xml) - where the coding and display for the event element is fixed to 'Family History'
- [CareConnect-DCH-Organization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Organization-1.xml)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1.xml)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1.xml)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1.xml)
- [CareConnect-DCH-Location-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Location-1.xml)
- [CareConnect-DCH-FamilyMemberHistory-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-FamilyMemberHistory-1)
- [CareConnect-DCH-MaternalProblemsInPregnancy-FamilyMemberHistory-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-MaternalProblemsInPregnancy-FamilyMemberHistory-1)

### Family History event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item        | FHIR resource element                                 | Mandatory/Required/Optional |
|----------------------|-------------------------------------------------------|-----------------------------|
| Date                 | CareConnect-DCH-Encounter-1.period.start              | Mandatory                   |
| ODS Site Code        | CareConnect-DCH-Location-1.identifier (ODS Site Code) | Mandatory                   |
| Family History       | CareConnect-DCH-FamilyMemberHistory-1.condition       | Mandatory                   |
| Person in the Family | CareConnect-DCH-FamilyMemberHistory-1.relationship    | Mandatory                   |
| Maternal or paternal relation       | CareConnect-DCH-FamilyMemberHistory-1.relationship       | Required                   |
| Maternal Problems in Pregnancy | CareConnect-DCH-MaternalProblemsInPregnancy-FamilyMemberHistory-1.code    | Required                   |