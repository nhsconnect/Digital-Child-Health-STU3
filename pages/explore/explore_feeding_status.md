---
title: Feeding Status Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_feeding_status.html
summary: "The FHIR profiles used for the Feeding Status Event Message Bundle"
---

{% include important.html content="The links below will refer to the StructureDefinition url applied to the FHIR profile, which are not yet active. For queries please refer to the Help and Support section." %} 

The following FHIR profiles are used to form the Feeding Status Event Message Bundle:

- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1.xml) - where the coding and display for the event element is fixed to 'Feeding Status'
- [CareConnect-DCH-Organization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Organization-1.xml)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1.xml)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1.xml)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1.xml)
- [CareConnect-DCH-Location-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Location-1.xml)
- [DCH-FeedingStatus-QuestionnaireResponse-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-FeedingStatus-QuestionnaireResponse-1)

### Feeding Status event data item mapping to FHIR profiles ###
----------
The Child Health Event data items are fulfilled by elements within the FHIR resources listed below.
                                                                                                   
| DCH Data Item                                | FHIR resource element                                                                          | Mandatory/Required/Optional |
|----------------------------------------------|------------------------------------------------------------------------------------------------|-----------------------------|
| Date                                         | CareConnect-DCH-Encounter-1.period.start or DCH-FeedingStatus-QuestionnaireResponse-1.authored | Mandatory                   |
| First Milk Feed                              | DCH-FeedingStatus-QuestionnaireResponse-1.item.firstMilkFeed                | Mandatory                   |
| Feeding Status of the baby                   | DCH-FeedingStatus-QuestionnaireResponse-1.item.feedingStatus                | Mandatory                   |
| Feeding method                               | DCH-FeedingStatus-QuestionnaireResponse-1.item.feedingMethod              | Required                    |
| Introduction of Solids                       | DCH-FeedingStatus-QuestionnaireResponse-1.item.introductionOfSolids        | Required                    |
| Approximate Date breastfeeding stopped       | DCH-FeedingStatus-QuestionnaireResponse-1.item.breastfeedingEndedDate       | Required                    |
| Encounter Type                               | CareConnect-DCH-Encounter-1.type (childHealthEncounterType)                                      | Mandatory                   |