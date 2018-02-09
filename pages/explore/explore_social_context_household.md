---
title: Social Context Household Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_social_context_household.html
summary: "The FHIR profiles used for the Social Context Household Event Message Bundle"
---

{% include important.html content="The links below will refer to the StructureDefinition url applied to the FHIR profile, which are not yet active. For queries please refer to the Help and Support section." %} 

The following FHIR profiles are used to form the Social Context Household Event Message Bundle:

- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1.xml) - where the coding and display for the event element is fixed to 'Social Context Household'
- [CareConnect-DCH-Organization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Organization-1.xml)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1.xml)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1.xml)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1.xml)
- [CareConnect-DCH-Location-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Location-1.xml)
- [DCH-SocialContextHousehold-QuestionnaireResponse-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-SocialContextHousehold-QuestionnaireResponse-1)

### Social Context Household event data item mapping to FHIR profiles ###
----------
The Child Health Event data items are fulfilled by elements within the FHIR resources listed below.

| DCH Data Item                                        | FHIR Resource element                                                                        | Mandatory/Required/Optional |
|------------------------------------------------------|----------------------------------------------------------------------------------------------|-----------------------------|
| Mothers Education Level                              | DCH-SocialContextHousehold-QuestionnaireResponse-1.item.mothersEducationLevel          | Required                    |
| Household smoking status                             | DCH-SocialContextHousehold-QuestionnaireResponse-1.item.householdSmokingStatus         | Required                    |
| Household substance status                           | DCH-SocialContextHousehold-QuestionnaireResponse-1.item.householdSubstanceStatus       | Required                    |
| Household alcohol drinking status                    | DCH-SocialContextHousehold-QuestionnaireResponse-1.item.householdAlcoholDrinkingStatus | Required                    |
| Employment status (Mother                           | DCH-SocialContextHousehold-QuestionnaireResponse-1.item.employmentStatusMother         | Required                    |
| Mothers Occupation                                   | DCH-SocialContextHousehold-QuestionnaireResponse-1.item.occupationMother               | Required                    |
| Employment status (Father                           | DCH-SocialContextHousehold-QuestionnaireResponse-1.item.employmentStatusFather         | Required                    |
| Fathers Occupation                                   | DCH-SocialContextHousehold-QuestionnaireResponse-1.item.occupationFather               | Required                    |
| Any Household member has/had social services support | DCH-SocialContextHousehold-QuestionnaireResponse-1.item.socialServicesSupport          | Required                    |
| Accommodation status                                 | DCH-SocialContextHousehold-QuestionnaireResponse-1.item.accommodationStatus            | Mandatory                   |
| Household Composition                                 | DCH-SocialContextHousehold-QuestionnaireResponse-1.item.householdComposition            | Optional                   |
| Significant Individuals                                 | DCH-SocialContextHousehold-QuestionnaireResponse-1.item.significantIndividuals            | Optional                |