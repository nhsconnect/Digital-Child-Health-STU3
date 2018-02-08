---
title: Examination Findings Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_examination_findings.html
summary: "The FHIR profiles used for the Examination Findings Event Message Bundle"
---
{% include custom/under.construction.html content="Please check back later for any updates to this page" %}

{% include important.html content="The links below will refer to the StructureDefinition url applied to the FHIR profile, which are not yet active. For queries please refer to the Help and Support section." %} 

The following FHIR profiles are used to form the Examination Findings Event Message Bundle:

- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1.xml) - where the coding and display for the event element is fixed to 'Examination Findings'
- [CareConnect-DCH-Organization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Organization-1.xml)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1.xml)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1.xml)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1.xml)
- [CareConnect-DCH-Location-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Location-1.xml)
- [CareConnect-DCH-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Practitioner-1.xml)
- [CareConnect-DCH-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PractitionerRole-1.xml)
- [CareConnect-DCH-ExaminationFinding-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-ExaminationFinding-Procedure-1)

### Examination Findings event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item                                    | FHIR resource element                                                                             | Mandatory/Required/Optional |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|-----------------------------|
| Date                                             | CareConnect-DCH-Encounter-1.period.start                                                          | Mandatory                   |
| ODS Site Code                                    | CareConnect-DCH-Organisation-1.identifier via CareConnect-DCH-Practitioner-1.managingOrganization | Mandatory                   |
| Professional Name                                | CareConnect-DCH-Practitioner-1.name                                                               | Mandatory                   |
| SDS Job Role Name                                | CareConnect-DCH-PractitionerRole-1.code (SDS Job Role Name)                               | Mandatory                   |
| General Appearance                               | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| General Appearance - Colour                      | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Vital signs                                      | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Mental state                                     | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Head and neck                                    | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Head and Neck - Head and Skull                   | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Head and Neck - Face                             | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Head and Neck - Ears                             | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Head and Neck - Neck and Clavicles               | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Oral examination                                 | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Oral examination - Mouth and Palate              | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Cardiovascular system                            | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Cardiovascular system - Chest                    | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Respiratory system                               | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Respiratory system - Respiratory Abdomen         | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Abdomen                                          | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Abdomen - Abdomen                                | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Umbilicus                                        | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Genitourinary                                    | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Genitourinary - Genitalia                        | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Genitourinary - Anus                             | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Nervous system                                   | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Nervous system - Reflexes                        | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Musculoskeletal                                  | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Musculoskeletal - Manipulation                   | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Musculoskeletal - Upper Limbs                    | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Musculoskeletal - Lower Limbs, feet              | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Musculoskeletal - Back and Spine                 | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Skin                                             | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Skin - Physical Examination                      | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Developmental Assessment                         | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Developmental Assessment - Hearing               | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Developmental Assessment - Locomotion            | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Developmental Assessment - Speech/Language       | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Developmental Assessment - Behaviour             | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Developmental Assessment - Posture and Behaviour | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Examination                                      | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Examination - Vision                             | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Examination Bowels                               | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Examination Urine                                | CareConnect-DCH-ExaminationFinding-Procedure-1.outcome                                            | Required                    |
| Encounter Type                                   | CareConnect-DCH-Encounter-1.type (childHealthEncounterType)                                                                   | Required                    |