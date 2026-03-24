---
title: Improvements to service navigation
description: |-
  The problem

  Navigation was inconsistent across the provider’s service, dataset guidance and the rest of the planning data platform.

  There wasn’t a consiste...
date: '2024-11-07'
screenshots:
  items:
  - text: Service navigation
    src: 01-service-navigation.png
    alt: The page header using the service navigation component plus a flow diagram
      showing the relationship between guidance and the service
tags: []
---

## The problem

Navigation was inconsistent across the provider’s service, dataset guidance and the rest of the planning data platform.

There wasn’t a consistent way for users to navigate between dataset guidance and the provider service.

Additionally the [existing navigation patterns were being deprecated](https://github.com/alphagov/govuk-frontend/blob/v5.9.0/CHANGELOG.md#move-service-name-and-navigation-links-from-the-govuk-header-to-service-navigation-component) by the GOV.UK Design System and replaced with the [new service navigation component](https://design-system.service.gov.uk/components/service-navigation/).

## Our approach

Using the service navigation component we added links to the guidance that would be consistent across the whole provider service.

![The page header using the service navigation component plus a flow diagram showing the relationship between guidance and the service](/improving-service-navigation/01-service-navigation.png)

The lack of user authentication / identification means we have to use a generic “Find your organisation” menu item that links to the choose organisation page. If user authentication was added then a link to the LPA’s dashboard could be added to the service navigation.

The guidance pages are hosted on a different subdomain to the provider service and the change in navigation patterns could cause some confusion when users need to navigate between the two sites.

## Next steps

- Ensure navigation is consistent across the guidance and provider service



