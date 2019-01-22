---
title: Legal Information Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_legal_information.html
summary: "The FHIR profiles used for the Legal Information Event Message Bundle"
---

The following FHIR profiles are used to form the Legal Information Event Message Bundle:

- [DCH-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-Bundle-1)
- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display elements for the 'event' type are fixed to 'CH033 - Legal Information'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [CareConnect-DCH-LookedAfterChildStartDate-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-LookedAfterChildStartDate-Observation-1)
- [CareConnect-DCH-LookedAfterChildEndDate-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-LookedAfterChildEndDate-Observation-1)
- [CareConnect-DCH-ChildProtectionPlanStartDate-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-ChildProtectionPlanStartDate-Observation-1)
- [CareConnect-DCH-ChildProtectionPlanEndDate-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-ChildProtectionPlanEndDate-Observation-1)

### Legal Information Event data item mapping to FHIR profiles ###

This Mapping table defines the FHIR elements that SHALL be used to encode the Healthy Child Event Specification data items for each DCH Event Message payload.  
Some common data item mappings, such as patient, publisher or Date/Time of event information, are defined within the [Header mapping table](../explore_event_header_design.html) and SHALL be considered in parallel with the payload mapping.

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item                                                | FHIR Resource element                                                 | Mandatory/Required/Optional |
|--------------------------------------------------------------|-----------------------------------------------------------------------|-----------------------------|
| Date                                                         | CareConnect-DCH-Encounter-1.period.start                              | Mandatory                   |
| Looked After Child Start Date                                | CareConnect-DCH-LookedAfterChildStartDate-Observation-1.valueDateTime | Required                    |
| Looked After Child End Date                                  | CareConnect-DCH-LookedAfterChildEndDate-Observation-1.valueDateTime   | Required                    |
| Local Authority (LAC)                                        | CareConnect-Organization-1.name                                       | Required                    |
| Local Authority (LAC) ODS Site Code                          | CareConnect-Organization-1.identifier (oDSOrganizationCode)           | Required                    |
| Local Authority (LAC) Office Hours Telephone                 | CareConnect-Organization-1.telecom                                    | Required                    |
| Local Authority (LAC) Emergeny Duty Team Telephone           | CareConnect-Organization-1.contact.telecom                            | Required                    |
| Child Protection Plan Start Date                             | CareConnect-DCH-ChildProtectionPlanStartDate-Observation-1.valueDateTime       | Required                    |
| Child Protection Plan End Date                               | CareConnect-DCH-ChildProtectionPlanEndDate-Observation-1.valueDateTime         | Required                    |
| Local Authority (CPP)                                        | CareConnect-Organization-1.name                                       | Required                    |
| Local Authority (CPP) ODS Site Code                          | CareConnect-Organization-1.identifier (oDSOrganizationCode)           | Required                    |
| Local Authority (CPP) Office Hours Telephone                 | CareConnect-Organization-1.telecom                                    | Required                    |
| Local Authority (CPP) Emergeny Duty Team Telephone           | CareConnect-Organization-1.contact.telecom                            | Required                    |

LAC: Looked After Child  
CPP: Child Protection Plan  
ODS: Organisation Data Service  

### Linkage Diagram ###

This Linkage diagram defines the required references that SHALL be made between resources within the DCH Event Message bundle. It includes both Header and Payload resources (but omits the DCH-Bundle-1 wrapper).

<img src="images/explore/LegalInformation1.png">

Required Child Health Observations are:

<img src="images/explore/LegalInformation2.png">

### Legal Information XML Example ###

<script src="https://gist.github.com/IOPS-DEV/177dc20663f8d3d5e4c67b4990ff2129.js"></script>

### Legal Information JSON Example ###

<script src="https://gist.github.com/IOPS-DEV/bdecb82cb6b07a1bb987f0f9f479110c.js"></script>