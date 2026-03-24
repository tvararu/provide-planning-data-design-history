---
title: 'Provider service walkthrough: Part 2 — walkthrough'
description: Service walkthrough
date: '2025-07-09'
screenshots:
  items:
  - text: Provider prototype to be june 2025
    src: 01-provider-prototype-to-be-june-2025.png
    alt: A user journey map of the provider service showing how the pages are linked
tags: []
---

## Service walkthrough

![A user journey map of the provider service showing how the pages are linked](/provider-service-walkthrough-part-2-walkthrough/01-provider-prototype-to-be-june-2025.png)
[Link to full resolution image](/provider-service-walkthrough-part-2-walkthrough/01-provider-prototype-to-be-june-2025.png)

### [Landing page](https://provider-design.prototype.planning.data.gov.uk/walkthrough)

The landing page has been recently updated. It clearly describes what the service does. We have also tested an email authentication flow from this page.

---

### [Choose organisation](https://provider-design.prototype.planning.data.gov.uk/walkthrough/organisations)

This page lists organisations expected to provide data.

It uses a **filter pattern** from GOV.UK. This pattern is accessible. We could add synonyms to the filter, but user research has not shown this is needed yet.

The list of organisations need to be populated using the provision data in the database.

In England, a **Local Planning Authority (LPA)** is an organisation responsible for planning in an area. LPAs include some Local Authorities, National Park Authorities, and Development Corporations.

This page shows the current list of **active Local Planning Authorities** (311 organisations). It does this by filtering 'role-organisations' that have the 'local-planning-authority' role and no end-date.

---

### [LPA dashboard](https://provider-design.prototype.planning.data.gov.uk/walkthrough/organisations/local-authority:SNO)

This page is the homepage for LPAs. Users should check it to see which datasets they need to provide and which provided datasets need attention.

It aims to give users a clear idea of what to do next.

**Notification banner**

For time-sensitive datasets (currently only brownfield land), we show a notification banner if the dataset has not been updated in time.

* The banner appears 3 months before the deadline.
* The content changes if the dataset is overdue.
* We also send email notifications.

**Dashboard status call-outs**

These call-outs aim to give an overview of tasks. We need to check if these are the right things to show.

**Dataset list**

This pattern currently works for the small number of datasets. However, as the number of datasets grows, we will need to review it. One option is a table with filters.

Each dataset has:

* a title
* a status message
* a status tag

The status message tells the user what they need to do.

The tags currently have these states:

* **Not provided** – no data has been submitted.
* **Needs fixing** – there are validation issues or checks that need to be resolved.
* **Live** – the data has been submitted, and there are no validation issues or checks.
* **Error** – there is an HTTP error when trying to access the data.

**Next steps:**

* Test and improve the dashboard status call-outs.
* Update the dataset list pattern to handle more datasets.
* Use the data quality framework for tags to show if data is trustworthy and complete.

---

### [Dataset details](https://provider-design.prototype.planning.data.gov.uk/walkthrough/organisations/local-authority:SNO/conservation-area/overview)

This page acts as a dashboard for each dataset.

It should give users a clear understanding of their data on the platform. This includes where it came from, when it was last updated, and if they need to do anything.

It is the central point for all actions users can take on a dataset. These currently include: read guidance, check data, provide data and review alternative data.

**Map**

