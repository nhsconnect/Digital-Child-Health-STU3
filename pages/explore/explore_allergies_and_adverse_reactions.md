---
title: Allergies and Adverse Reactions Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_allergies_and_adverse_reactions.html
summary: "The FHIR profiles used for the Allergies and Adverse Reactions Event Message Bundle"
---
{% include custom/under.construction.html content="Please check back later for any updates to this page" %}

The following FHIR profiles are used to form the Allergies and Adverse Reactions Event Message Bundle:

- DCH-MessageHeader-1 - where the coding and display elements for the 'event' type are fixed to 'Allergies and Adverse Reactions'
- CareConnect-DCH-Organization-1
- CareConnect-DCH-Patient-1
- CareConnect-DCH-Encounter-1
- DCH-HealthcareService-1
- CareConnect-DCH-AllergyIntolerance-1
- DCH-AllergiesAndAdverseReactions-Flag-1
- CareConnect-DCH-Location-1

### Allergies and Drug Reactions event data item mapping to FHIR profiles ###
----------
The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:
                                                                                                   
| DCH Data Item               | FHIR resource element                                                                                   | Mandatory/Required/Optional |
|-----------------------------|---------------------------------------------------------------------------------------------------------|-----------------------------|
| Date                        | CareConnect-DCH-AllergyIntolerance-1.onset or CareConnect-DCH-AllergyIntolerance-1.reaction.onset       | Mandatory                   |
| Causative Agent             | CareConnect-DCH-AllergyIntolerance-1.reaction.substance                                                 | Mandatory                   |
| Description of Reaction     | CareConnect-DCH-AllergyIntolerance-1.reaction.manifestation.description                                 | Optional                    |
| Type Of Reaction            | DCH-AllergiesAndAdverseReactions-Flag-1.code                                                            | Optional                    |
| Certainty                   | CareConnect-DCH-AllergyIntolerance-1.reaction.allergyCertainty                                          | Optional                    |
| Severity                    | CareConnect-DCH-AllergyIntolerance-1.reaction.allergySeverity                                           | Optional                    |
| Evidence                    | CareConnect-DCH-AllergyIntolerance-1.evidence															| Optional                    |
| Probability of Recurrence   | CareConnect-DCH-AllergyIntolerance.probabilityOfRecurrence                                              | Optional                    |
| Date First Experienced      | CareConnect-DCH-AllergyIntolerance.onset                                                                | Optional                    |