---
title: Playing back LPA's data
description: |-
  The problem

  Initially, when the service was a tool which checked the quality of data, LPA’s did not have the means to see the data they had provided to the ...
date: '2025-02-28'
screenshots:
  items:
  - text: Initial dataset details designs from the design sprint
    src: 01-initial-dataset-details-designs-from-the-design-sprint.png
    alt: Page shows a map and a summary table of meta data
  - text: Current dataset details design
    src: 02-current-dataset-details-design.png
    alt: 'Page shows a map with the LPA boundary highlighted, metadata summary table
      and active endpoint data '
  - text: Dataset details release iterations
    src: 03-dataset-details-release-iterations.png
    alt: 'Two flow diagrams: the first shows a simple flat approach and the other
      shows how the dataset details page becomes a hub'
    caption: Original dataset details user journeys
  - text: Current dataset details user journey
    src: 04-current-dataset-details-user-journey.png
    alt: This flow diagram shows how the dataset details page is the hub with different
      flows starting from that point
    caption: Current dataset details user journey
tags: []
---

## The problem

Initially, when the service was a tool which checked the quality of data, LPA’s did not have the means to see the data they had provided to the platform. We wanted to focus more on playing data back to the LPA, rather than there being a focus on what was wrong with the data. 

## Our approach

In May 2024, we utilised a design sprint (an intensive process aimed at innovation, in which pages/features were designed and prototyped in five days). Since then we have introduced pages and features into the service which play data back, and iterated on these over time as below:

### Dataset details 

The first iteration of this played back geospatial data on a map and key information about the dataset. 

![Page shows a map and a summary table of meta data](https://design-history.ams3.digitaloceanspaces.com/yebf0wjij02c46usyztk3e5g0ifw)

### Introduction of dataset table and task list

We introduced a playback of each dataset an LPA has provided in a table so that users could see what their data looks like on the platform. 

The task list was improved by grouping issues to reduce the number of individual issues that is presented to users and therefore make it easier for LPAs to identify what needs to be done. 

### Improving the map

Insights from user testing have helped us to understand how users interact with the map. We have made the following improvements iteratively:

- introduced controls to allow users to open full screen and zoom
- changed the map base layer 
- introduced an LPA’s boundary outline to help them visualise when data is falling outside of this 

### Dataset navigation

A horizontal sub navigation menu sits along the top of the dataset page giving users different views of their data:

- an overview
- the data in a table
- task list showing what issues need fixing

On the overview page there is a dataset actions sub menu that lets users access the different actions they can perform on their data (read guidance, check and submit their data)

Original dataset details user journey:
![Two flow diagrams: the first shows a simple flat approach and the other shows how the dataset details page becomes a hub](https://design-history.ams3.digitaloceanspaces.com/fx3ua6qab5rzjpmigfs97t9qq0j9)

Current dataset details user journey:
![This flow diagram shows how the dataset details page is the hub with different flows starting from that point](https://design-history.ams3.digitaloceanspaces.com/j9g4r6akggfpk2gzdsha07smefcl)

## Our solution

The dataset details page has been iterated and improved, adding the The dataset details page has been iterated and improved, adding the map, dataset table, task list, and navigation options to provide a comprehensive playback of LPAs' data.

![Page shows a map with the LPA boundary highlighted, metadata summary table and active endpoint data ](https://design-history.ams3.digitaloceanspaces.com/1asyp5rk62pmg5xtdrpy0v3hln8a)

## Next steps

We plan to make further improvements to the dataset details page, including:

- playing back data from other sources that falls within an LPA’s boundary
- highlighting entities outside of the boundary
Improving the display of multiple endpoints


