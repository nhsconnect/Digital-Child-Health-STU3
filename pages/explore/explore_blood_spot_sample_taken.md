---
title: Blood Spot Sample Taken Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_blood_spot_sample_taken.html
summary: "The FHIR profiles used for the Blood Spot Sample Taken Event Message Bundle"
---

The following FHIR profiles are used to form the Blood Spot Sample Taken Event Message Bundle:

- [DCH-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-Bundle-1)
- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display for the event element is fixed to 'CH006 - Blood Spot Sample Taken'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [CareConnect-DCH-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Practitioner-1)
- [CareConnect-DCH-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PractitionerRole-1)
- [CareConnect-DCH-NewbornBloodSpotSampleTaken-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-NewbornBloodSpotSampleTaken-Procedure-1)
- [DCH-NewbornBloodSpotScreening-ProcedureRequest-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-NewbornBloodSpotScreening-ProcedureRequest-1)


### Blood Spot Sample Taken event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below.

<table>
<tr>
<th>DCH Data Item</th><th>FHIR resource element</th><th>Mandatory/<br/>Required/<br/>Optional</th><th>Note</th>
</tr>
<tr>
<td>Date</td><td>CareConnect-DCH-NewbornBloodSpotSampleTaken-Procedure-1.performedDateTime</td><td>Mandatory</td><td></td>
</tr>
<tr>
<td>ODS Site Code</td><td>CareConnect-Location-1.identifier (ODS Site Code)</td><td>Required</td><td></td>
</tr>
<tr>
<td>Professional Name</td><td>CareConnect-DCH-Practitioner-1.name</td><td>Required</td><td></td>
</tr>
<tr>
<td>SDS Job Role Name</td><td>CareConnect-DCH-PractitionerRole-1.code (SDS Job Role Name)</td><td>Required</td><td></td>
</tr>
<tr>
<td>Date</td><td>DCH-NewbornBloodSpotScreening-ProcedureRequest-1.authoredOn</td><td>Mandatory</td><td></td>
</tr>
</table>

### Linkage Diagram ###

<img src="images/explore/BloodSpotSampleTaken.png">

### Blood Spot Sample Taken XML Example ###

<script src="https://gist.github.com/IOPS-DEV/495d8e510756d21f29a42d2c022dfb46.js"></script>

### Blood Spot Sample Taken JSON Example ###

<script src="https://gist.github.com/IOPS-DEV/452ebd9647559aa29e280830e35a6d6c.js"></script>