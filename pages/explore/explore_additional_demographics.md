---
title: Additional Demographics Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_additional_demographics.html
summary: "The FHIR profiles used for the Additional Demographics Event Message Bundle"
---
{% include custom/under.construction.html content="Please check back later for any updates to this page" %}

{% include important.html content="The links below will refer to the StructureDefinition url applied to the FHIR profile, which are not yet active. For queries please refer to the Help and Support section." %} 

The following FHIR profiles are used to form the Additional Demographics Event Message Bundle:

- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1.xml) - where the coding and display elements for the 'event' type are fixed to 'Additional Demographics'
- [CareConnect-DCH-Organization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Organization-1.xml)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1.xml)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1.xml)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1.xml)
- [CareConnect-DCH-Location-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Location-1.xml)
                                                                                                   
### Additional Demographics event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item            | FHIR resource element                                 | Mandatory/Required/Optional |
|--------------------------|-------------------------------------------------------|-----------------------------|
| Local Patient Identifier | CareConnect-DCH-Patient-1.identifier (localIdentifier) | Mandatory                   |
| Town of Birth            | CareConnect-DCH-Patient-1.birthPlace                  | Required                    |
| Country of Birth         | CareConnect-DCH-Patient-1.birthPlace                  | Required                    |
| Communication Preference | CareConnect-DCH-Patient-1.telecom.system              | Required                    |
| Patient email address    | CareConnect-DCH-Patient-1.telecom.value               | Required                    |
| Ethnicity                | CareConnect-DCH-Patient-1.ethnicCategory              | Required                    |
| Religion                 | CareConnect-DCH-Patient-1.religiousAffiliation        | Required                    |

