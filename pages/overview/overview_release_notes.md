---
title: Release Notes
keywords: development, versioning
tags: [development]
sidebar: overview_sidebar
permalink: overview_release_notes.html
summary: Summary release notes of the versions released in Digital Child Health Implementation Guide
---

This site is under active development by NHS Digital and is intended to provide the FHIR messaging components for the Digital Child Health event messages. This project is being developed using an agile methodology so iterative updates to content will be added on a regular basis, and remains subject to clinical review. Changes to this specification following the initial beta release will be documented here.

## Beta 1.1.0 ##
Following stakeholder feedback and INTEROPen curation, this implementation guidance has been updated:

- [Digital Child Health Events Model](explore_dch_events_model.html) - a new page sharing Digital Child Health Events Model mapping to Healthy Child Programme interventions
- **Admission Details** - Patient Location clarified to use CareConnect-DCH-Location-1.type.text
- **Birth Details** - Location of Birth changed to Required
- **Blood Spot Card Received** - All items changed to Mandatory
- **Conditions** - Added item Condition end date
- **Clinical Risk Factors** - Relevant Clinical Risk Factor and Clinical Risk Assessment revised to accept coded or plain text values
- **Discharge Details** - Encounter Type changed to Required
- **Early Years Progress** - Site Code, Professional Name and Professional Type changed to Required
- **Feeding Status** - Date and Time of First Milk Feed changed to Required; new item Approximate Date Breastfeeding Stopped added
- **Immunisation Administration** - Outcome Status and Dose Sequence changed to Optional
- **Individual Requirements** - Cognition item changed to Cognitive
- **Information and Advice Given** - Recipient changed to Required
- **Measurements** - Birth Weight changed to Required, updated to use generic profiles for HeadCircumference and Weight observations
- **Medication** - Course status, Dose directions description, Dose Direction Duration and Additional instruction changed to Optional
- **Newborn Hearing** - Procedure profiles for AABR and AOAE hearing tests and outcomes added:
	- [CareConnect-DCH-AABRHearingTest-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-AABRHearingTest-Procedure-1)
	- [CareConnect-DCH-AOAEHearingTest-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-AOAEHearingTest-Procedure-1)
- **Referral** - Specialty Referred From changed to Source Of Referral

**Changes following INTEROPen curation**

- **Birth Details** - Event remodelled to use [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1) and [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- **Event header** - [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1) - the terminology binding for 'type' will now use the [Care Connect Care Setting Type Value Set](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-CareSettingType-1).
- **Immunisation Administration** - Added FHIR profiles to support sharing of Information and Advice Given, and Allergies and Adverse Reactions 
- **Professional Contacts** - Event data item mapping clarified to detail team or care professional association requirements. The event has been redesigned as follows:
	- 'Specialty' data item removed
	- [CodeSystem DCH-ProfessionalType-1](https://fhir.nhs.uk/STU3/CodeSystem/DCH-ProfessionalType-1) updated to use new codes
	- **CareConnect-DCH-Team-Organization-1** profile removed and replaced with [DCH-CareTeam-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-CareTeam-1)
	- 'Role' changed to Required
	- 'Telephone number' changed to 'Contact details'

- The following Level 3 profiles have been removed and replaced with Level 2 CareConnect profiles:
	- **CareConnect-DCH-Organisation-1** replaced with CareConnect-Organization-1
	- **CareConnect-DCH-Location-1** replaced with CareConnect-Location-1

All example instances, and the **DCH-DSTU2-STU3-Map** provided in the [About](support_about.html) section have been updated to reflect these changes.

## Beta 1.0.1 ##
This implementation guidance has been updated to:
- include a guidance page for accessing example messages
- apply a correction to the title for Blood Spot Test Outcome event

## Beta 1.0.0 ##
This Beta release includes implementation guidance to support the development of the Digital Child Health Event Messages, supporting the following:

- the [Healthy Child Record Standard](https://theprsb.org/standards/healthychildrecord/)
- FHIR profiles developed using the [FHIR Release STU3](https://www.hl7.org/fhir/STU3/index.html) specification
- [SNOMED CT](https://digital.nhs.uk/snomed-ct) coding support where applicable
