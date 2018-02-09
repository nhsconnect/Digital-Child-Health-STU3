---
title: Individual Requirements Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_individual_requirements.html
summary: "The FHIR profiles used for the Individual Requirements Event Message Bundle"
---

{% include important.html content="The links below will refer to the StructureDefinition url applied to the FHIR profile, which are not yet active. For queries please refer to the Help and Support section." %} 

The following FHIR profiles are used to form the Individual Requirements Event Message Bundle:

- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1.xml) - where the coding and display for the event element is fixed to 'Individual Requirements'
- [CareConnect-DCH-Organization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Organization-1.xml)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1.xml)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1.xml)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1.xml)
- [CareConnect-DCH-Location-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Location-1.xml)
- [DCH-IndividualRequirements-QuestionnaireResponse-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-IndividualRequirements-QuestionnaireResponse-1)


### Individual Requirements event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item                                                 | FHIR Resource element                                                    | Mandatory/Required/Optional |
|---------------------------------------------------------------|--------------------------------------------------------------------------|-----------------------------|
| GP Opt Out Indicator                                          | DCH-IndividualRequirements-QuestionnaireResponse-1.gPOptOutIndicator     | Required                    |
| Individual Needs Person Indicator                             | DCH-IndividualRequirements-QuestionnaireResponse-1.individualNeedsPersonIndicator | Required                   |
| Accessible Information - Communication Support                | DCH-IndividualRequirements-QuestionnaireResponse-1.communicationSupport                    | Required                    |
| Accessible Information - Requires Communication Professional  | DCH-IndividualRequirements-QuestionnaireResponse-1.communicationProfessional               | Required                    |
| Accessible Information - Requires Specific Contact Method     | DCH-IndividualRequirements-QuestionnaireResponse-1.specificContactMethod                           | Required                    |
| Accessible Information - Requires specific information format | DCH-IndividualRequirements-QuestionnaireResponse-1.specificInformationFormat                       | Required                    |
| Mobility Needs                                                | DCH-IndividualRequirements-QuestionnaireResponse-1.mobilityNeeds                         | Required                    |
| Cognition                                                     | DCH-IndividualRequirements-QuestionnaireResponse-1.cognition                        | Required                    |