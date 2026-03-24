---
title: Handling multiple endpoints
description: |-
  The problem

  Some local planning authorities LPAs have multiple active endpoints for a single dataset. This is particularly common for LPAs that joined the p...
date: '2024-11-18'
screenshots:
  items:
  - text: Multiple endpoints design options
    src: 01-multiple-endpoints-design-options.png
    alt: Three designs of the dataset details page with different ways of showing
      endpoints
  - text: Multiple endpoints final design
    src: 02-multiple-endpoints-final-design.png
    alt: The dataset details page showing 4 active endpoints using the summary card
      pattern
tags: []
---

## The problem

Some local planning authorities (LPAs) have multiple active endpoints for a single dataset. This is particularly common for LPAs that joined the programme early and with brownfield land, as LPAs upload a new CSV each year.

It can be difficult for LPAs to manage their data with multiple endpoints, as it is not clear where the data is coming from.

There is also currently no way for LPAs to manage or retire endpoints without contacting the data management team.

## Our approach

Ideally, LPAs would have a single endpoint per dataset, but this is not currently the case.

They would also still need the functionality to edit or retire endpoints manually.

Initially, we explored different ways of presenting the data before choosing the summary card component from the design system.

This keeps each endpoint visually distinct and provides space for actions to edit endpoints.

It also allows space to highlight errors and issues with the endpoint data.

![Three designs of the dataset details page with different ways of showing endpoints](/handling-multiple-endpoints/01-multiple-endpoints-design-options.png)

## Our solution

The [preferred design solution](https://provider-design.prototype.planning.data.gov.uk/multiple-endpoints/organisations/local-authority:SNO/conservation-area/):

- uses the summary card component to display endpoint data
- shows endpoints in the order they were added to the platform, with the latest at the top
- has actions for LPAs to edit or retire endpoints
- allows errors with the endpoint data to be highlighted in the card

We haven't designed the edit or retire flows, but they should have the following features:

**Edit endpoint:**

- allow user to edit endpoint URL, webpage URL and licence
- editing endpoint would retire current endpoint and add a new one in the background
- follow GOV.UK patterns on checking answers and confirming changes

**Retire endpoint:**

- show a confirmation screen with a description of what would happen and a check box the user has to check before submitting

![The dataset details page showing 4 active endpoints using the summary card pattern](/handling-multiple-endpoints/02-multiple-endpoints-final-design.png)

## Next steps

- implement the designs
- test the edit and retire flows
- data management team to retire legacy inactive endpoints 
- implement data quality checks to ensure documentation URLs are on the authoritative domain and link to the correct dataset


