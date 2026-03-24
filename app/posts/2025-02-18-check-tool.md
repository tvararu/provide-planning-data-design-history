---
title: Check tool
description: "The problem\n\nOur service not only allows users to submit their datasets,
  but users can also use it to check their data for any errors before submitting.
  \n\nWe..."
date: '2025-02-18'
screenshots:
  items:
  - text: 07a results blocking
    src: 01-07a-results-blocking.png
    alt: check tool results page
  - text: '08 issues table'
    src: 02-08-issues-table.png
    alt: check tool issue details
tags: []
---

## The problem

Our service not only allows users to submit their datasets, but users can also use it to check their data for any errors before submitting. 

We had iterated and improved the platform to better align with the needs of users and senior stakeholders of the programme, but found that the number of LPAs using  the Check tool didn’t match the number of LPAs submitting data to the service. This meant that the tool wasn’t creating enough value for LPAs to consider using it to assist in their process. Therefore, we needed to find ways to improve the tool to increase its value for users.

## Our approach

We engaged directly with users and stakeholders to identify focus areas to improve and add value to the service. We used a series of observation tools such as Smartlook and traditional research techniques to identify these focus areas. 

Our research highlighted pain points that users directly experienced when interacting with our platform, such as:

- confusing UX
- exhaustive details on error pages
- other pain points that increase the amount of time a user spends scrolling to access relevant information

[See the full list of research insights for more detail](https://docs.google.com/spreadsheets/d/1bGvflNF9pTR6E76sujmGwMFB24B8ZttAGEXtOIw5vxg/edit?gid=0#gid=0).

##&nbsp;Our solution

### Limited scope of datasets

**Problem:** LPAs have a vast amount of datasets to manage and maintain. To increase the likelihood of the service being used (and its usability), we needed to increase the range of datasets the service is able to review. For the service to increase value for senior stakeholders, we needed to ensure it can review all the mandated datasets.

**Solution:** We worked with senior management to review each mandatory dataset and identify mandatory fields for those datasets. This enabled our engineers to increase the volume of datasets that the tool could review and process. 

### Enable parity between internal and external tools

**Problem:** The Check tool is not used by internal stakeholders due to its limited functionality. This resulted in stakeholders relying on legacy tools, such as the Endpoint Checker. 

The Endpoint Checker was a tool that enabled the Data Management team to quickly review and assess data submitted by an LPA.

The teams found that the Endpoint Checker provided a holistic review of the data provided by an LPA compared to the Check tool. This also made it difficult for users as the Check tool did not highlight issues which the Endpoint Checker did, resulting in users and internal stakeholders being frustrated.

**Solution:** We worked alongside the Data Management and Infrastructure team to assess the differences between the Check tool, the Endpoint Checker and the Pipeline tool, which helped us identify what must be changed to support internal stakeholders.

[Take a look at the gap analysis](https://docs.google.com/spreadsheets/d/1fvkgwENMooojZVXLxMpNpr1fKqaPQVA8UiGOUvra-RU/edit?usp=sharing).

We used this insight to adjust the Check tool to ensure there was parody between internal and external tools, leading to the Data Management team resigning the legacy tool and using the Check tool when reviewing submitted data.

### Visualising outputs

**Problem:** Users found it difficult to verify if their data was accurate if reviewing it in tabular view, resulting in LPAs submitting data which was outside their LPAs boundaries. 

**Solution:** Enabling users to view a map that features the data they uploaded for review, so users can visually see if their data is accurate and within their boundary.

![check tool results page](/check-tool/01-07a-results-blocking.png)

### Assist users to identify issues with their data

**Problem:** Users of the service found it difficult to see and understand issues with the data while using the Check service. 

**Solution:** We made it easier for users to identify the issues with their data by highlighting in the tabular view where the issues were within their dataset and provided additional commentary to contextualize why this is an issue.

![check tool issue details](/check-tool/02-08-issues-table.png)

### Supporting users to submit their datasets incrementally 

**Problem:** Users want to be confident about the quality and accuracy of data before they can make data 'public', preventing them from submitting data.

**Solution:** We integrated a new data quality framework to encourage iterative submissions of data. We believe that some data is better than no data, so LPAs can partially submit accurate data to the platform. We made it easier to distinguish between blocking and non-blocking issues, to encourage more iterative provision of data. 

## Next steps

- Addressing tech debt related to [mandatory fields](https://github.com/digital-land/submit/issues/790)
- Integrating a submit form within the Check flow


