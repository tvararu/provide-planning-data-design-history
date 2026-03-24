---
title: Displaying data from alternative sources
description: |-
  The problem
  Not all data on the platform has been provided by LPAs: a variety of different sources are used for various datasets for example, Historic Englan...
date: '2025-05-29'
screenshots:
  items:
  - text: Alternative sources wireframes
    src: 01-alternative-sources-wireframes.png
    alt: Wireframes showing the alternative sources flow with feedback on sticky notes
  - text: Dataset details page showing alternative sources
    src: 02-dataset-details-page-showing-alternative-sources.png
  - text: Review alternative sources page
    src: 03-review-alternative-sources-page.png
  - text: Review single record page
    src: 04-review-single-record-page.png
tags: []
---

## The problem
Not all data on the platform has been provided by LPAs: a variety of different sources are used for various datasets (for example, Historic England has a dataset of all conservation areas in England).

We have also gathered some data from LPA’s websites manually.

We have a hypothesis that this data could be useful to some LPAs to help them seed their datasets.
It might also help them to highlight discrepancies with other data sources so that data can be corrected.

## Our approach

We started by designing a set of wireframes showing how data from alternative sources could be presented to users.

![Wireframes showing the alternative sources flow with feedback on sticky notes](https://design-history.ams3.digitaloceanspaces.com/mdiocwq1o1mm2krk1r8e3zgsqi19)

The designs include a flow for users to review each entity individually and build up a batch of records to download.

The designs were developed in Figma using feedback from stakeholders and colleagues from the design crit. These designs were then tested with users.

[Insights from the research](https://docs.google.com/presentation/d/1q0spAX4AFB2vAsrpSkmYqxpFcGL6FV4Qv-93kG8Nfgc/edit?slide=id.g27a5adb8929_0_485#slide=id.g27a5adb8929_0_485) revealed that the review flow could end up being cumbersome, especially on larger datasets and also that there was some confusion about what users were supposed to do with the alternative source data.

## The solution

The designs were iterated based on this feedback and developed into an [interactive prototype](https://provider-design.prototype.planning.data.gov.uk/alternative-sources/organisations/local-authority:SNO/conservation-area/overview).

![](https://design-history.ams3.digitaloceanspaces.com/92mzsa20z5wia71ok08hijbhc1kk)

The map was improved to add a list of records on the left which can be used to select elements on the map. The colours were updated to follow the [Local Plans policy maps](https://www.gov.uk/guidance/how-to-present-your-policies-map) guidance.

![](https://design-history.ams3.digitaloceanspaces.com/m2ju44hh4i1o5zy7y8ih7una5q2v)

The process to select which records to download was dropped, from the research we gathered this would be better done in LPA’s own systems, and would be adding duplicate functionality to the provider service and creating scope creep. Instead users have the option to download the full dataset and review the records in their own systems.

![](https://design-history.ams3.digitaloceanspaces.com/0fe6ftisge2fw8q4lflu8epb3fcx)

## Next steps

- Implement the designs
- Gather feedback and test with users that they are able to use the alternative source data
- Ensure there is a process for removing incorrect data from non-authoritative sources
- Make sure the map is usable for users with access needs


