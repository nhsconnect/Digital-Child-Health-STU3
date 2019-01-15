---
title: Messaging Architecture Overview
keywords:  messaging
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore.html
summary: "Overview of the Messaging Architecture section"
---

**NOTE: The publication of Digital Child Health event messages to the [National Events Management Service](http://developer.nhs.uk/apis/ems-beta) (NEMS) will rely on the successful implementation of support for each event by the NEMS. Currently only the following Digital Child Health events are within the scope of this implementation by the NEMS:**

- Admission Details
- Allergies and Adverse Reactions
- Birth Details
- Blood Spot Sample Taken
- Blood Spot Card Received
- Blood Spot Test Outcome
- Conditions/Diagnoses
- Discharge Details
- Emergency Care Attendance
- Vaccination Administration
- Individual Requirements
- Legal Information
- Measurements
- Medication
- Newborn Hearing
- Physical Examination
- Professional Contacts
- Safety Alerts 

**Message Patterns and Message Structure**

The [National Events Management Service](http://developer.nhs.uk/apis/ems-beta) is based on a Publish and Subscribe messaging pattern. The events are published to a national events hub, which also manages subscriptions to the published events.

**Events**

The event originator will construct an event message, as outlined in this implementation guide. Event messages will be sent into the Events Management Service hub using a simple [FHIR Event Publication API](http://developer.nhs.uk/apis/ems-beta/publication_publish.html).

Onward delivery to subscribers will initially be over MESH, although other delivery channels may be developed in future if there is a demand for them. For further information relating to MESH see [Message Exchange for Social Care and Health (MESH)](https://digital.nhs.uk/message-exchange-social-care-health).

**Events Diagram**

The diagram shows an example of an event message being published to the hub. The hub manages subscriptions to these publications (in accordance with the Hub Registration Authority):

<img src="images/overview/Events.png" style="width:80%;max-width: 80%;">

**Event message data item requirement notation**

Each event message will detail the information requirements applicable to each data item requirement, these are described as: 

**Mandatory:** should always be included in the electronic communication. Where there is no information then the message will contain appropriate coded text to identify this.   
**Required:** where information should be recorded (and communicated) if available.           
**Optional:** where local decisions can be made about whether or not to communicate the information 
