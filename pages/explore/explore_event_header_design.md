---
title: Digital Child Health Event Header Design
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_event_header_design.html
summary: "The design approach applied to support the standard event header information applicable to Digital Child Health (DCH)"
---

{% include warning.html content="This **temporary** site is provided to assist with the development of the **Beta** Digital Child Health Events Specification and is being updated regularly. It is advised not to develop against these specifications until a formal announcement has been made. Note: The [current published Digital Child Health Events Specification](https://nhsconnect.github.io/Digital-Child-Health/Generated/Chapter.1.About/index.html) is the **Alpha** version published on the NHS Developers Network. " %}

## Event header information for Digital Child Health ##
Each event message will carry a standard set of event header information to help identify the patient, publisher, and actual event, etc.

This event header information must consist of the following **mandatory** items and their corresponding FHIR profiles and elements:

| DCH Event Header item requirement      | FHIR resource               | FHIR element                                                                |
|----------------------------------------|-----------------------------|-----------------------------------------------------------------------------|
| patient identification data:           | CareConnect-DCH-Patient-1   |                                                                             |
| NHS Number                             | CareConnect-DCH-Patient-1   | identifier using NHS Number slice                                           |
| Date of Birth                          | CareConnect-DCH-Patient-1   | birthDate                                                                   |
| name                                   | CareConnect-DCH-Patient-1   | name                                                                        |
| event type                             | DCH-MessageHeader-1         | event                                                                       |
| type of service originating the event  | DCH-HealthcareService-1     | type 			                                                             |
| service provider originating the event | CareConnect-DCH-Encounter-1 | serviceProvider                                                             |
| IT system holding the event data       | DCH-MessageHeader-1         | source                                                                      |
| location at which the event occurred   | CareConnect-DCH-Location-1 | location                                                                    |
| event date time                        | CareConnect-DCH-Encounter-1 | period.start                                                                |
| event publisher                        | DCH-MessageHeader-1         | responsible                                                                 |
| event published date                   | DCH-MessageHeader-1         | timestamp                                                                   |
| a publication reference number         | DCH-MessageHeader-1         | The resource identifier for the MessageHeader, which will use a UUID format |

The remaining resources in the bundle depend on the Digital Child Health Event, listed under the [Messages](explore.html) section for more information.









