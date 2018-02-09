---
title: Birth Details Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_birth_details.html
summary: "The FHIR profiles used for the Birth Details Event Message Bundle"
---

{% include important.html content="The links below will refer to the StructureDefinition url applied to the FHIR profile, which are not yet active. For queries please refer to the Help and Support section." %} 

The following FHIR profiles are used to form the Birth Details Event Message Bundle:

- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1.xml) - where the coding and display for the event element is fixed to 'Birth Details'
- [CareConnect-DCH-Organization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Organization-1.xml)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1.xml)
- [CareConnect-DCH-Baby-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Baby-Patient-1.xml)
- [CareConnect-DCH-Birth-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Birth-Encounter-1.xml)
- [CareConnect-DCH-ProblemAtBirth-Condition-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-ProblemAtBirth-Condition-1.xml)
- [CareConnect-DCH-ProblemDuringDelivery-Condition-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-ProblemDuringDelivery-Condition-1.xml)
- [CareConnect-DCH-APGARScore-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-APGARScore-Observation-1.xml)
- [CareConnect-DCH-LengthOfGestation-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-LengthOfGestation-Observation-1.xml)
- [CareConnect-DCH-NumberOfBirths-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-NumberOfBirths-Observation-1.xml)
- [CareConnect-DCH-SpontaneousRespirationOnset-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-SpontaneousRespirationOnset-Observation-1.xml)
- [CareConnect-DCH-NeonatalResuscitationMethod-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-NeonatalResuscitationMethod-Procedure-1.xml)
- [CareConnect-DCH-TypeOfDelivery-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-TypeOfDelivery-Procedure-1.xml)
- [CareConnect-DCH-PutToBreastIndicator-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PutToBreastIndicator-Observation-1.xml)
- [CareConnect-DCH-FraternalTwinIndicator-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-FraternalTwinIndicator-Observation-1.xml)
- [CareConnect-DCH-Delivery-Location-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Delivery-Location-1.xml)

### Birth Details event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item                       | FHIR resource element                                                   | Mandatory/Required/Optional |
|-------------------------------------|-------------------------------------------------------------------------|-----------------------------|
| Location of Birth                   | CareConnect-DCH-Delivery-Location-1.identifier (ODS Site Code)           | Mandatory                   |
| Delivery Place Type Code            | CareConnect-DCH-Delivery-Location-1.physicalType                        | Mandatory                   |
| Birth Order                         | CareConnect-DCH-Baby-Patient-1.multipleBirthInteger                     | Mandatory                   |
| Length of Gestation at Birth        | CareConnect-DCH-LengthOfGestation-Observation-1.valueQuantity           | Mandatory                   |
| Number of Births in confinement     | CareConnect-DCH-NumberOfBirths-Observation-1.valueQuantity                  | Mandatory                    |
| Problems during Delivery            | CareConnect-DCH-ProblemDuringDelivery-Condition-1.code                          | Required                    |
| Physical Problems detected at Birth | CareConnect-DCH-ProblemAtBirth-Condition-1.code            | Required                    |
| Neonatal Resuscitation Method       | CareConnect-DCH-NeonatalResuscitationMethod-Procedure-1.code                           | Required                 |
| Date and Time of Birth              | CareConnect-DCH-Baby-Patient-1.birthDate                           | Mandatory                 |
| Type of Delivery                    | CareConnect-DCH-TypeOfDelivery-Procedure-1.code   | Mandatory                    |
| Attempted Type of Delivery          | CareConnect-DCH-TypeOfDelivery-Procedure-1.code where the 'status' element is presented as 'aborted'  | Required                    |
| Onset of Spontaneous Respiration    | CareConnect-DCH-SpontaneousRespirationOnset-Observation-1.valueQuantity  | Optional                    |
| APGAR Score (1 Minute)              | CareConnect-DCH-APGARScore-Observation-1.valueRange                 | Mandatory                   |
| APGAR Score (5 Minute)              | CareConnect-DCH-APGARScore-Observation-1.valueRange                  | Mandatory                   |
| APGAR Score (10 Minute)             | CareConnect-DCH-APGARScore-Observation-1.valueRange                | Optional                    |
| Put To Breast                       | CareConnect-DCH-PutToBreastIndicator-Observation-1.code                  | Required                    |
| Identical Twin Indicator		      | CareConnect-DCH-FraternalTwinIndicator-Observation-1.code               | Optional                    |

