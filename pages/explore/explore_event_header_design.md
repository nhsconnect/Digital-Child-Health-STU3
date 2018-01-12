---
title: Digital Child Health Event Header Design
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_event_header_design.html
summary: "The event header design for use with Digital Child Health (DCH) Event messages"
---

{% include important.html content="This site is under active development by NHS Digital and is intended to provide the FHIR messaging components for the Digital Child Health Events Specification. This project is being developed using an agile methodology so iterative updates to content will be added on a regular basis. It is advised not to develop against these specifications until a formal announcement has been made." %}

## Background ##
Each event will carry a standard set of data to act as an event "header" (to help identify the patient, publisher, and actual event).

## The DCH Event Header Design ##

This standard header consists of the following **mandatory** items and their corresponding FHIR profiles and elements:

| DCH Event Header item requirement      | FHIR resource               | FHIR element                                                                |
|----------------------------------------|-----------------------------|-----------------------------------------------------------------------------|
| patient identification data:           | CareConnect-DCH-Patient-1   |                                                                             |
| NHS Number                             | CareConnect-DCH-Patient-1   | identifier using NHS Number slice                                           |
| Date of Birth                          | CareConnect-DCH-Patient-1   | birthDate                                                                   |
| name                                   | CareConnect-DCH-Patient-1   | name                                                                        |
| event type                             | DCH-MessageHeader-1         | event                                                                       |
| type of service originating the event  | DCH-HealthcareService-1     | serviceType.type                                                            |
| service provider originating the event | CareConnect-DCH-Encounter-1 | serviceProvider                                                             |
| IT system holding the event data       | DCH-MessageHeader-1         | source                                                                      |
| location at which the event occurred   | CareConnect-DCH-Encounter-1 | location                                                                    |
| event date time                        | CareConnect-DCH-Encounter-1 | period.start                                                                |
| event publisher                        | DCH-MessageHeader-1         | responsible                                                                 |
| event published date                   | DCH-MessageHeader-1         | timestamp                                                                   |
| a publication reference number         | DCH-MessageHeader-1         | The resource identifier for the MessageHeader, which will use a UUID format |

The remaining resources in the bundle depend on the Digital Child Health Event, listed under the [Messages](/explore/explore.html) section for more information.









