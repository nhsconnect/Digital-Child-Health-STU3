---
title: Assessment Scales Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_assessment_scales.html
summary: "The FHIR profiles used for the Assessment Scales Event Message Bundle"
---

{% include important.html content="The links below will refer to the StructureDefinition url applied to the FHIR profile, which are not yet active. For queries please refer to the Help and Support section." %} 

The following FHIR profiles are used to form the Assessment Scales Event Message Bundle:

- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1.xml) - where the coding and display elements for the 'event' type are fixed to 'Assessment Scales'
- [CareConnect-DCH-Organization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Organization-1.xml)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1.xml)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1.xml)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1.xml)
- [CareConnect-DCH-Location-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Location-1.xml)
- [CareConnect-DCH-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Practitioner-1.xml)
- [CareConnect-DCH-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PractitionerRole-1.xml)
- [CareConnect-DCH-ASQ3AssessmentScale-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-ASQ3AssessmentScale-Observation-1.xml)
- [CareConnect-DCH-ASQSEAssessmentScale-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-ASQSEAssessmentScale-Observation-1.xml)
- [CareConnect-DCH-AssessmentScale-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-AssessmentScale-Observation-1.xml)
                                                                                                   
### Assessment Scales event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

**Assessment Scales Child Health Event**

| DCH Data Item              | FHIR Resource element                                                                     | Mandatory/Required/Optional |
|----------------------------|-------------------------------------------------------------------------------------------|-----------------------------|
| Date                       | CareConnect-DCH-Encounter-1.period.start                                                  | Mandatory                   |
| ODS Site Code              | CareConnect-DCH-Location-1.identifier (ODS Site Code)                                     | Mandatory                   |
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
| Coded Assessment Tool Type | CareConnect-DCH-ASQSEAssessmentScale-Observation-1.code 									   | Mandatory                   |
| Score                      | CareConnect-DCH-ASQSEAssessmentScale-Observation-1.component.valueQuantity				   | Mandatory                   |

**Other Assessment Tools**

| DCH Data Item              | FHIR Resource element                                                                                   | Mandatory/Required/Optional |
|----------------------------|---------------------------------------------------------------------------------------------------------|-----------------------------|
| Coded Assessment Tool Type | CareConnect-DCH-AssessmentScale-Observation-1.code 													   | Required                    |
| Score                      | CareConnect-DCH-AssessmentScale-Observation-1.value[x]									       		   | Required                    |


