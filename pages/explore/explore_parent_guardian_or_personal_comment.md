---
title: Parent, Guardian or Personal Comment Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_parent_guardian_or_personal_comment.html
summary: "The FHIR profiles used for the Parent, Guardian or Personal Comment Event Message Bundle"
---
{% include custom/under.construction.html content="Please check back later for any updates to this page" %}

The following FHIR profiles are used to form the Parent, Guardian or Personal Comment Event Message Bundle:

- DCH-MessageHeader-1 - where the coding and display elements for the 'event' type are fixed to  'Parent Guardian Or Personal Comment'
- CareConnect-DCH-Organization-1
- DCH-HealthcareService-1
- CareConnect-DCH-Patient-1
- CareConnect-DCH-Encounter-1
- DCH-ParentGuardianOrPersonalComment-Communication-1
- DCH-RelatedPerson-1
- CareConnect-DCH-Practitioner-1
- CareConnect-DCH-Location-1

### Parent, Guardian or Personal Comment event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item       | FHIR resource element                     | Mandatory/Required/Optional |
|---------------------|-------------------------------------------|-----------------------------|
| Date                | CareConnect-DCH-Encounter-1.period.start  | Required                    |
| Name                | CareConnect-DCH-Practitioner.name         | Required                    |
| Details             | DCH-ParentOrGuardianComment-Communication-1.payload.contentString | Required                    |
| Relationship Status | DCH-RelatedPerson-1.relationship          | Optional                    |



