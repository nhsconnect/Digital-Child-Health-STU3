---
title: Immunisation Administration Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_immunisation_administration.html
summary: "The FHIR profiles used for the Immunisation Administration Event Message Bundle"
---
{% include custom/under.construction.html content="Please check back later for any updates to this page" %}

{% include important.html content="The links below will refer to the StructureDefinition url applied to the FHIR profile, which are not yet active. For queries please refer to the Help and Support section." %} 

The following FHIR profiles are used to form the Immunisation Administration Event Message Bundle:

- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1.xml) - where the coding and display for the event element is fixed to 'Immunisation Administration'
- [CareConnect-DCH-Organization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Organization-1.xml)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1.xml)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1.xml)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1.xml)
- [CareConnect-DCH-Location-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Location-1.xml)
- [CareConnect-DCH-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Practitioner-1.xml)
- [CareConnect-DCH-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PractitionerRole-1.xml)
- [CareConnect-DCH-Immunization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Immunization-1)


### Immunisation Administration event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item               | FHIR resource element                                               | Mandatory/Required/Optional |
|-----------------------------|---------------------------------------------------------------------|-----------------------------|
| Date                        | CareConnect-DCH-Immunisation-1.date                                 | Mandatory                   |
| ODS Site code               | CareConnect-DCH-Location-1.identifier (ODS Site Code)               | Mandatory                   |
| Professional Name           | CareConnect-DCH-Practitioner-1.name                                 | Mandatory                   |
| SDS Job Role Name           | CareConnect-DCH-PractitionerRole-1.code (SDS Job Role Name)         | Mandatory                   |
| Name of Immunisation        | CareConnect-DCH-Immunization-1.vaccineCode                          | Mandatory                   |
| Dose sequence               | CareConnect-DCH-Immunization-1.vaccinationProtocol.doseSequence     | Required                    |
| Outcome Status              | CareConnect-DCH-Immunization-1.explanation                          | Mandatory                   |
| Vaccine Product (DM+D code) | CareConnect-DCH-Immunization-1.vaccineCode                          | Required                    |
| Vaccine Manufacturer        | CareConnect-DCH-Immunization-1.manufacturer                         | Required                    |
| Batch Number                | CareConnect-DCH-Immunization-1.lotNumber                            | Required                    |
| Site                        | CareConnect-DCH-Immunization-1.site                                 | Required                    |
| Route                       | CareConnect-DCH-Immunization-1.route                                | Required                    |
| Dose Amount                 | CareConnect-DCH-Immunization-1.doseQuantity                         | Optional                    |
| Reported                    | CareConnect-DCH-Immunization-1.primarySource                        | Required                    |