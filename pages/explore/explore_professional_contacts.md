---
title: Professional Contacts Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_professional_contacts.html
summary: "The FHIR profiles used for the Professional Contacts Event Message Bundle"
---
{% include custom/under.construction.html content="Please check back later for any updates to this page" %}

The following FHIR profiles are used to form the Professional Contacts Event Message Bundle:

- DCH-MessageHeader-1 - where the coding and display elements for the 'event' type are fixed to 'Professional Contacts'
- CareConnect-DCH-Organization-1
- DCH-HealthcareService-1
- CareConnect-DCH-Patient-1
- CareConnect-DCH-Encounter-1
- CareConnect-DCH-Practitioner-1
- CareConnect-DCH-Location-1
- CareConnect-DCH-Team-Organization-1
- CareConnect-DCH-Practitioner-1
- CareConnect-DCH-PractitioneRole-1
- DCH-ProfessionalContact-EpisodeOfCare-1

### Professional Contacts event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:
                                                                                                   
| DCH Data Item                 | FHIR resource element                                                                            | Mandatory/Required/Optional |
|-------------------------------|--------------------------------------------------------------------------------------------------|-----------------------------|
| Organisation                  | CareConnect-DCH-Team-Organisation-1.identifier (ODS Code or ODS Site Code)                       | Required                    |
| Team                          | CareConnect-DCH-Team-Organisation-1                                                              | Mandatory                   |
| Name                          | CareConnect-DCH-Practitioner-1.name                                                              | Required                    |
| Role                          | CareConnect-DCH-PractitionerRole-1.code (careProfessionalType)                                       | Mandatory                   |
|                               | or DCH-HealthcareService-1.serviceType.type                                                      | Mandatory                   |
| Care Professional Association | DCH-EpisodeOfCare-1.type                                                                         | Mandatory                   |
| Speciality                    | CareConnect-DCH-PractitioneRole-1.specialty 										               | Mandatory                   |
|                               | or DCH-HealthcareService-1.specialty			                                                   | Mandatory                   |
| Telephone Number              | CareConnect-DCH-Practitioner-1.telecom                                                           | Required                    |
|                               | or CareConnect-DCH-Team-Organization-1.telecom                                                   | Required                    |
| Start date                    | DCH-ProfessionalContact-EpisodeOfCare-1.period.start                                                                 | Mandatory                   |
| End date                      | DCH-ProfessionalContact-EpisodeOfCare-1.period.end                                                                   | Mandatory                   |