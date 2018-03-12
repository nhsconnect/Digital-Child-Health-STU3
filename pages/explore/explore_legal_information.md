---
title: Legal Information Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_legal_information.html
summary: "The FHIR profiles used for the Legal Information Event Message Bundle"
---

{% include important.html content="The links below will refer to the StructureDefinition url applied to the FHIR profile, which are not yet active. For queries please refer to the Help and Support section." %}

The following FHIR profiles are used to form the Legal Information Event Message Bundle:

- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display elements for the 'event' type are fixed to 'Legal Information'
- [CareConnect-DCH-Organization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-DCH-Location-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Location-1)
- [DCH-LookedAfterChild-EpisodeOfCare-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-LookedAfterChild-EpisodeOfCare-1)
- [DCH-ChildProtection-CarePlan-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-ChildProtection-CarePlan-1)

### Legal Information event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item                    | FHIR Resource element                             | Mandatory/Required/Optional |
|----------------------------------|---------------------------------------------------|-----------------------------|
| Date                             | CareConnect-DCH-Encounter-1.period.start          | Mandatory                   |
| Looked After Child Start Date    | DCH-LookedAfterChild-EpisodeOfCare-1.period.start | Required                    |
| Looked After Child End Date      | DCH-LookedAfterChild-EpisodeOfCare-1.period.end   | Required                    |
| Local Authority (LAC)            | CareConnect-DCH-Organization-1.name               | Required                    |
| Child Protection Plan Start Date | DCH-ChildProtection-CarePlan-1.period.start       | Required                    |
| Child Protection Plan End Date   | DCH-ChildProtection-CarePlan-1.period.end         | Required                    |
| Local Authority (CPP)            | CareConnect-DCH-Organization-1.name               | Required                    |