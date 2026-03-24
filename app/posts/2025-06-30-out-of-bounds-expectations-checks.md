---
title: Out of bounds expectations checks
description: |-
  The problem

  To improve the quality of data on the platform, expectations checks are being added to identify issues with the information beyond the validity ...
date: '2025-06-30'
screenshots:
  items:
  - text: Design critique providers & data design
    src: 01-design-critique-providers-data-design.png
    alt: Wireframs of the out of bounds flow with post-its showing feedback
  - text: Dataset details – out of bounds
    src: 02-dataset-details-out-of-bounds.png
    alt: Figma mock up of dataset details page showing out of bounds entities
  - text: Dataset details — out of bounds prototype
    src: 03-dataset-details-out-of-bounds-prototype.png
    alt: Dataset details page showing out of bounds entities
  - text: Segmented tasklist
    src: 04-segmented-tasklist.png
    alt: Task list page with tasks separated out under different headings
tags: []
---

## The problem

To improve the quality of data on the platform, expectations checks are being added to identify issues with the information beyond the validity of the data.

The first of these to be implemented checks whether the entities in a dataset are within an LPA’s boundary.

Some LPA’s have used incorrect geospatial coordinates which results in entities appearing in the North Sea or far from the LPA’s geographical area.

There are some exceptions where LPAs may have legitimate reasons for entities to appear outside of their boundaries. For example, some LPAs have administrative responsibilities for conservation areas in neighbouring national parks.

## Our approach

We set out to look at how we could represent out of bounds entities in the provider service.

We needed to ensure that: 

- users are informed entities are outside their boundary.
- users are able to see the out of boundary records highlighted on the map
- users are able to view the out of boundary records in a table
- users are informed of how to fix the errors

## Our solution

Exploring this problem it made sense for this to fit within the established patterns for highlighting issues to users using the task list.

![Wireframs of the out of bounds flow with post-its showing feedback](/out-of-bounds-expectations-checks/01-design-critique-providers-data-design.png)

We designed some wireframes showing the proposed flow and presented them in a [design crit](https://app.mural.co/t/mhclg2837/m/mhclg2837/1729841459350/3c903499841bd18b161b2a1c8a7c778ac461c85b?wid=0-1738846628830) with other members of the team and stakeholders from the Data Managment team.

The feedback from this session was used to refine the designs.

![Figma mock up of dataset details page showing out of bounds entities](/out-of-bounds-expectations-checks/02-dataset-details-out-of-bounds.png)

As the designs used the existing flow we decided that this feature could be rolled out without testing, and we could gather feedback and usage metrics once it was in production.

We refined the design further, creating an [interactive prototype](https://provider-design.prototype.planning.data.gov.uk/out-of-bounds/organisations/local-authority:SNO/conservation-area/overview) to develop the map including using an accessible colour palette based on the [Local Plans policy map guidance](https://www.gov.uk/guidance/how-to-present-your-policies-map) and adding a legend.

![Dataset details page showing out of bounds entities](/out-of-bounds-expectations-checks/03-dataset-details-out-of-bounds-prototype.png)

We segmented the task list into 3 sections, based on the iterative check flow:

- **Issues you must fix:** These are pipeline issues that stop data from being added to the platform. Without valid data in these fields, the record cannot be processed. We call these ‘blocking issues’. When these occur, we have no information on the platform. This section should include HTTP errors.
- **Issues you should fix:** These are data validation errors found by the pipeline. The record can be processed, but the data returned by the API would not meet the specifications. For example, a date in the wrong format or text where a number is expected.
- **Improve the accuracy of your data:** This category is for expectation checks being added to the pipeline. Currently, this would show out-of-bounds issues.

![Task list page with tasks separated out under different headings](/out-of-bounds-expectations-checks/04-segmented-tasklist.png)

On the issue detail page we included some guidance on what to do if the entity is outside of the boundary for legitimate reasons.

At the moment this is a manual task of emailing the Data Management team as this would not happen very often.

## Next steps

- Implement the designs
- Gather feedback from users and observe whether users are able to correct any mistakes in their data
- Measure the change in out of bounds entities across the platform to see if this makes an improvement.


