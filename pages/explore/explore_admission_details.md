---
title: Admission Details Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_admission_details.html
summary: "The FHIR profiles used for the Admission Details Event Message Bundle"
---

{% include important.html content="The links below will refer to the StructureDefinition url applied to the FHIR profile, which are not yet active. For queries please refer to the Help and Support section." %} 

The following FHIR profiles are used to form the Admission Details Event Message Bundle:

- [DCH-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-Bundle-1)
- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display for the event element is fixed to 'CH002 - Admission Details'
- [CareConnect-DCH-Organization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-DCH-Location-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Location-1)
- [CareConnect-DCH-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Practitioner-1)
- [CareConnect-DCH-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PractitionerRole-1)
- [DCH-RelatedPerson-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-RelatedPerson-1) 


### Admission Details Event data item mapping to FHIR profiles ###
----------
The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item               | FHIR resource element                                   | Mandatory/Required/Optional |
|-----------------------------|---------------------------------------------------------|-----------------------------|
| Date                        | CareConnect-DCH-Encounter-1.period.start                | Mandatory                   |
| ODS Site Code               | CareConnect-DCH-Location-1.identifier (ODS Site Code)   | Mandatory                   |
| Name of Location            | CareConnect-DCH-Location-1.name   | Required                   |
| Responsible Consultant      | CareConnect-DCH-Practitioner-1                          | Required                    |
| Name of Location            | CareConnect-DCH-Location-1    | Required                   |
| Reason for Admission        | CareConnect-DCH-Encounter-1.reason.text                      | Required                    |
| Admission Method            | CareConnect-DCH-Encounter-1.hospitalization.admissionMethod | Required                    |
| Speciality                  | DCH-HealthcareService-1.serviceType.specialty or          | Required                    |
|      						  | CareConnect-DCH-PractitionerRole-1.specialty         | Required                    |
| Source of Admission         | CareConnect-DCH-Encounter-1.hospitalization.admitSource        | Required                    |
| Person accompanying patient | DCH-RelatedPerson-1                                     | Required                    |



