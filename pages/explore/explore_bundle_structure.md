---
title: Bundle Structure
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_bundle_structure.html
summary: "The structure of the bundle used for Digital Child Health (DCH) event messages"
---

{% include warning.html content="This **temporary** site is provided to assist with the development of the **Beta** Digital Child Health Events Specification and is being updated regularly. It is advised not to develop against these specifications until a formal announcement has been made. Note: The [current published Digital Child Health Events Specification](https://nhsconnect.github.io/Digital-Child-Health/Generated/Chapter.1.About/index.html) is the **Alpha** version published on the NHS Developers Network. " %}

## Background ##
To enable a standardised structure to carry information regarding event messages within the scope of the Digital Child Health Events specification, the Bundle and the Message Header resources combine to make up the initial event message bundle. 

## The Digital Child Health Event Message Bundle Structure ##

The diagram below demonstrates the components needed to meet the initial DCH Event Message Bundle structure.

<img src="images/explore/dchbundlestructure.png" style="width:50%;max-width: 50%;">

**MessageHeader focus**

The root class of the MessageHeader is fulfilled using the 'focus' element in the resource.For Digital Child Health events this will reference the Encounter resource.









