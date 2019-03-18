---
title: Newborn Hearing Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_newborn_hearing.html
summary: "The FHIR profiles used for the Newborn Hearing Event Message Bundle"
---

- [DCH-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-Bundle-1)
- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display for the event element is fixed to 'CH021 - Newborn Hearing'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [CareConnect-DCH-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Practitioner-1)
- [CareConnect-DCH-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PractitionerRole-1) 
- [CareConnect-DCH-AABRHearingTest-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-AABRHearingTest-Procedure-1)
- [CareConnect-DCH-AOAEHearingTest-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-AOAEHearingTest-Procedure-1)
- [CareConnect-DCH-HearingScreeningSummaryOutcome-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-HearingScreeningSummaryOutcome-Observation-1)
- [DCH-ProfessionalComment-Communication-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-ProfessionalComment-Communication-1) 

### Newborn Hearing Event data item mapping to FHIR profiles ###

This Mapping table defines the FHIR elements that SHALL be used to encode the Healthy Child Event Specification data items for each DCH Event Message payload.  
Some common data item mappings, such as patient, publisher or Date/Time of event information, are defined within the [Header mapping table](./explore_event_header_design.html) and SHALL be considered in parallel with the payload mapping.

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:
                                                                     
| DCH Data Item                  | FHIR resource element                               | Mandatory/<br/>Required/<br/>Optional | Note                                                                  |
|--------------------------------|-----------------------------------------------------|---------------------------------------|-----------------------------------------------------------------------|
| Date/Time                      | CareConnect-DCH-Encounter-1.period.start            | Mandatory                             |                                                                       |
| Location (ODS Site Code)       | CareConnect-Location-1.identifier                   | Required                              |                                                                       |
| Performing Professional        | CareConnect-DCH-Practitioner-1.name                 | Required                              |                                                                       |
| SDS Job Role Name              | CareConnect-DCH-PractitionerRole-1.codeableConcept  | Required                              | * |
| Hearing Test Results (AABR)    | CareConnect-DCH-AABRHearingTest-Procedure-1.outcome | Required                              | two occurrences of this resource are required, one for each ear |
| Hearing Test Result (AOAE)     | CareConnect-DCH-AOAEHearingTest-Procedure-1.outcome |Required                               | up to four occurrences of this resource are required, with two for each test performed |
| Summary Outcome                | CareConnect-DCH-HearingScreeningSummaryOutcome-Observation-1.valueCodeableConcept           | Mandatory                   |                                          |
| Comment                        | DCH-ProfessionalComment-Communication-1                  | Optional                         |                                                                        |

**\*** Northgate do not record SDS Job Role Codes as part of their Child Health Screening record. As the code is typed CodeableConcept, and sliced on system, a system must be present. i.e. we can't just send:
```
        <!-- Do not do this -->
        <code>
            <text value="Specialist Registrar"/>
        </code>
```

We therefore use the UNC code from the HL7 nullFlavor codesystem to indicate there is no SDS Job Role Code. The Job Role Name is contained in the text element. Example below:
```
        <code>
            <coding>
                <system value="http://hl7.org/fhir/v3/NullFlavor"/>
                <code value="UNC"/>
                <display value="un-encoded"/>
            </coding>
            <text value="Specialist Registrar"/>
        </code>
```

### Reference Linkage Diagram ###

This Linkage diagram defines the required references that SHALL be made between resources within the DCH Event Message bundle. It includes both Header and Payload resources (but omits the DCH-Bundle-1 wrapper).

<img src="images/explore/NewbornHearing1.png">

Allowed Child Health Observations are: 

<img src="images/explore/NewbornHearing2.png">

### Examples ###

<script src="https://gist.github.com/IOPS-DEV/b8f0d3a8da033037ad0dfbd60a662d93.js"></script>

<script src="https://gist.github.com/IOPS-DEV/d50001b1a618a5ae1f89394cfeaa7ae8.js"></script>
