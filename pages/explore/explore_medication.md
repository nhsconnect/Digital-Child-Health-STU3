---
title: Medication Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_medication.html
summary: "The FHIR profiles used for the Medication Event Message Bundle"
---

{% include important.html content="The links below will refer to the StructureDefinition url applied to the FHIR profile, which are not yet active. For queries please refer to the Help and Support section." %}

The following FHIR profiles are used to form the Medication Event Message Bundle:

- [DCH-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-Bundle-1)
- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display elements for the 'event' type are fixed to 'Medication'
- [CareConnect-DCH-Organization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-DCH-Location-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Location-1)
- [CareConnect-DCH-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Practitioner-1)
- [CareConnect-DCH-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PractitionerRole-1)
- [CareConnect-DCH-Medication-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Medication-1)
- [CareConnect-DCH-Medication-Flag-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Medication-Flag-1)
- [CareConnect-DCH-MedicationRequest-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-MedicationRequest-1)
- [DCH-MedicationAdministration-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MedicationAdministration-1)
- [CareConnect-MedicationStatement-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-MedicationStatement-1)  


### Medication event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item               | FHIR Resource element                                                     | Mandatory/Required/Optional |
|-----------------------------|---------------------------------------------------------------------------|-----------------------------|
| Date                        | DCH-MedicationAdministration-1.effectiveTimeDateTime (if administered) or                     | Mandatory                   |
|                             | CareConnect-DCH-MedicationRequest-1.authoredOn (if prescribed)                     	| Mandatory                   |
| Start Date                  | CareConnect-DCH-MedicationRequest-1.dosageInstruction.timing.repeat.boundsPeriod.start   | Required                    |
| End Date                    | CareConnect-DCH-MedicationRequest-1.dosageInstruction.timing.repeat.boundsPeriod.end     | Required                    |
| ODS Site Code               | CareConnect-DCH-Location.identifier (ODS Site Code)                       | Required                    |
| Professional Name           | CareConnect-DCH-Practitioner-1.name                                       | Required                    |
| SDS Job Role Name           | CareConnect-DCH-PractitionerRole-1.code (SDS Job Role Name)       | Required                    |
| Medication Name             | CareConnect-DCH-Medication-1.code	                                | Mandatory                   |
| Form                        | CareConnect-DCH-Medication-1.form                                 | Required                    |
| Route                       | DCH-MedicationAdministration-1.dosage.route (if administered) or                             | Required                    |
|                             | CareConnect-DCH-MedicationRequest-1.dosageInstruction.route (if prescribed)                               | Required                    |
| Course status               | CareConnect-DCH-MedicationRequest-1.status                                  | Required                    |
| Dose directions description | CareConnect-DCH-MedicationRequest-1.dosageInstruction.text (if prescribed) or             | Required                    |
|                             | DCH-MedicationAdministration-1.dosage.text (if administered)                               | Required                    |
| Dose Direction Duration     | CareConnect-DCH-MedicationRequest-1.dosageInstruction.asNeededCodeableConcept                                    | Required                    |
| Additional instruction      | CareConnect-DCH-MedicationRequest-1.dosageInstruction.additionalInstruction | Required                    |
| Medical devices             | CareConnect-MedicationStatement-1                                                 | Optional                    |
| Indication                  | CareConnect-DCH-MedicationRequest-1.reasonCode                                  | Required                    |          