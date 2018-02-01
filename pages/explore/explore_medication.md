---
title: Medication Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_medication.html
summary: "The FHIR profiles used for the Medication Event Message Bundle"
---
{% include custom/under.construction.html content="Please check back later for any updates to this page" %}

{% include important.html content="The links below will refer to the StructureDefinition url applied to the FHIR profile, which are not yet active. For queries please refer to the Help and Support section." %}

The following FHIR profiles are used to form the Medication Event Message Bundle:

- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1.xml) - where the coding and display elements for the 'event' type are fixed to 'Medication'
- [CareConnect-DCH-Organization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Organization-1.xml)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1.xml)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1.xml)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1.xml)
- [CareConnect-DCH-Location-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Location-1.xml)
- [CareConnect-DCH-Medication-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Medication-1)
- [CareConnect-DCH-Medication-Flag-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Medication-Flag-1)
- [CareConnect-DCH-MedicationRequest-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-MedicationRequest-1)
- [DCH-MedicationAdministration-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MedicationAdministration-1)
- [CareConnect-MedicationStatement-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-MedicationStatement-1)  


### Medication event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item               | FHIR Resource element                                                     | Mandatory/Required/Optional |
|-----------------------------|---------------------------------------------------------------------------|-----------------------------|
| Date                        | DCH-MedicationAdministration-1.effectiveTimeDateTime                      | Mandatory                   |
| Start Date                  | CareConnect-DCH-MedicationRequest-1.dosageInstruction.timing.repeat.boundsPeriod   | Required                    |
| End Date                    | CareConnect-DCH-MedicationRequest-1.dosageInstruction.timing.repeat.boundsPeriod     | Required                    |
| ODS Site Code               | CareConnect-DCH-Location.identifier (ODS Site Code)                       | Required                    |
| Professional Name           | CareConnect-DCH-Practitioner-1.name                                       | Required                    |
| SDS Job Role Name           | CareConnect-DCH-PractitionerRole-1.code (SDS Job Role Name)       | Required                    |
| Medication Name             | CareConnect-DCH-Medication-1.code	                                | Mandatory                   |
| Form                        | CareConnect-DCH-Medication-1.form                                 | Required                    |
| Route                       | DCH-MedicationAdministration-1.dosage.route                               | Required                    |
| Course status               | CareConnect-DCH-MedicationRequest-1.status                                  | Required                    |
| Dose directions description | CareConnect-DCH-MedicationRequest-1.dosageInstruction.text or               | Required                    |
|                             | DCH-MedicationAdministration-1.dosage.text                                | Required                    |
| Dose Direction Duration     | CareConnect-DCH-Medication-Flag-1.code                                    | Required                    |
| Additional instruction      | CareConnect-DCH-MedicationRequest-1.dosageInstruction.additionalInstruction | Required                    |
| Medical devices             | CareConnect-MedicationStatement-1                                                 | Optional                    |
| Indication                  | CareConnect-DCH-MedicationRequest-1.reasonCode                                  | Required                    |          