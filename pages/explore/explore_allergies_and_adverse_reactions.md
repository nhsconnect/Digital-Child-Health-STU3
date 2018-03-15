---
title: Allergies and Adverse Reactions Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_allergies_and_adverse_reactions.html
summary: "The FHIR profiles used for the Allergies and Adverse Reactions Event Message Bundle"
---

{% include important.html content="The links below will refer to the StructureDefinition url applied to the FHIR profile, which are not yet active. For queries please refer to the Help and Support section." %} 

The following FHIR profiles are used to form the Allergies and Adverse Reactions Event Message Bundle:

- [DCH-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-Bundle-1)
- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display elements for the 'event' type are fixed to 'Allergies and Adverse Reactions'
- [CareConnect-DCH-Organization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-DCH-Location-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Location-1)
- [CareConnect-DCH-AllergyIntolerance-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-AllergyIntolerance-1)


### Allergies and Drug Reactions event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:
                                                                                                   
| DCH Data Item               | FHIR resource element                                                                                   | Mandatory/Required/Optional |
|-----------------------------|---------------------------------------------------------------------------------------------------------|-----------------------------|
| Date                        | CareConnect-DCH-AllergyIntolerance-1.assertedDate      | Mandatory                   |
| Causative Agent             | CareConnect-DCH-AllergyIntolerance-1.code                                                 | Mandatory                   |
| Description of Reaction     | CareConnect-DCH-AllergyIntolerance-1.reaction.manifestation.description or                                 | Optional                    |
| 	     | CareConnect-DCH-AllergyIntolerance-1.reaction.manifestation.coding                                 | Optional                    |
| Type Of Reaction            | CareConnect-DCH-AllergyIntolerance-1.type                                                            | Optional                    |
| Certainty                   | CareConnect-DCH-AllergyIntolerance-1.verificationStatus                                         | Optional                    |
| Severity                    | CareConnect-DCH-AllergyIntolerance-1.reaction.manifestation.severity                                          | Optional                    |
| Evidence                    | CareConnect-DCH-AllergyIntolerance-1.reaction.note															| Optional                    |
| Probability of Recurrence   | CareConnect-DCH-AllergyIntolerance.reaction.note                                              | Optional                    |
| Date First Experienced      | CareConnect-DCH-AllergyIntolerance.onset                                                                | Optional                    |