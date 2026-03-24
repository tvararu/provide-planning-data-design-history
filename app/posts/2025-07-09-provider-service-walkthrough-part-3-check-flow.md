---
title: 'Provider service walkthrough: Part 3 — check flow'
description: |-
  The check flow is launched from the dataset details page.

  There has been feedback that users want a more immediate way to access this page, so a stand along...
date: '2025-07-09'
tags: []
---

The check flow is launched from the dataset details page.

There has been feedback that users want a more immediate way to access this page, so a stand along check flow could be provided but this could mean users miss out on the benefits on seeing their progress on the LPA dashboard and dataset details pages.

The check flow has been recently redesigned to encourage more iterative provision of data. Previously users were waiting until their data was complete before uploading it, however it is beneficial to the platform and end users and to LPAs to provide their data as they gather and prepare it.

It gives the platform more coverage and LPAs can get feedback on what they need to do improve their data.

**Future considerations**

Users have expressed concern about publishing unfinished or incomplete data. This may also have an effect on end consumers and some of the outcomes of the consumers discovery (currently ongoing) is that end users are also concerned about the quality, completeness and trustworthiness of the data.

A way to mitigate this could be to allow users to confirm when their data is ready to be made public or to flag incomplete data on the consumer end.

A future consideration could be to log details of each time a dataset is checked and play this back to the user on the dataset details page so they know their data is up to date.

### [Choose method](https://provider-design.prototype.planning.data.gov.uk/iterative-check/organisations/local-authority:SNO/conservation-area/choose-upload)

Users have two choices on how to check their data, either by uploading a file or providing an endpoint URL. The file upload is beneficial because users can check their data before they have published it on their open data platform.

### [Upload data / Endpoint details](https://provider-design.prototype.planning.data.gov.uk/iterative-check/organisations/local-authority:SNO/conservation-area/upload-data)

Both these pages have tested well without any major issues. 

When the data is uploaded or the URL is submitted there is an asynchronous processing step. 

We may want to add something to notify users that their data is being processed if this is taking a long time or a way to catch errors if there is a problem.

### [Results page](https://provider-design.prototype.planning.data.gov.uk/iterative-check/organisations/local-authority:SNO/conservation-area/results)

The results have been split into three sections:

**Data that passed checks**
This is to give the user positive reinforcement about their data rather than chastasing them about errors.

**Issues you must fix**
This section highlights issues that mean the data cannot be processed. This includes missing specific fields like reference or geometry.

**Issues you should fix**
This section shows issues that affect the quality of the data. These can include missing supplementary fields and validiity errors. The check tool currently doesn’t process any expectation checks as these need to compared with data on the platform

If there are blocking issues that must be fixed the only way forward is to upload a new version.

If there are [no blocking issues](https://provider-design.prototype.planning.data.gov.uk/iterative-check/organisations/local-authority:SNO/conservation-area/results-non-blocked) users can continue to the next page to review their data and follow through to provide their data.

### [Issue table](https://provider-design.prototype.planning.data.gov.uk/iterative-check/organisations/local-authority:SNO/conservation-area/issue-non-blocking)

This page follows the same pattern we are using to show issues in the dashboard.

In the check flow the data should be played back in the format the user provided it, not as it would appear after being transformed on the platform.

It includes a snippet of contextual guidance so users know how to resolve the issue.

### [Review data](https://provider-design.prototype.planning.data.gov.uk/iterative-check/organisations/local-authority:SNO/conservation-area/check-data)

This page plays back the data on a map and in a table for users to review before continuing to the confirmation page.

### [Confirmation page](https://provider-design.prototype.planning.data.gov.uk/iterative-check/organisations/local-authority:SNO/conservation-area/confirmation)

This page follows the standard GOV.UK confirmation page pattern.

The user is given clear guidance their next steps:  publishing their data on their LPA website and submitting their data to the planning data platform.

There is a large call to action to take users directly to the provide flow.


## Related links

[Provider service walkthrough: Part 1](https://submit-planning-data.designhistory.app/provider-service-walkthrough-part-1-principles)
[Provider service walkthrough: Part 2](https://submit-planning-data.designhistory.app/provider-service-walkthrough-part-2-walkthrough)

