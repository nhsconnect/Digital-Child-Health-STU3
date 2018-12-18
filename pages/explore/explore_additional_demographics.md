---
title: Additional Demographics Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_additional_demographics.html
summary: "The FHIR profiles used for the Additional Demographics Event Message Bundle"
---

The following FHIR profiles are used to form the Additional Demographics Event Message Bundle:

- [DCH-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-Bundle-1)
- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display elements for the 'event' type are fixed to 'CH001 - Additional Demographics'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
                                                                                                   
### Additional Demographics Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item            | FHIR resource element                                 | Mandatory/Required/Optional |
|--------------------------|-------------------------------------------------------|-----------------------------|
| Local Patient Identifier | CareConnect-DCH-Patient-1.identifier (localIdentifier) | Mandatory                   |
| Local Patient Identifier assigning Organisation| CareConnect-DCH-Patient-1.identifier(localIdentifier).assigner | Required                   |
| Town of Birth            | CareConnect-DCH-Patient-1.birthPlace                  | Required                    |
| Date and Time            | CareConnect-DCH-Encounter-1.period.start              | Required                    |
| Country of Birth         | CareConnect-DCH-Patient-1.birthPlace                  | Required                    |
| Patient email address    | CareConnect-DCH-Patient-1.telecom.value               | Required                    |
| Ethnicity <br> see table below             | CareConnect-DCH-Patient-1.ethnicCategory              | Required                    |
| Religion                 | CareConnect-DCH-Patient-1.religiousAffiliation        | Required                    |


### Ethnic categories mapping table ###

Ethnicity recording in Digital Child Health is requested to use the reduced 16+1 Ethnic Category list.
However, CareConnect-Patient-1 has a required binding to the [CareConnect-EthnicCategory-1 valueset](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-EthnicCategory-1).  
The following mapping SHOULD be used to map the ethnicCategory value to the reduced valueset.

<table>
<tr>
<th scope="col">DCH (16+1) valueSet</th>
<th scope="col">DCH display</th>
<th scope="col">CareConnect-EthnicCategory-1 valueSet</th>
<th scope="col">CareConnect-EthnicCategory-1 display</th>	​ 	​ 	​
​</tr>

Partial Table - WIP - Awaiting confirmation of mapping

<tr>
  <td rowspan="6">A</td><td rowspan="6">British, Mixed British</td>
  <td>A</td><td>British, Mixed British</td>
</tr>
<tr><td>C2</td><td>Northern Irish</td></tr>
<tr>​<td>CA</td><td>English</td></tr>
<tr>​<td>CB</td><td>Scottish</td></tr>
<tr>​<td>CC</td><td>Welsh</td></tr>
<tr>​<td>CD</td><td>Cornish</td></tr>
<tr>
  <td>B</td><td>Irish</td>
  ​<td>B</td><td>Irish</td>
</tr>
<tr>
  <td rowspan="2">C</td><td rowspan="2">Any other White background</td>
  ​<td>C</td><td>Any other White background</td>
</tr>
<tr>
  <td>C3</td><td>Other white, white unspecified</td>
</tr>
<tr>
  <td>D</td><td>White and Black Caribbean</td>
</tr>
<tr>
  <td>E</td><td>White and Black African</td>
</tr>
<tr>
  <td>F</td><td>White and Asian</td>
</tr>
<tr>
  <td>G</td><td>Any other mixed background</td>
</tr>
<tr>
  <td>H</td><td>Indian or British Indian</td>
</tr>
<tr>
  <td>J</td><td>Pakistani or British Pakistani</td>
</tr>
<tr>
  <td>K</td><td>Bangladeshi or British Bangladeshi</td>
</tr>
<tr>
  <td>L</td><td>Any other Asian background</td>
</tr>
<tr>
  <td>M</td><td>Caribbean</td>
</tr>
<tr>
  <td>N</td><td>African</td>
</tr>
<tr>
  <td>P</td><td>Any other Black background</td>
</tr>
<tr>
  <td>R</td><td>Chinese</td>
</tr>
<tr>
  <td>S</td><td>Any other ethnic group</td>
</tr>
<tr>
  <td>Z</td><td>Not stated</td>
</tr>
