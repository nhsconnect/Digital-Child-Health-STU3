---
title: Bundle Structure
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_bundle_structure.html
summary: "The structure of the bundle used for Digital Child Health (DCH) event messages"
---

{% include important.html content="This site is under active development by NHS Digital and is intended to provide the FHIR messaging components for the Digital Child Health Events Specification. This project is being developed using an agile methodology so iterative updates to content will be added on a regular basis. It is advised not to develop against these specifications until a formal announcement has been made." %}

## Background ##
To enable a standardised structure to carry information regarding event messages within the scope of the Digital Child Health Events specification, the Bundle and the Message Header  resources combine to make up the initial event message bundle. 

## The Digital Child Health Event Message Bundle Structure ##

The diagram below demonstrates the components needed to meet the initial DCH Event Message Bundle structure.

<img src="images/explore/dchbundlestructure.png" style="width:50%;max-width: 50%;">

**MessageHeader focus**

The root class of the MessageHeader is fulfilled using the 'focus' element in the resource. This will reference the Encounter resource depending on the following conditions for clinical events.









