---
title: Social Context Person Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_social_context_person.html
summary: "The FHIR profiles used for the Social Context Person Event Message Bundle"
---

The following FHIR profiles are used to form the Social Context Person Event Message Bundle:

- [DCH-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-Bundle-1)
- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display for the event element is fixed to 'CH032 - Social Context Person'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [DCH-SocialContextPerson-QuestionnaireResponse-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-SocialContextPerson-QuestionnaireResponse-1)

### Social Context Person Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below.
                                                                                                   
| DCH Data Item        | FHIR Resource element                                                             | Mandatory/Required/Optional |
|----------------------|-----------------------------------------------------------------------------------|-----------------------------|
| Social Circumstances | DCH-SocialContextHousehold-QuestionnaireResponse-1.item.socialCircumstances | Required                    |
| Lifestyle            | DCH-SocialContextHousehold-QuestionnaireResponse-1.item.lifestyle           | Required                    |
| Smoking Status       | DCH-SocialContextHousehold-QuestionnaireResponse-1.item.smokingStatus       | Required                    |
| Alcohol intake       | DCH-SocialContextHousehold-QuestionnaireResponse-1.item.alchoholIntake      | Required                    |
| Drug/substance use   | DCH-SocialContextHousehold-QuestionnaireResponse-1.item.substanceStatus      | Required                    |