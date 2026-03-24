---
title: Processing files asynchronously in the check tool
description: |-
  &nbsp;The problem

  In order to improve the stability and reliabilty of the check tool, especially when handling large data files, the dev team needed to impl...
date: '2024-04-08'
screenshots:
  items:
  - text: Proposed user flow
    src: 01-proposed-user-flow.png
    alt: User flow diagram showing how files would be processed asynchronously
tags: []
---

##&nbsp;The problem

In order to improve the stability and reliabilty of the check tool, especially when handling large data files, the dev team needed to implement [asynchronous processing for file uploads](https://digital-land.github.io/technical-documentation/architecture-and-infrastructure/proposals/001-publish-async/).

This means that file uploads and URL submissions aren’t processed immediately, but put in a queue.

We needed a way to handle this in the UI, so users would be informed their file is being processed and notified when it was complete, whilst keeping compliant with the WCAG accessibility standards and providing a user friendly experience.

## What we did

In order to comply with [WCAG 2.1 Success Criterion 2.2.1 Timing Adjustable](https://www.w3.org/TR/UNDERSTANDING-WCAG20/time-limits-required-behaviors.html) it is not possible to redirect the user to the results page automatically, so an intersitial page has to be shown to the user.

The proposed flow:
![User flow diagram showing how files would be processed asynchronously](/asynchronous-file-upload-processing/01-proposed-user-flow.png)

The intersitial page polls the server to see if the request has been processed. Once it has, it reveals a continue button for the user to manually progress.

For non-javascript users the continue button is always visible and once clicked it checks whether the request has been processed. If it has the user proceedes to the results page, and if not they stay on the processing page.

I asked on x-gov slack if any one else had done similar and got replies from Adam Liptrot at HMRC and Joe Lanman at GDS. They confirmed that the approach above was similar to what they had done in their services.

I also got confirmation that animated loading spinners can cause accessibility issues:

> I’d always personally steer away from the continuous loading spinners (especially large ones like the one you linked) due to their vestibular / distraction impact. It might only be for 5-10 seconds but that’s enough to trigger someone (and a reason WCAG 2.2.2 is there). Unfortunately we can’t rely on prefers-reduced-motion (and that spinner doesn’t support it anyway). Loaders which have a short animation followed by a pause and then repeat the short animation are much less prone to cause issues.

## Future iterations

The results of the check tool are persistent which means that anyone can view them at any time after they’ve been processed.

We might want to provide a way to access previous check results and a way to share them with other team members.

