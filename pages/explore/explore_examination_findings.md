---
title: Examination Findings Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_examination_findings.html
summary: "The FHIR profiles used for the Examination Findings Event Message Bundle"
---

The following FHIR profiles are used to form the Examination Findings Event Message Bundle:

- [DCH-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-Bundle-1)
- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display for the event element is fixed to 'CH012 - Examination Findings'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [CareConnect-DCH-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Practitioner-1)
- [CareConnect-DCH-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PractitionerRole-1)
- [DCH-ExaminationFindings-QuestionnaireResponse-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-ExaminationFindings-QuestionnaireResponse-1)

### Examination Findings Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item                                   | FHIR resource element                                                                           | Mandatory/Required/Optional |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------|-----------------------------|
| Date                                            | CareConnect-DCH-Encounter-1.period.start                                                        | Mandatory                   |
| ODS Site Code                                   | CareConnect-Organization-1.identifier                                                       | Mandatory                   |
| Professional Name                               | CareConnect-DCH-Practitioner-1.name                                                             | Mandatory                   |
| SDS Job Role Name                               | CareConnect-DCH-PractitionerRole-1.code (SDS Job Role Name)                                     | Mandatory                   |
| General Appearance - Colour                     | DCH-ExaminationFindings-QuestionnaireResponse-1.item.generalAppearanceColour                    | Required                    |
| Vital signs                                     | DCH-ExaminationFindings-QuestionnaireResponse-1.item.vitalSigns                                 | Required                    |
| Mental state                                    | DCH-ExaminationFindings-QuestionnaireResponse-1.item.mentalState                                | Required                    |
| Head and Skull                                  | DCH-ExaminationFindings-QuestionnaireResponse-1.item.headAndSkull                               | Required                    |
| Face                                            | DCH-ExaminationFindings-QuestionnaireResponse-1.item.face                                       | Required                    |
| Ears                                            | DCH-ExaminationFindings-QuestionnaireResponse-1.item.ears                                       | Required                    |
| Neck and Clavicles                              | DCH-ExaminationFindings-QuestionnaireResponse-1.item.neckAndClavicles                           | Required                    |
| Oral examination: Mouth and Palate              | DCH-ExaminationFindings-QuestionnaireResponse-1.item.oralExaminationMouthAndPalate              | Required                    |
| Cardiovascular system: Chest                    | DCH-ExaminationFindings-QuestionnaireResponse-1.item.cardiovascularSystemChest                  | Required                    |
| Respiratory system                              | DCH-ExaminationFindings-QuestionnaireResponse-1.item.respiratorySystem                          | Required                    |
| Abdomen                                         | DCH-ExaminationFindings-QuestionnaireResponse-1.item.abdomen                                    | Required                    |
| Abdomen Umbilicus                               | DCH-ExaminationFindings-QuestionnaireResponse-1.item.abdomenUmbilicus                           | Required                    |
| Genitourinary: Genitalia                        | DCH-ExaminationFindings-QuestionnaireResponse-1.item.genitourinaryGenitalia                     | Required                    |
| Genitourinary: Anus                             | DCH-ExaminationFindings-QuestionnaireResponse-1.item.genitorurinaryAnus                         | Required                    |
| Nervous system: Reflexes                        | DCH-ExaminationFindings-QuestionnaireResponse-1.item.nervousSystemReflexes                      | Required                    |
| Musculoskeletal: Manipulation                   | DCH-ExaminationFindings-QuestionnaireResponse-1.item.musculoskeletalManipulation                | Required                    |
| Musculoskeletal: Upper Limbs                    | DCH-ExaminationFindings-QuestionnaireResponse-1.item.musculoskeletalUpperLimbs                  | Required                    |
| Musculoskeletal: Lower Limbs, feet              | DCH-ExaminationFindings-QuestionnaireResponse-1.item.musculoskeletalLowerLimbsFeet              | Required                    |
| Musculoskeletal: Back and Spine                 | DCH-ExaminationFindings-QuestionnaireResponse-1.item.musculoskeletalBackAndSpine                | Required                    |
| Skin                                            | DCH-ExaminationFindings-QuestionnaireResponse-1.item.skin                                       | Required                    |
| Developmental Assessment:- Hearing              | DCH-ExaminationFindings-QuestionnaireResponse-1.item.developmentalAssessmentHearing             | Required                    |
| Developmental Assessment: Locomotion            | DCH-ExaminationFindings-QuestionnaireResponse-1.item.developmentalAssessmentLocomotion          | Required                    |
| Developmental Assessment: Speech/Language       | DCH-ExaminationFindings-QuestionnaireResponse-1.item.developmentalAssessmentSpeechLanguage      | Required                    |
| Developmental Assessment: Behaviour             | DCH-ExaminationFindings-QuestionnaireResponse-1.item.developmentalAssessmentBehaviour           | Required                    |
| Developmental Assessment: Posture and Behaviour | DCH-ExaminationFindings-QuestionnaireResponse-1.item.developmentalAssessmentPostureAndBehaviour | Required                    |
| Examination: Vision                             | DCH-ExaminationFindings-QuestionnaireResponse-1.item.examinationVision                          | Required                    |
| Examination: Bowels                             | DCH-ExaminationFindings-QuestionnaireResponse-1.item.examination.Bowels                         | Required                    |
| Examination: Urine                              | DCH-ExaminationFindings-QuestionnaireResponse-1.item.examinationUrine                           | Required                    |
| Encounter Type                                  | CareConnect-DCH-Encounter-1.type (childHealthEncounterType)                                     | Mandatory                    |