---
title: Parent, Guardian or Personal Comment Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_parent_guardian_or_personal_comment.html
summary: "The FHIR profiles used for the Parent, Guardian or Personal Comment Event Message Bundle"
---

{% include important.html content="The links below will refer to the StructureDefinition url applied to the FHIR profile, which are not yet active. For queries please refer to the Help and Support section." %} 

The following FHIR profiles are used to form the Parent, Guardian or Personal Comment Event Message Bundle:

- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1.xml) - where the coding and display elements for the 'event' type are fixed to  'Parent Guardian Or Personal Comment'
- [CareConnect-DCH-Organization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Organization-1.xml)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1.xml)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1.xml)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1.xml)
- [CareConnect-DCH-Location-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Location-1.xml)
- [DCH-ParentGuardianOrPersonalComment-Communication-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-ParentGuardianOrPersonalComment-Communication-1.xml)
- [DCH-RelatedPerson-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-RelatedPerson-1.xml)
- [CareConnect-DCH-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Practitioner-1.xml)


### Parent, Guardian or Personal Comment event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item       | FHIR resource element                     | Mandatory/Required/Optional |
|---------------------|-------------------------------------------|-----------------------------|
| Date                | CareConnect-DCH-Encounter-1.period.start  | Required                    |
| Name                | CareConnect-DCH-Practitioner.name         | Required                    |
| Details             | DCH-ParentOrGuardianComment-Communication-1.payload.contentString | Required                    |
| Relationship Status | DCH-RelatedPerson-1.relationship          | Optional                    |