* The map should show data provided by the LPA.
* Alternative source data should appear on a separate layer.
* Out-of-bounds records provided by the LPA should appear on a separate layer.
* The map uses the OS Maps Light tiles as the base layer. This offers good contrast for layering shapes, a good level of detail with building boundaries, and familiar, official map styles.
* Map controls could look more like other GOV.UK elements.
* The map should follow the guidelines in our [map documentation](https://docs.google.com/presentation/d/1lOCgTRK7FDOwAVqSXuLRYiiRj0I_K2-oMeavQhr6lKc/edit?slide=id.gd56b1bae44_0_4#slide=id.gd56b1bae44_0_4).

**Map colours**

We chose colours based on [Local Plans policy map](https://www.gov.uk/guidance/how-to-present-your-policies-map#policy-categories) guidance. We also picked combinations that should provide enough contrast for colour blind users.

* In the prototype, colours are set by the order layers are added.
* We could explore assigning colours based on dataset categories.
* We are also looking at using hatching and other textures or patterns for different data layers or overlays.
* Map pop-ups should link to the record detail page.

**Map accessibility**

The map has not yet been tested for accessibility.

* Always provide a text alternative to the map (on this page, this is the dataset table).
* We need to implement keyboard controls for the map.

**Dataset sub-menu**

These menus provide different views of the dataset information:

* **Overview:** Shows the data on a map and extra information about the dataset. It includes links to actions like checking, providing, and reading guidance.
* **Dataset table:** A table view of the data that should link to individual record views.
* **Task list:** Validation and expectation issues that need to be resolved to improve data trustworthiness and accuracy.

**Dataset actions**

This is a menu of actions that can be performed on the dataset.

* It currently shows links to check, provide, and guidance.
* It could be expanded to include reviewing alternative data and other features later.
* We moved it to the left-hand side because users were not noticing it on the right.
* It could be redesigned to be more task-focused.

**Dataset details table**

This table aims to give an overview of the dataset's metadata.

It could be used to show when things are correct (for example, if a licence is missing).

**Active endpoints**

Endpoint metadata was moved out of the dataset details table to allow more space for multiple endpoints.

* Each endpoint has a documentation URL.
* It shows when the endpoint was last accessed and last updated, and if there are any HTTP errors.
* It could be used to flag when a documentation URL is not from an authoritative domain.
* The 'Edit' link was for managing endpoint data (updating URLs).
* The 'Retire' link would take the user to a confirmation screen to retire the endpoint.
* Neither link is implemented or has been tested.
* The current approach is that the data management team should clean up datasets with multiple endpoints.

**[Empty state](https://provider-design.prototype.planning.data.gov.uk/walkthrough/organisations/local-authority:SNO/listed-building-outline/overview)**

We recently tested designs that removed the 'get started' page content. We now need an alternative for when LPAs have not submitted any data.

* The empty state should show the map with the LPA boundary. It should also show any data from alternative sources.
* This page could also be more task-focused.

---

### [Dataset table](https://provider-design.prototype.planning.data.gov.uk/walkthrough/organisations/local-authority:SNO/conservation-area/table)

This page allows the user to view their data in a table.

* It should show the data as it appears on the platform or through the API — not how the user supplied it.
* Table headings should use the same column names and 'kebab-case' as the specifications.
* Columns should be in the same order as the specifications.
* The 'Reference' column should appear first and link to the record detail page.
* Long fields (like URLs or geometry) should be shortened. Users should have an option to expand the full data.

**Future considerations:**

* Should we show the map on this page?
* The scrollable table has not been accessibility tested.
* The page has not been designed to be responsive or for mobile use.
* We should show where data has been transformed (if technically possible).

---

### [Record detail](https://provider-design.prototype.planning.data.gov.uk/walkthrough/organisations/local-authority:SNO/conservation-area/detail/44006084)

This page is not yet implemented in the live service.

* It will show a map with the single record and the LPA boundary.
* It will show a summary card with the data from the platform.
* Column names and case should match the specification, not what the user supplied.
* The order of columns should be the same as the specification.
* Long fields (URLs, geometry, etc.) should be shortened. Users should have an option to expand the full data.

**Future considerations:**

* Should we show validation and expectation issues in this table?
* We should show where data has been transformed (if technically possible).

---

### [Task list](https://provider-design.prototype.planning.data.gov.uk/walkthrough/organisations/local-authority:SNO/conservation-area/tasklist)

The task list page lists validation issues found by the data pipeline.

It also shows any HTTP errors when trying to access the data.

Issue messages are stored in a specific file.

Tasks have tags showing different categories:

* **Needs fixing** – validation errors caught by the pipeline.
* **Error** – HTTP errors when trying to access the data.

In recent design work, we split the task list into 3 sections. This mimics our check tool:

* **Issues you must fix:** These are pipeline issues that stop data from being added to the platform. Without valid data in these fields, the record cannot be processed. We call these 'blocking issues'. When these occur, we have no information on the platform. This section should include HTTP errors.
* **Issues you should fix:** These are data validation errors found by the pipeline. The record can be processed, but the data returned by the API would not meet the specifications. For example, a date in the wrong format or text where a number is expected.
* **Improve the accuracy of your data:** This category is for expectation checks being added to the pipeline. Currently, this would show out-of-bounds issues.

---

### [Issue table](https://provider-design.prototype.planning.data.gov.uk/overview/v2/local-authority:LBH/dataset/listed-building-outline/error/3011ff5e9ed59166a3fa9bb1c33b453cf6478caaef39583d7ef4f47f116fea6f/reference%20values%20are%20not%20unique/table)

This view shows records with issues in a table. The problem field is highlighted.

* The error summary component should detail how many records are affected and the problem.
* The map should show the affected records.
* The 'Reference' field should link to the issue detail page.
* The table should follow the same pattern as the dataset table.
* The 'how to fix' section should explain the problem. It uses a snippet from the dataset guidance for help.

**Insights**

Research showed that some people could not find the issue in the table. The column with the issue should be moved to come after the 'Reference' column.

**Next steps:**

* We should remove the 'How to improve' snippet from this page.

---

### [Issue detail](https://provider-design.prototype.planning.data.gov.uk/overview/v2/local-authority:LBH/dataset/listed-building-outline/error/3011ff5e9ed59166a3fa9bb1c33b453cf6478caaef39583d7ef4f47f116fea6f/reference%20values%20are%20not%20unique)

This view shows an issue on a single record. It is similar to the record detail view.

* It will show a map with the single record and the LPA boundary.
* It will show a summary card with the data from the platform.
* Column names and case should match the specification, not what the user supplied.
* The order of columns should be the same as the specification.
* Long fields (URLs, geometry, etc.) should be shortened. Users should have an option to expand the full data.
* If data has been transformed, this should be flagged in the table.

## Related links

[Provider service walkthrough: Part 1](https://submit-planning-data.designhistory.app/provider-service-walkthrough-part-1-principles)
[Provider service walkthrough: Part 3](https://submit-planning-data.designhistory.app/provider-service-walkthrough-part-3-check-flow)

