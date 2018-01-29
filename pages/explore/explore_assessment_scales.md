---
title: Assessment Scales Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_assessment_scales.html
summary: "The FHIR profiles used for the Assessment Scales Event Message Bundle"
---
{% include custom/under.construction.html content="Please check back later for any updates to this page" %}

The following FHIR profiles are used to form the Assessment Scales Event Message Bundle:

- DCH-MessageHeader-1 - where the coding and display elements for the 'event' type are fixed to 'Assessment Scales'
- CareConnect-DCH-Organization-1
- CareConnect-DCH-Patient-1
- CareConnect-DCH-ASQ3AssessmentScale-Observation-1
- CareConnect-DCH-ASQSEAssessmentScale-Observation-1
- CareConnect-DCH-AssessmentScale-Observation-1
- CareConnect-DCH-Encounter-1
- DCH-HealthcareService-1
- CareConnect-DCH-Practitioner-1
- CareConnect-DCH-PractitionerRole-1
- CareConnect-DCH-Location-1
                                                                                                   
### Assessment Scales event data item mapping to FHIR profiles ###
----------
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
| Score                      | CareConnect-DCH-ASQ3AssessmentScale-Observation-1.valueRange						     | Mandatory                   |

**Ages and Stages Questionnaires: Social-Emotional**

| DCH Data Item              | FHIR Resource element                                                                       | Mandatory/Required/Optional |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------------|
| Coded Assessment Tool Type | CareConnect-DCH-ASQSEAssessmentScale-Observation-1.code 									   | Mandatory                   |
| Score                      | CareConnect-DCH-ASQSEAssessmentScale-Observation-1.valueRange							   | Mandatory                   |

**Other Assessment Tools**

| DCH Data Item              | FHIR Resource element                                                                                   | Mandatory/Required/Optional |
|----------------------------|---------------------------------------------------------------------------------------------------------|-----------------------------|
| Coded Assessment Tool Type | CareConnect-DCH-AssessmentScale-Observation-1.code 													   | Required                    |
| Score                      | CareConnect-DCH-AssessmentScale-Observation-1.valueString										       | Required                    |


