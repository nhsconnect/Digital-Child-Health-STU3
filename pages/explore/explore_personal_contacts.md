---
title: Personal Contacts Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_personal_contacts.html
summary: "The FHIR profiles used for the Personal Contacts Event Message Bundle"
---
{% include custom/under.construction.html content="Please check back later for any updates to this page" %}

{% include important.html content="The links below will refer to the StructureDefinition url applied to the FHIR profile, which are not yet active. For queries please refer to the Help and Support section." %} 

The following FHIR profiles are used to form the Personal Contacts Event Message Bundle:

- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1.xml) - where the coding and display elements for the 'event' type are fixed to 'Personal Contacts'
- [CareConnect-DCH-Organization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Organization-1.xml)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1.xml)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1.xml)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1.xml)
- [CareConnect-DCH-Location-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Location-1.xml)
- [DCH-RelatedPerson-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-RelatedPerson-1.xml)

### Personal Contacts event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item           | FHIR resource element                                          | Mandatory/Required/Optional |
|-------------------------|----------------------------------------------------------------|-----------------------------|
| First Given Name        | DCH-RelatedPerson-1.name.given                                 | Mandatory                   |
| Family Name             | DCH-RelatedPerson-1.name.family                                | Mandatory                   |
| NHS Number              | Connect-DCH-Patient-1.identifier (NHS Number)                  | Required                    |
| Contact Details         | DCH-RelatedPerson-1.address and/or DCH-RelatedPerson-1.telecom | Required                    |
| Relationship Type       | DCH-RelatedPerson-1.relationship                               | Mandatory                   |
| Household member        | DCH-RelatedPerson-1.householdMember                            | Required                    |
| Parental Responsibility | DCH-RelatedPerson-1.parentalResponsibility - extension         | Required                    |
| Significant Individual  | DCH-RelatedPerson-1.significantIndividual - extension          | Required                    |