---
title: Blood Spot Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_blood_spot.html
summary: "The FHIR profiles used for the Blood Spot Event Message Bundle"
---

{% include important.html content="The links below will refer to the StructureDefinition url applied to the FHIR profile, which are not yet active. For queries please refer to the Help and Support section." %} 

The following FHIR profiles are used to form the Blood Spot Event Message Bundle:

- [DCH-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-Bundle-1)
- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display for the event element is fixed to 'Blood Spot'
- [CareConnect-DCH-Organization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-DCH-Location-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Location-1)
- [CareConnect-DCH-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Practitioner-1)
- [CareConnect-DCH-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PractitionerRole-1) 
- [CareConnect-DCH-NewbornBloodSpotScreeningPKU-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-NewbornBloodSpotScreeningPKU-Procedure-1)
- [CareConnect-DCH-NewbornBloodSpotScreeningSCD-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-NewbornBloodSpotScreeningSCD-Procedure-1)
- [CareConnect-DCH-NewbornBloodSpotScreeningCF-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-NewbornBloodSpotScreeningCF-Procedure-1)
- [CareConnect-DCH-NewbornBloodSpotScreeningCHT-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-NewbornBloodSpotScreeningCHT-Procedure-1)
- [CareConnect-DCH-NewbornBloodSpotScreeningMCADD-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-NewbornBloodSpotScreeningMCADD-Procedure-1)
- [CareConnect-DCH-NewbornBloodSpotScreeningHCU-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-NewbornBloodSpotScreeningHCU-Procedure-1)
- [CareConnect-DCH-NewbornBloodSpotScreeningMSUD-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-NewbornBloodSpotScreeningMSUD-Procedure-1)
- [CareConnect-DCH-NewbornBloodSpotScreeningGA1-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-NewbornBloodSpotScreeningGA1-Procedure-1)
- [CareConnect-DCH-NewbornBloodSpotScreeningIVA-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-NewbornBloodSpotScreeningIVA-Procedure-1)
- [DCH-NewbornBloodSpotScreening-DiagnosticReport-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-NewbornBloodSpotScreening-DiagnosticReport-1)
- [DCH-NewbornBloodSpotScreening-ProcedureRequest-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-NewbornBloodSpotScreening-ProcedureRequest-1)
- [DCH-NewbornBloodSpotScreening-Specimen-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-NewbornBloodSpotScreening-Specimen-1)


### Blood Spot event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below.

**Blood Spot Sample Taken Event**

| DCH Data Item     | FHIR resource element                           | Mandatory/Required/Optional |
|-------------------|-------------------------------------------------|-----------------------------|
| Date              | CareConnect-DCH-Encounter-1.period.start        | Mandatory                   |
| ODS Site Code     | CareConnect-DCH-Location-1.identifier (ODS Site Code)          | Mandatory                   |
| Professional Name | CareConnect-DCH-Practitioner-1.name | Mandatory                   |
| SDS Job Role Name | CareConnect-DCH-PractitionerRole-1.code (SDS Job Role Name)            | Mandatory                   |
| Date              | DCH-NewbornBloodSpotScreening-ProcedureRequest-1.authoredOn                | Mandatory                   |

**Blood Spot Administrative Status Event**

| DCH Data Item           | FHIR resource element                     | Mandatory/Required/Optional |
|-------------------------|-------------------------------------------|-----------------------------|
| Date                    | DCH-NewbornBloodSpotScreening-Specimen-1.receivedTime               | Required                    |
| Laboratory Identifier | CareConnect-DCH-Organisation-1.identifier | Required                    |

**Blood Spot Test Outcome Event**

| DCH Data Item                                            | FHIR resource element             | Mandatory/Required/Optional |
|----------------------------------------------------------|-----------------------------------|-----------------------------|
| Date                                                     | DCH-NewbornBloodSpotScreening-DiagnosticReport-1.issued     | Mandatory                   |
| Outcome - PHENYLKETONURIA                                | CareConnect-DCH-NewbornBloodSpotScreeningPKU-Procedure-1.outcome | Mandatory                   |
| Outcome - SICKLE CELL DISEASE                            | CareConnect-DCH-NewbornBloodSpotScreeningSCD-Procedure-1.outcome | Mandatory                   |
| Outcome - CYSTIC FIBROSIS                                | CareConnect-DCH-NewbornBloodSpotScreeningCF-Procedure-1.outcome | Mandatory                   |
| Outcome - CONGENITAL HYPOTHYROIDISM                      | CareConnect-DCH-NewbornBloodSpotScreeningCHT-Procedure-1.outcome | Mandatory                   |
| Outcome - MEDIUM CHAIN ACYL-COA DEHYDROGENASE DEFICIENCY | CareConnect-DCH-NewbornBloodSpotScreeningMCADD-Procedure-1.outcome | Mandatory                   |
| Outcome - HOMOCYSTINURIA                                 | CareConnect-DCH-NewbornBloodSpotScreeningHCU-Procedure-1.outcome | Mandatory                   |
| Outcome - MAPLE SYRUP URINE DISEASE                      | CareConnect-DCH-NewbornBloodSpotScreeningMSUD-Procedure-1.outcome | Mandatory                   |
| Outcome - GLUTARIC ACIDURIA TYPE 1                       | CareConnect-DCH-NewbornBloodSpotScreeningGA1-Procedure-1.outcome | Mandatory                   |
| Outcome - ISOVALERIC ACIDAEMIA                            | CareConnect-DCH-NewbornBloodSpotScreeningIVA-Procedure-1.outcome | Mandatory                   |

