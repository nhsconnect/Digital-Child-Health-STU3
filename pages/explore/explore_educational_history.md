---
title: Educational History Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_educational_history.html
summary: "The FHIR profiles used for the Educational History Event Message Bundle"
---

The following FHIR profiles are used to form the Educational History Event Message Bundle:

- [DCH-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-Bundle-1)
- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display for the event element is fixed to 'CH032 - Educational History'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [DCH-EducationalHistory-QuestionnaireResponse-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-EducationalHistory-QuestionnaireResponse-1)

### Educational History Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item                      | FHIR Resource element                                                                 | Mandatory/Required/Optional |
|------------------------------------|---------------------------------------------------------------------------------------|-----------------------------|
| Educational establishment attended | DCH-EducationalHistory-QuestionnaireResponse-1.item.educationalEstablishmentName  | Mandatory                   |
| Type of Educational establishment  | DCH-EducationalHistory-QuestionnaireResponse-1.item.educationalEstablishmentType  | Mandatory                   |
| Year From                          | DCH-EducationalHistory-QuestionnaireResponse-1.item.educationalEstablishmentStart | Mandatory                   |
| Year To                            | DCH-EducationalHistory-QuestionnaireResponse-1.item.educationalEstablishmentEnd   | Mandatory                   |
| Educational Assessment             | DCH-EducationalHistory-QuestionnaireResponse-1.item.educationalAssessmentOutcome  | Required                    |
| Type of Special Educational Need   | DCH-EducationalHistory-QuestionnaireResponse-1.item.specialEducationalNeedType    | Required                    |
