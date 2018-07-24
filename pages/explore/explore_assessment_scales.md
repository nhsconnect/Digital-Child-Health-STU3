---
title: Assessment Scales Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_assessment_scales.html
summary: "The FHIR profiles used for the Assessment Scales Event Message Bundle"
---

The following FHIR profiles are used to form the Assessment Scales Event Message Bundle:

- [DCH-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-Bundle-1)
- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display elements for the 'event' type are fixed to 'CH004 - Assessment Scales'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [CareConnect-DCH-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Practitioner-1)
- [CareConnect-DCH-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PractitionerRole-1)
- [CareConnect-DCH-ASQ3AssessmentScale-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-ASQ3AssessmentScale-Observation-1)
- [CareConnect-DCH-ASQSE-AssessmentScale-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-ASQSE-AssessmentScale-Observation-1)
- [CareConnect-DCH-AssessmentScale-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-AssessmentScale-Observation-1)
                                                                                                   
### Assessment Scales Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

**Assessment Scales Child Health Event**

| DCH Data Item              | FHIR Resource element                                                                     | Mandatory/Required/Optional |
|----------------------------|-------------------------------------------------------------------------------------------|-----------------------------|
| Date                       | CareConnect-DCH-Encounter-1.period.start                                                  | Mandatory                   |
| ODS Site Code              | CareConnect-Location-1.identifier (ODS Site Code)                                     | Mandatory                   |
| Professional Name          | CareConnect-DCH-Practitioner.name                                                         | Mandatory                   |
| SDS Job Role Name          | CareConnect-DCH-PractitionerRole-1.code (SDS Job Role Name)	                             | Mandatory                   |

**ASQ-3 (Ages and Stages Questionnaires Third Edition)**

| DCH Data Item              | FHIR Resource element                                                                     | Mandatory/Required/Optional |
|----------------------------|-------------------------------------------------------------------------------------------|-----------------------------|
| Coded Assessment Tool Type | CareConnect-DCH-ASQ3AssessmentScale-Observation-1.code 									 | Mandatory                   |
| Score                      | CareConnect-DCH-ASQ3AssessmentScale-Observation-1.component.valueQuantity				 | Mandatory                   |

**Ages and Stages Questionnaires: Social-Emotional**

| DCH Data Item              | FHIR Resource element                                                                       | Mandatory/Required/Optional |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------------|
| Coded Assessment Tool Type | CareConnect-DCH-ASQSE-AssessmentScale-Observation-1.code 									   | Mandatory                   |
| Score                      | CareConnect-DCH-ASQSE-AssessmentScale-Observation-1.component.valueQuantity				   | Mandatory                   |

**Other Assessment Tools**

| DCH Data Item              | FHIR Resource element                                                                                   | Mandatory/Required/Optional |
|----------------------------|---------------------------------------------------------------------------------------------------------|-----------------------------|
| Coded Assessment Tool Type | CareConnect-DCH-AssessmentScale-Observation-1.code 													   | Required                    |
| Score                      | CareConnect-DCH-AssessmentScale-Observation-1.value[x] or CareConnect-DCH-AssessmentScale-Observation-1.componentvalue[x]										       		   | Required                    |


