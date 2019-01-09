---
title: Personal Contacts Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_personal_contacts.html
summary: "The FHIR profiles used for the Personal Contacts Event Message Bundle"
---

The following FHIR profiles are used to form the Personal Contacts Event Message Bundle:

- [DCH-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-Bundle-1)
- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display elements for the 'event' type are fixed to 'CH023 - Personal Contacts'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [DCH-RelatedPerson-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-RelatedPerson-1)

### Personal Contacts Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item           | FHIR resource element                                          | Mandatory/Required/Optional |
|-------------------------|----------------------------------------------------------------|-----------------------------|
| First Given Name        | DCH-RelatedPerson-1.name.given                                 | Mandatory                   |
| Family Name             | DCH-RelatedPerson-1.name.family                                | Mandatory                   |
| NHS Number              | Connect-DCH-Patient-1.identifier (NHS Number)                  | Required                    |
| Contact Details         | DCH-RelatedPerson-1.address and/or DCH-RelatedPerson-1.telecom | Required                    |
| Relationship Type       | DCH-RelatedPerson-1.relationship                               | Mandatory                   |
| Household member        | DCH-RelatedPerson-1.householdMember - extension                            | Required                    |
| Parental Responsibility | DCH-RelatedPerson-1.parentalResponsibility - extension         | Required                    |
| Significant Individual  | DCH-RelatedPerson-1.significantIndividual - extension          | Required                    |