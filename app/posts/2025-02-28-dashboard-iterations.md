---
title: Dashboard iterations
description: |-
  The problem

  Initially, the service was a tool which checked LPAs’ data. They had no way of understanding the landscape of data they were providing to the Pl...
date: '2025-02-28'
screenshots:
  items:
  - text: Inital dashboard design
    src: 01-inital-dashboard-design.png
    alt: LPA dashboard as a grid
  - text: LPA dashboard tasklist design
    src: 02-lpa-dashboard-tasklist-design.png
    alt: LPA dashboard using task list pattern
  - text: LPA dashboard tasklist segmented
    src: 04-lpa-dashboard-tasklist-segmented.png
    alt: LPA dashboard showing segmented dataset list
tags: []
---

## The problem

Initially, the service was a tool which checked LPAs’ data. They had no way of understanding the landscape of data they were providing to the Planning Data Platform. When we were building the service into an end-to-end service, we needed to design and build a feature which allowed us to play back the status of datasets to LPAs. After careful consideration, we decided to introduce a dashboard.  

## Our approach

We began building the dashboard into the service following a design sprint in May 2024. Since then, we have iterated on these designs based on user needs surfaced in user research, understanding user groups and by a mandated dataset (brownfield land) being introduced into the service. 

The initial design shown below displayed a status for the 8 datasets required by LPAs engaged in Open Digital Planning (ODP). At this point, we introduced colours to the dashboard to help users prioritise actions. Our approach to colour has remained present in further iterations of the dashboard. We also included a link for the users to access their task list in order to address any issues in their datasets. 

![LPA dashboard as a grid](/dashboard-iterations/01-inital-dashboard-design.png)

We initially iterated on the design in many ways including:

- the layout becoming more of a list format with tags 
- using clearer language to describe the status of datasets 

![LPA dashboard using task list pattern](/dashboard-iterations/02-lpa-dashboard-tasklist-design.png)

## Our solution

Further considerations and iterations have been made to the dashboard design including:

- iterating on the language we have used to describe the status of datasets. We did this as we observed that users were finding the difference between ‘issues’ and ‘errors’ confusing
- segmenting the dashboard to make the onward journey clearer to different user groups. For example organisations may just be required to provide the only current mandated dataset (brownfield land), they may be part of ODP and therefore be required to provide an additional 8 datasets
- adding a segment which allows users to understand the landscape of their data provision at a quick glance (the blue boxes in the image below)
- changing the user journey so that selecting each dataset will take a user to a dataset details and task list specific to that dataset

![LPA dashboard showing segmented dataset list](/dashboard-iterations/04-lpa-dashboard-tasklist-segmented.png)

## Next steps

We will continue to carry out user research to understand how users interact with this page and consider how this changes as more datasets are added to the service. 


