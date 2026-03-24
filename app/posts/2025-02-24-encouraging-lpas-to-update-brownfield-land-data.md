---
title: Encouraging LPAs to update brownfield land data
description: "The problem\n\nBrownfield land BfL is land which has previously been
  developed upon. \n\nThe Town and County Planning Brownfield Land Register Register
  2017 requ..."
date: '2025-02-24'
screenshots:
  items:
  - text: Screenshot 2025-02-24 at 15.29.51
    src: 01-screenshot-2025-02-24-at-15.29.51.png
  - text: Screenshot 2025-02-24 at 15.33.08
    src: 02-screenshot-2025-02-24-at-15.33.08.png
  - text: Screenshot 2025-02-24 at 14.30.37
    src: 03-screenshot-2025-02-24-at-14.30.37.png
tags: []
---

## The problem

Brownfield land (BfL) is land which has previously been developed upon. 

The Town and County Planning (Brownfield Land Register) Register 2017 requires LPAs to maintain a register of their brownfield land which are suitable for housing development.

Historically, the Planning Data Service receives around 45 BfL submissions per year. 

The submissions would also feature a large number of data quality issues. We were tasked to address this by:

* expanding the range of datasets LPAs can submit via the service
* encouraging LPAs to use the service to check their data before submitting
* ensuring that 40% of all LPAs have submitted their brownfield land data through the service

## Our approach

The team devised a plan that included informing LPAs of the need to:

* check their data
* submit their data 

We identified fields within the BfL dataset that LPAs must provide, versus fields which they should provide. [Those fields can be viewed in the GitHub ticket for this piece of work](https://github.com/orgs/digital-land/projects/7/views/36?filterQuery=-status%3ATech-debt%2CBugs%2CRefined%2C%22Eng+sprint+backlog%22%2C%22In+Development%22%2C%22Code+review+%26+QA%22%2C%22Ready+for+release%22%2CDone%2CEPICs++fields&amp;pane=issue&amp;itemId=82918074&amp;issue=digital-land%7Csubmit%7C541).

This approach ensured that the feedback provided to LPAs would not undermine or mislead data providers on their statutory duty. 

The team's engineers used these requirements when enabling the check tool to review BfL datasets.

### Notifying LPAs

We devised a way to identify which LPAs were required to submit BfL data for the register year [by creating an SQL query](https://datasette.planning.data.gov.uk/digital-land?sql=SELECT%0D%0A*%0D%0AFROM+%0D%0A++++++reporting_latest_endpoints+rle%0D%0AWHERE%0D%0A++++++organisation+LIKE+%27local-authority%3A%25%27%0D%0AAND+%0D%0A++++++rle.pipeline+%3D+%27brownfield-land%27%3B). This resulted in Datasette displaying a number of LPAs who are yet to update their endpoint nor submit a new one for the register year. 

[View the Github ticket for this piece of work.](https://github.com/digital-land/submit/issues/616)

We reached out to the LPAs directly to notify them via email of the need to submit BfL data to the service. 

We secured 70 of the required 283 email addresses via the community management team’s CRM system and the rest via Google. We used GOV UK Notify to send the emails and the links featured in the email included a UTM code, which allowed us to track user engagement with the emails and the service itself.

### Tracking engagement

To track the impact of our approach, we utilised Smartlook to track and review interactions with the platform via the UTM code. We did find instances where LPAs were interacting with the service without clicking the UTM link, but overall, it gave us a good indication as to the volume of LPAs who had clicked the link featured on the email. Via Smartlook, we could also view how they interacted with the service. 

[We tracked the engagement using a spreadsheet](https://docs.google.com/spreadsheets/d/1SBuBqmsP4dUXhYprDjWhSQ96FqyasRsbkMRCWsYQBtY/edit?gid=733731380#gid=733731380) and collected data on:

* the number of emails sent and bounced
* the number of LPAs engaging with our platform via the UTM link, the date of the service interaction, and the volume of sessions
* if the LPA has submitted the BfL dataset and how they engaged with MHCLG

## Our solution

### Notification banner

To encourage LPAs to review their register by 31 December, we designed a notification banner to appear on LPAs’ dashboards at the top of the screen, [based on best practice from the design system](https://design-system.service.gov.uk/components/notification-banner/). 

![](/encouraging-lpas-to-update-brownfield-land-data/01-screenshot-2025-02-24-at-15.29.51.png)

### Email to LPAs

>Subject line: Action required: review your brownfield land register by 31 December 2024

>Dear ((LPA name)),

>You must review your brownfield land register by 31 December 2024.

>Update your register as soon as a new brownfield site is identified or an existing one changes status, to increase trust in the data.

>**How to update your brownfield land register**

>Go to the service: ((UTM link))

>This will guide you through:

>* checking your brownfield land register for errors
>* publishing it
>* telling us where you’ve published it

>Use the guidance to help you: https://www.gov.uk/government/publications/brownfield-land-registers-data-standard/publish-your-brownfield-land-data

>If you need further support, email us at DigitalLand@communities.gov.uk

>Regards,

>Michael-Jordan Faucher-Folie on behalf of Digital Land, MHCLG

We sent the email to 283 recipients. Of those, 41 emails bounced.

In total, 83 LPAs updated their brownfield land registers after receiving the email.

![](/encouraging-lpas-to-update-brownfield-land-data/02-screenshot-2025-02-24-at-15.33.08.png)

### LinkedIn post

We also worked with the comms team to publish a LinkedIn post to help catch the eye of more LPAs:

![](/encouraging-lpas-to-update-brownfield-land-data/03-screenshot-2025-02-24-at-14.30.37.png)

## Next steps

Due to the banner using incorrect logic, we've decided to temporarily remove the banner for now. 

Additional steps will be required before implementing this feature. 

The previous logic was based on LPAs needing to submit their BfL data each year before the 31st December, but the new logic should be based on the last submission date (for example, if an LPA submitted BfL data in April, then we would expect them to submit again the following year in April).


