---
title: Professional Contacts Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_professional_contacts.html
summary: "The FHIR profiles used for the Professional Contacts Event Message Bundle"
---
There are two versions of the Professional Contacts Event Message Bundle.
- **Professional Contacts (Team) Event** records a child's contact with a Care Team
- **Professional Contacts (Professional) Event** records a child's contact with a Healthcare Professional

The following FHIR profiles are used to form the Professional Contacts Event Message Bundle:

- [DCH-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-Bundle-1)
- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display elements for the 'event' type are fixed to 'CH027 - Professional Contacts'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [DCH-ProfessionalContact-EpisodeOfCare-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-ProfessionalContact-EpisodeOfCare-1)

Then for Professional Contacts (Team) Event
- [DCH-CareTeam-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-CareTeam-1)

Or for Professional Contacts (Professional) Event
- [CareConnect-DCH-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Practitioner-1)
- [CareConnect-DCH-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PractitionerRole-1)

### Professional Contacts Event data item mapping to FHIR profiles ###

Depending on the association, the Child Health Event data items are fulfilled by elements within the FHIR resources listed below.

## Professional Contacts (Team) Event ##
                                                                                                   
| DCH Data Item                 | FHIR resource element                                                                            | Mandatory/Required/Optional |
|-------------------------------|--------------------------------------------------------------------------------------------------|-----------------------------|
| Organisation                  | CareConnect-Organization-1.identifier (ODS Code or ODS Site Code)                       | Mandatory                    |
| Team                          | DCH-CareTeam-1                                                              | Required                   |
| Role                          | DCH-CareTeam-1.participant.role                                      | Required                   |
| Care Professional Association | DCH-ProfessionalContact-EpisodeOfCare-1.type                                                                         | Mandatory                   |
| Contact details             | CareConnect-Organization-1.telecom                                                              | Required                    |
| Start date                    | DCH-ProfessionalContact-EpisodeOfCare-1.period.start                                                                 | Required                   |
| End date                      | DCH-ProfessionalContact-EpisodeOfCare-1.period.end                                                                   | Required                   |
| Reason                        | DCH-ProfessionalContact-EpisodeOfCare-1.reason                                                                   | Optional                   |

### Linkage Diagram ###

This Linkage diagram defines the required references that SHALL be made between resources within the DCH Professional Contacts (Team) Event Message bundle. It includes both Header and Payload resources (but omits the DCH-Bundle-1 wrapper).

<img src="images/explore/ProfessionalContacts1.png">

## Professional Contacts (Professional) Event ##  
                                                                                                
| DCH Data Item                 | FHIR resource element                                                                            | Mandatory/Required/Optional |
|-------------------------------|--------------------------------------------------------------------------------------------------|-----------------------------|
| Organisation                  | CareConnect-Organization-1.identifier (ODS Code or ODS Site Code)                       | Mandatory                    |
| Name                          | CareConnect-DCH-Practitioner-1.name                                                     | Required                    |
| Role                          | CareConnect-DCH-PractitionerRole-1.code (careProfessionalType)                          | Required                  |
| Specialty                     | CareConnect-DCH-PractitionerRole-1.specialty                                            | Optional |
| Key Worker                    | CareConnect-DCH-PractitionerRole-1.code (keyWorker)                                     | Optional |
| Care Professional Association | DCH-ProfessionalContact-EpisodeOfCare-1.type                                                                         | Mandatory                   |
| Contact details              | CareConnect-DCH-Practitioner-1.telecom                                                           | Required                    |
| Start date                    | DCH-ProfessionalContact-EpisodeOfCare-1.period.start                                                                 | Required                   |
| End date                      | DCH-ProfessionalContact-EpisodeOfCare-1.period.end                                                                   | Required                   |
| Reason                        | DCH-ProfessionalContact-EpisodeOfCare-1.reason                                                                   | Optional                   |

### Linkage Diagram ###

This Linkage diagram defines the required references that SHALL be made between resources within the DCH Professional Contacts (Professional) Event Message bundle. It includes both Header and Payload resources (but omits the DCH-Bundle-1 wrapper).

<img src="images/explore/ProfessionalContacts2.png">
