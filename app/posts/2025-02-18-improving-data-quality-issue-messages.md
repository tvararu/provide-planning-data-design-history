---
title: Improving data quality issue messages
description: |-
  The problem

  Our core mission as a service is to encourage and support Local Planning Authorities in providing trustworthy and high quality planning and hous...
date: '2025-02-18'
screenshots:
  items:
  - text: Screenshot 2025 02 17 at 11.42.00
    src: 01-screenshot-2025-02-17-at-11.42.00.png
    caption: Examples of messages received from users requesting advice following
      becoming aware of issues in their datasets.
  - text: Screenshot 2025 02 18 at 10.28.08
    src: 02-screenshot-2025-02-18-at-10.28.08.png
    caption: Screen shot of Mural to show mapping of error messages.
  - text: Screenshot 2025 02 18 at 10.25.28
    src: 03-screenshot-2025-02-18-at-10.25.28.png
    caption: Severities in Datasette
  - text: Screenshot 2025 02 18 at 10.50.21
    src: 04-screenshot-2025-02-18-at-10.50.21.png
    caption: 'A section of the Mural board which illustrates the links between datasets,
      data types and description of what we are expecting in each field. '
  - text: Screenshot 2025 02 18 at 10.51.09
    src: 05-screenshot-2025-02-18-at-10.51.09.png
    caption: 'A screenshot of the completed spreadsheet which will be used to build
      new issues messages into the service. '
tags: []
---

## The problem

Our core mission as a service is to encourage and support Local Planning Authorities in providing trustworthy and high quality planning and housing data. If the data they provide doesn't meet the requirements set out in the specifications, then the service provides feedback to them, highlighting data quality issues that they will need to address.

Feedback and insights from user research has highlighted that issue messages were not always clear to users and did not point them towards the action required to address data quality issues. We also know this from emails we receive and messages from LPAs in the #group-data-support Slack channel. For example the use of ‘{column_name} must have valid coordinates’ and ‘{column_name} must be above the minimum number needed’. In these instances, it is not clear what format of coordinates are required, or what the minimum number that can be provided is. 

![](https://design-history.ams3.digitaloceanspaces.com/56leas2ejq9e6skm17cyloz02t4l)

## Our approach

[In a workshop we mapped out where issue messages are seen by users in the service.](https://app.mural.co/t/mhclg2837/m/mhclg2837/1728654025264/16e0efd10d44506f2e66e5b02de469a99692b024?wid=0-1732701363269)

![](https://design-history.ams3.digitaloceanspaces.com/1t9l7bfvkw1ox7bibtcu9yq7ma1d)

We then reviewed the content, and began recording issue types, severity of the issue message, the dataset it relates to along with which fields and datatypes it affects in a spreadsheet. 

[Severities are found in Datasette.](https://datasette.planning.data.gov.uk/digital-land/severity) ‘Errors’ are the most important ones for this piece of work, as they’re ‘external’ errors which means users must act on them to fix them. 

![](https://design-history.ams3.digitaloceanspaces.com/zlkandgkyar69cpv2cuje5nm44p3)

This was with the aim of helping us to create new issue messages which are more descriptive of the action needed. To collate this information we used several tables which are held in Datasette. This work was complex and challenging to follow all of the relationships between the columns in a spreadsheet. 

We moved our thinking and mapping from Google Sheets [into a Mural board to allow us to connect datasets with data types more freely] (https://app.mural.co/t/mhclg2837/m/mhclg2837/1734011169645/8bf106fe41725b7b68b8efe71908a075061f9972). We discussed that we wanted the issue messages to be more descriptive, however as some error messages can be related to datasets which may have slightly different requirements, we could not make them completely individualised due to how they are categorised in data management processes. We then collaborated with data management to pair write the new versions of the issue messages. [These have now been transferred back into an amended spreadsheet for easier access when integrating into the service](https://docs.google.com/spreadsheets/d/1Nvr2Hl4RAw_81ggE2V09d4MCR1j7tsxGY-Vy-JeIYX0/edit?gid=1329820769#gid=1329820769). 

![](https://design-history.ams3.digitaloceanspaces.com/g4dk8aw5yhk1gq56aee8dknvaca8)

![](https://design-history.ams3.digitaloceanspaces.com/f8k41py25e6xjlz4t7tkcbffj8vt)

This process surfaced some other content inconsistencies within the guidance. These were recorded to be actioned as part of a wider guidance content review. 

## Our solution

Working with the data management team, we took each message and focused on how we could give the user more of a steer into how they should fix the issue. For example, “{column name} must have valid coordinates” does not give the user any indication of what we mean by valid coordinates. Instead, we can say, “{column name} must use the WGS84 or ETRS89 coordinate systems”. 

We hope that the messages now include more information to users about how to fix their issues, and we will look to show them to users in upcoming research sessions.

## Next steps

The wider team is meeting to discuss storage of new issue messages and how to integrate them into the service. We will also continue to conduct user testing across the service to ensure that the content resonates with users. 

The wider user centred design team are also working on improving guidance across the service. The inconsistencies that surfaced will be shared in this process. 



