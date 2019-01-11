---
title: Vaccination Administration Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_vaccination_administration.html
summary: "The FHIR profiles used for the Vaccination Administration Event Message Bundle"
---

The following FHIR profiles are used to form the Vaccination Administration Event Message Bundle:

- [DCH-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-Bundle-1)
- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display for the event element is fixed to 'CH015 - Immunisation Administration'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [CareConnect-DCH-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Practitioner-1)
- [CareConnect-DCH-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PractitionerRole-1)
- [CareConnect-DCH-Immunization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Immunization-1)
- [CareConnect-DCH-Composition-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Composition-1)
- [CareConnect-DCH-AllergyIntolerance-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-AllergyIntolerance-1)

### Vaccination Administration Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item               | FHIR resource element                                               | Mandatory/Required/Optional | Note                    |
|-----------------------------|---------------------------------------------------------------------|-----------------------------|
| Date/Time                   | CareConnect-DCH-Immunisation-1.date                                 | Mandatory                   | Format is YYYY-MM-DD”T”HH:MM:SS                        |
| ODS/ORD Site code           | CareConnect-Location-1.identifier (ODS Site Code)                   | Required                    |                         |
| Performing Professional     | CareConnect-DCH-Practitioner-1.name                                 | Required                    |                         |
| SDS Job Role Name           | CareConnect-DCH-PractitionerRole-1.code (SDS Job Role Name)         | Required                    |                         |
| Reported Date            	  | CareConnect-DCH-Immunization-1.date                                 | Required                    |                         |
| Primary Source              | CareConnect-DCH-Immunization-1.primarySource                        | Mandatory                   | Boolean (FALSE (if reported)/True                        |
| Report Origin               | CareConnect-DCH-Immunization-1.reportOrigin                         | Required                    |                         |

| Name of Immunisation        | CareConnect-DCH-Immunization-1.vaccinationProcedure                 | Mandatory                   |                         |
| Dose sequence               | CareConnect-DCH-Immunization-1.vaccinationProtocol.doseSequence     | Optional                    |                         |
| Outcome Status              | CareConnect-DCH-Immunization-1.explanation                          | Optional                    |                         |
| Vaccine Product             | CareConnect-DCH-Immunization-1.vaccineCode                          | Required                    |                         |
| Vaccine Manufacturer        | CareConnect-DCH-Immunization-1.manufacturer                         | Required                    |                         |
| Batch Number                | CareConnect-DCH-Immunization-1.lotNumber                            | Required                    |                         |
| Site                        | CareConnect-DCH-Immunization-1.site                                 | Required                    |                         |
| Route                       | CareConnect-DCH-Immunization-1.route                                | Required                    |                         |
| Dose Amount                 | CareConnect-DCH-Immunization-1.doseQuantity                         | Optional                    |                         |
| Reported                    | CareConnect-DCH-Immunization-1.primarySource                        | Required                    |                         |
| Information and Advice Given                    | CareConnect-DCH-Composition-1                   | Required                    |                         |
| Allergies and Adverse Reactions                    | CareConnect-DCH-AllergyIntolerance-1         | Required                    |                         |