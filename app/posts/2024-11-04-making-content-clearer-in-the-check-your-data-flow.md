---
title: Improving content in the 'check your data' flow
description: |-
  The problem

  We spotted an opportunity to improve some of the content in the ‘check’ flow to make things clearer for users who are checking their data for er...
date: '2024-11-04'
screenshots:
  items:
  - text: 379241496 fccf6395 1f85 4816 bcc6 0273988323dc
    src: 01-379241496-fccf6395-1f85-4816-bcc6-0273988323dc.png
  - text: Screenshot 2024 10 25 at 10.27.00
    src: 02-screenshot-2024-10-25-at-10.27.00.png
  - text: Screenshot 2024-10-25 at 10.29.10
    src: 03-screenshot-2024-10-25-at-10.29.10.png
  - text: Screenshot 2024-10-25 at 10.29.49
    src: 04-screenshot-2024-10-25-at-10.29.49.png
tags: []
---

## The problem

We spotted an opportunity to improve some of the content in the ‘check’ flow to make things clearer for users who are checking their data for errors. 

## What we did 

We reviewed the content in the existing flow, and provided suggestions to iterate.

### You have [x number] of rows ready to publish 

![](https://design-history.ams3.digitaloceanspaces.com/hspul1firzdzdi25jh531cd02u0w)
![](https://design-history.ams3.digitaloceanspaces.com/07bcun31y6a5m48d9gt5ge7wp1ds)

We’ve changed ‘check your data before you continue’ to ‘you have [x number] of rows ready to publish’ to more accurately reflect the outcome of the previous action of the user who’s providing a file / URL. 

The user’s data either has errors, or it doesn’t - that’s the key message here. In this case, there are no errors, and they therefore have data ready to publish. Using dynamic content and bringing the number of rows to publish into the heading gives it more prominence. 

The original content implies that we haven’t checked a user’s file yet, but we have.

## Your data has errors

![](https://design-history.ams3.digitaloceanspaces.com/kqro2gj4s3mbngh503lg46n590si)

The content underneath the errors used to be similar to this, except we used to provide a third step which was ‘publish the data’, but the user isn’t actually at that step just yet. 

We want to give users the information they need at the time they need it, and in this instance that time isn’t right now, so we don’t want to add more to their plate just yet. We’ve moved that to the confirmation screen instead, where it sits more accurately in their journey.

We also now provide a link to the data guidance for the user to refer to whilst fixing their errors.

## You can now publish your data 

![](https://design-history.ams3.digitaloceanspaces.com/4w5xx16i9op2bzcpkkeb91m761t9)

The confirmation banner used to say ’Send us your data’, but it felt passive and we thought we could be more intentional with the action the user now needs to take. We’ve changed this to ‘You can now publish your data’ to reflect that. It’s also more of a positive action reflective of the confirmation banner pattern, and the publishing needs to come first anyway before sending it to us.

We’ve kept the ‘what you need to do next’, to reinforce the fact the user needs to take an action and that although they’ve reached the end of the check service, this isn’t the end of their journey. We don’t want users to exit this screen thinking that they have nothing else to do.

## Outcomes 

No outcomes yet. We haven't tested the new content with users.

## Future iterations 

### Explore users’ behaviours to fixing their data 

It’d be interesting to learn more about users’ behaviour with the part of the journey where they receive errors about their data. In the future, we may want to allow users to download a copy of their errors as there could be a lot. Downloading a copy would allow users to exit the service and come back later once their errors are fixed.

### Confirmation screen 

On the confirmation screen, we’ve removed the example webpage for now until we can mock up a more accurate version. The way this was designed originally was confusing some users, so we want to make sure it’s helping people instead of hindering them.




