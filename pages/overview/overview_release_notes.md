---
title: Release Notes
keywords: development, versioning
tags: [development]
sidebar: overview_sidebar
permalink: overview_release_notes.html
summary: Summary release notes of the versions released in Digital Child Health Implementation Guide
---

This site is under active development by NHS Digital and is intended to provide the FHIR messaging components for the Digtal Child Health event messages. This project is being developed using an agile methodology so iterative updates to content will be added on a regular basis, and remains subject to clinical review. Changes to this specification following the initial beta release will be documented here.

## Beta 2.0.0 ##
Following stakeholder feedback, this implementation guidance has been updated as follows:

- **Admission Details** - Patient Location clarified to use CareConnect-DCH-Location-1.type.text
- **Birth Details** - Location of Birth changed to Required
- **Blood Spot Card Received** - All items changed to Mandatory
- **Conditions** - Added item Condition end date
- **Discharge Details** - Encounter Type changed to Required
- **Early Years Progress** - Site Code, Professional Name and Professional Type changed to Required
- **Feeding Status** - Date and Time of First Milk Feed changed to Required; new item Approximate Date Breastfeeding Stopped added
- **Immunisation Administration** - Outcome Status and Dose Sequence changed to Optional
- **Individual Requirements** - Cognition item changed to Cognitive
- **Information and Advice Given** - Recipient changed to Required
- **Measurements** - Birth Weight changed to Required
- **Medication** - Course status, Dose directions description, Dose Direction Duration and Additional instruction changed to Optional
- **Referral** - Specialty Referred From changed to Source Of Referral

The **DCH-DSTU2-STU3-Map** provided in the [About](support_about.html) section has been updated to reflect these changes.

FHIR Profile updates:

- [CareConnect-DCH-ASQ3AssessmentScale-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-ASQ3AssessmentScale-Observation-1) - upversioned to 1.1.0
	- 'component' is now 1..*
- [CareConnect-DCH-ASQSE-AssessmentScale-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-ASQSE-AssessmentScale-Observation-1) - upversioned to 1.1.0
	- 'component' is now 1..*
- [CareConnect-DCH-BirthWeight-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-BirthWeight-Observation-1) - upversioned to 2.0.0
	- 'performer' referenced to 'CareConnect-DCH-Practitioner-1'
- [DCH-EarlyYearsProgress-QuestionnaireResponse-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-EarlyYearsProgress-QuestionnaireResponse-1) - upversioned to 2.0.0:
	- code, system and display elements for question 'parentalConsent' changed to 1..1
- [DCH-FeedingStatus-QuestionnaireResponse-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-FeedingStatus-QuestionnaireResponse-1) - upversioned to 2.0.0:
	- added item 'approximateDateBreastfeedingStopped'
- [DCH-IndividualRequirements-QuestionnaireResponse-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-IndividualRequirements-QuestionnaireResponse-1) - upversioned to 2.0.0
	- item 'cognition' renamed to 'cognitive'
- [DCH-Bundle-1] - upversioned to 2.0.0
	- type element uses fixed value 'message'
	- entry.fullUrl is now 1..1
	- entry.resource is now 1..1
	- entry.search is now 0..0
	- entry.request is now 0..0
	- entry.response is now 0..0 
- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - upversioned to 2.0.0: 
	- 'DCH-MessageHeader-1.id' is now 1..1
	- 'DCH-MessageHeader-1.responsible.reference' is now 1..1
- [DCH-NewbornBloodSpotScreening-Specimen-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-NewbornBloodSpotScreening-Specimen-1) - upversioned to 2.0.0
	- 'receivedTime' is now 1..1
	- code, system and display elements for all questions changed to 1..1
- [Extension-DCH-MessageEventType-1](https://fhir.nhs.uk/STU3/StructureDefinition/Extension-DCH-MessageEventType-1) - upversioned to 2.0.0:
	- 'Extension.valueCodeableConcept:valueCodeableConcept.coding.system' is now 1..1
	- 'Extension.valueCodeableConcept:valueCodeableConcept.coding.code' is now 1..1
	- 'Extension.valueCodeableConcept:valueCodeableConcept.coding.display' is now 1..1


## Beta 1.0.1 ##
This implementation guidance has been updated to:
- include a guidance page for accessing example messages
- apply a correction to the title for Blood Spot Test Outcome event

## Beta 1.0.0 ##
This Beta release includes implementation guidance to support the development of the Digital Child Health Event Messages, supporting the following:

- the [Healthy Child Record Standard](https://theprsb.org/standards/healthychildrecord/)
- FHIR profiles developed using the [FHIR Release STU3](https://www.hl7.org/fhir/STU3/index.html) specification
- [SNOMED CT](https://digital.nhs.uk/snomed-ct) coding support where applicable
