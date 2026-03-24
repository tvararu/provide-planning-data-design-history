---
title: Using email reminders to help users fix their data
description: |-
  The problem

  Up until recently, users were not automatically notified about the status of their data unless they accessed the service to check their dashboar...
date: '2025-02-20'
tags: []
---

## The problem

Up until recently, users were not automatically notified about the status of their data unless they accessed the service to check their dashboard. 

Our aim was to let users know about the status of their data via email, to encourage them to access the service and fix their errors.

## Our approach

We piloted an email with 4 LPAs in total [(see more information about the pilot work)](https://docs.google.com/document/d/1eFYaBbhmIP5IOnZ4nYGeaGIu0Mq16xCcHVJ-Kxg3ZAU/edit?tab=t.0#heading=h.584b8se776s7), who all received the following email:

>Hello,

>We wanted to give you an update on the status of your data on the Planning Data platform. 

>As of 11/10/2024, this is what your data looks like:

>✅ Article 4 Direction Area

>✅ Conservation Area

>❌ Article 4 Direction

>❌Fields have reference values that are not unique

>View more using your dashboard: ((dashboard link)) 

>**((Link to change the recipient of this message))**

>As the main point of contact, you are currently listed to receive  all project-related updates. If there are other members of your team who should also receive this information, please use this form to let us know.

 >**Addressing your questions**

>If you have any questions or concerns about any data-related issue, please sign up to attend a Data Drop-In session.

>**Submit and update service**

>We have improved our service to help you in developing and publishing datasets. The service includes a dashboard for your LPA that enables you to monitor submitted and outstanding datasets, highlighting any that need your attention. Additionally, the service allows you to check your data and identify areas for improvement, making sure they meet data standards before submission.

>**Pausing service messages**

>Please use this form to let us know  the date you expect to be able to solve the data quality issues we’ve shown in your dashboard. Service messages will be paused until that date.

>Thanks,

>Planning Data Team


There is an entire [Google Slides presentation to highlight the feedback from LPAs](https://docs.google.com/presentation/d/1BeHBJCh2x81T8Tj1_QIbrn4XUS2VdTw8V0hGCioc9Pc/edit#slide=id.g2eff037075c_1_152), but in summary:

* all 4 LPAs either took action to address data quality issues, or visited their dashboard via the link in the email
* all 4 LPAs said the email included enough information to prompt intended actions and highlighted key areas to focus on
* the inclusion of easily understood symbols (✅❌) helped LPAs understand what to focus on
the majority of the issues raised in the email were actionable

However:

* without context, the ‘from’ email address did not make sense (DigitalLandTeam@communities.gov.uk)
* the subject line of the email did not provide enough useful context (Status of your data - 16/09/2024)

## Our solution

Our next iteration of the email focused on addressing the points above, and incorporating content design best practice [(including ‘Planning and writing text messages and emails’ on GOV.UK)](https://www.gov.uk/service-manual/design/sending-emails-and-text-messages). 

We also agreed to remove the use of emojis, as these weren’t accessible, but instead used clear headings. 

This time, we also sent the email manually via GOV.UK Notify, to more users than the original 4 pilot LPAs:

>Subject: An update about your planning data

>Dear ((LPA)),

>Here’s an overview of the data you’ve submitted to the Planning Data platform as of Monday 2 December.

>((live data))

>((data with errors to fix))

>View your dashboard to fix your errors: ((UTM link)). 

>This helps keep data accurate and up to date.

>You can use the guidance to help you: https://www.planning.data.gov.uk/guidance/

>If you need further support, email us at DigitalLand@communities.gov.uk

>Thank you for helping to standardise planning data.

>Regards,

>Michael-Jordan Faucher-Folie on behalf of Digital Land, MHCLG

---
>You’re listed as the main point of contact. To change this, or unsubscribe from updates about your data, let us know: ((form link))

>You can also pause these emails by telling us when you expect to resolve any errors with your data: ((form link))

>Sign up to our regular data drop in sessions to ask questions about your data and get support from our data management team: ((form link))

>((Unsubscribe link))


We sent the email to 420 recipients in total. Out of those, 51 emails bounced. 

9 LPAs out of 25 LPAs with data issues to fix, fixed at least 1 issue.

In total, out of the 60% of recipients who received the email, 36% acted on it and fixed errors with their data. 

## Next steps

Currently, sending this email via GOV.UK Notify is a fiddly, manual process. [We’re exploring how we can automate this process, and have a ticket in flight to document this](https://github.com/digital-land/submit/issues/647).




