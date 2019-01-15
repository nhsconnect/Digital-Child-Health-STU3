---
title: NIPE Outcome Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_nipe_outcome.html
summary: "The FHIR profiles used for the NIPE Outcome Event Message Bundle"
---

The following FHIR profiles are used to form the NIPE Outcome Event Message Bundle:

- [DCH-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-Bundle-1)
- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display for the event element is fixed to 'CH024 - Physical Examination'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [CareConnect-DCH-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Practitioner-1)
- [CareConnect-DCH-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PractitionerRole-1)
- [CareConnect-DCH-PhysicalExaminationHips-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PhysicalExaminationHips-Procedure-1)
- [CareConnect-DCH-PhysicalExaminationEyes-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PhysicalExaminationEyes-Procedure-1)
- [CareConnect-DCH-PhysicalExaminationTestes-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PhysicalExaminationTestes-Procedure-1)
- [CareConnect-DCH-PhysicalExaminationHeart-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PhysicalExaminationHeart-Procedure-1)
- [DCH-ProfessionalComment-Communication-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-ProfessionalComment-Communication-1)

### Physical Examination Details Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:
                                                                                                   
<table>
<tr>
<th>DCH Data Item</th><th>FHIR resource element</th><th>Mandatory/<br/>Required/<br/>Optional</th><th>Note</th>
</tr>
<tr>
<td>Date/Time</td><td>CareConnect-DCH-Encounter-1.period.start</td><td>Required</td><td></td>
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
<td>Outcome Status Hips</td><td>CareConnect-DCH-PhysicalExaminationHips-Procedure-1.outcome</td><td>Mandatory</td><td></td>
</tr>
<tr>
<td>Outcome Status Eyes</td><td>CareConnect-DCH-PhysicalExaminationEyes-Procedure-1.outcome</td><td>Mandatory</td><td></td>
</tr>
<tr>
<td>Outcome Status Testes</td><td>CareConnect-DCH-PhysicalExaminationTestes-Procedure-1.outcome</td><td>Mandatory</td><td></td>
</tr>
<tr>
<td>Outcome Status Heart</td><td>CareConnect-DCH-PhysicalExaminationHeart-Procedure-1.outcome</td><td>Mandatory</td><td></td>
</tr>
<tr>
<td>Comment</td><td>DCH-ProfessionalComment-Communication-1</td><td>Optional</td><td></td>
</tr>
</table>

### Linkage Diagram ###

<img src="images/explore/NIPE-Outcome.png">

### NIPE Outcome XML Example ###

<script src="https://gist.github.com/IOPS-DEV/646e6275b390034a5a1fbf7948b8375b.js"></script>

### NIPE Outcome JSON Example ###

<script src="https://gist.github.com/IOPS-DEV/6463522f305a65b01af174283acc21f4.js"></script>