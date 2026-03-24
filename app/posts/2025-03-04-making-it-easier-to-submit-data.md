---
title: Making it easier to submit data
description: |-
  The problem

  Historically, users have had to email our data management team whenever they had datasets ready to submit. This caused a few problems:

  1. Users...
date: '2025-03-04'
screenshots:
  items:
  - text: Screenshot 2025 03 04 at 10.36.14
    src: 01-screenshot-2025-03-04-at-10.36.14.png
  - text: Screenshot 2025 03 04 at 10.39.06
    src: 02-screenshot-2025-03-04-at-10.39.06.png
tags: []
---

## The problem

Historically, users have had to email our data management team whenever they had datasets ready to submit. This caused a few problems:

1. Users would naturally wait until they had more than 1 dataset to submit, so they could email them over in bulk. This went against our ethos of iterative submission and meant a longer period of time between submissions.

2. Users would have to exit the service to complete an ‘offline’ part of the journey by emailing their data to us, causing a disjointed and inconsistent user experience. 

3. Our data management team uses JIRA to track submissions from users. Sometimes, users have replied to old JIRA email threads to submit their datasets, not realising those JIRA threads had been closed on our end. This meant that our team didn’t pick those up. 

![](/making-it-easier-to-submit-data/01-screenshot-2025-03-04-at-10.36.14.png)
The screenshot shows our current guidance, prompting users to email us manually. 

## Our approach

Our approach to these problems has been to design a way for users to submit their datasets to us without having to manually send us an email each time. 

## Our solution

We’re currently working on an integrated form which means users can now submit their data in the service itself, without having to leave and email us manually.

This is a short process where users provide their:

* full name
* work email address
* endpoint URL
* webpapge URL

We’ve started to show this journey in user research sessions to collect feedback.

It’s clear that users are relieved about this iteration to the service, allowing them to stay in their current journey to submit their datasets. 

##&nbsp;Next steps

We’ve faced a few challenges with this piece of work, which has slowed down the submission form going live.

We needed initial cyber approval to use JIRA integration in our service. Once we got approval, we built the integration but needed infrastructure to review our code (due to team available this delayed us a bit).

Once they reviewed it, one of the suggestions was that we needed the Atlassian supplier to give us a copy of production service desk in a sandbox environment for use in staging and development.

Once we got a sandbox environment, we needed API keys (this is still in progress).

As part of the cyber approval, we were advised to do an IT health check. We’re still waiting on a response from cyber about this.

We’ve also started to make design tweaks to recurring user insights, such as confusion around terminology like ‘endpoint URL’ and ‘webpage URL’. 

![](/making-it-easier-to-submit-data/02-screenshot-2025-03-04-at-10.39.06.png)

We’ll be researching this further over the next few weeks by carrying out some highlighter testing with participants to help us refine this further.



