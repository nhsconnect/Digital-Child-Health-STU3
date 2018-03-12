---
title: Educational History Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_educational_history.html
summary: "The FHIR profiles used for the Educational History Event Message Bundle"
---

{% include important.html content="The links below will refer to the StructureDefinition url applied to the FHIR profile, which are not yet active. For queries please refer to the Help and Support section." %} 

The following FHIR profiles are used to form the Educational History Event Message Bundle:

- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display for the event element is fixed to 'Educational History'
- [CareConnect-DCH-Organization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-DCH-Location-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Location-1)
- [DCH-EducationalHistory-QuestionnaireResponse-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-EducationalHistory-QuestionnaireResponse-1)

### Educational History event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item                      | FHIR Resource element                                                                 | Mandatory/Required/Optional |
|------------------------------------|---------------------------------------------------------------------------------------|-----------------------------|
| Educational establishment attended | DCH-EducationalHistory-QuestionnaireResponse-1.item.educationalEstablishmentName  | Mandatory                   |
| Type of Educational establishment  | DCH-EducationalHistory-QuestionnaireResponse-1.item.educationalEstablishmentType  | Mandatory                   |
| Year From                          | DCH-EducationalHistory-QuestionnaireResponse-1.item.educationalEstablishmentStart | Mandatory                   |
| Year To                            | DCH-EducationalHistory-QuestionnaireResponse-1.item.educationalEstablishmentEnd   | Mandatory                   |
| Educational Assessment             | DCH-EducationalHistory-QuestionnaireResponse-1.item.educationalAssessmentOutcome  | Required                    |
| Type of Special Educational Need   | DCH-EducationalHistory-QuestionnaireResponse-1.item.specialEducationalNeedType    | Required                    |
