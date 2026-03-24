---
title: 'Provider service walkthrough: Part 1 — principles and context'
description: |-
  Provider service walkthough

  Whilst designing the provider service, we used established usability principles. We followed the Nielsen Norman Group NNG Usabil...
date: '2025-07-09'
tags: []
---

## Provider service walkthough

Whilst designing the provider service, we used established usability principles. We followed the [Nielsen Norman Group (NNG) Usability Heuristics](https://www.nngroup.com/articles/ten-usability-heuristics/) as well as the [Government Design Principles](https://www.gov.uk/guidance/government-design-principles).

### How we used the NNG Usability Heuristics

We applied these 10 guidelines consistently:

1.  **Visibility of System Status:** Users need to know the status of their data on the platform. Users should understand what is happening and what they need to do to add, change, or update information.
2.  **Match Between System and the Real World:** The dashboard reflects the state of the data on the planning data platform.
3.  **User Control and Freedom:** We gave users ways to undo actions and leave processes easily. This helps them feel in control.
4.  **Consistency and Standards:** We kept design elements and terms the same across the service. We used patterns and components from the GOV.UK Design System.
5.  **Error Prevention:** We designed the service to stop errors before they happen by explaining what users need to go and giving them guidance in context.
6.  **Recognition Rather Than Recall:** The service shows options and information clearly. Users do not need to remember details.
7.  **Flexibility and Efficiency of Use:** The service is easy for new users. It also has features that help experienced users work efficiently.
8.  **Aesthetic and Minimalist Design:** We kept the design simple and tidy following the GOV.UK design system and adapting patterns as necessary. This helps users focus on key content and tasks.
9.  **Help Users Recognise, Diagnose, and Recover from Errors:** If an error occurs, messages are clear. They explain what went wrong and how to fix it.
10. **Help and Documentation:** We made help guides easy to find and understand. This supports users.

The main goal is that the user is able to see the state of their data on the system and understand what they need to do to provide, maintain and update their data.

---

### Other design principles we used

Two other principles guided our design:

* **Progressive disclosure:** We avoided giving users too much information at once. Instead, we give users what they need at that point and reveal more detail closer to the context

* **Open data:** Our service is built on open data. This means all information is public. This was a challenge because we do not always know who the user is. For simplicity we decided to assume the Local Planning Authority (LPA) is the main user. This helped us choose the right words and features. In the service, 'we' means the MHCLG/Planning data team, and 'you' refers to the LPA.

### Constraints

The system currently has **no authentication or user accounts**. The team did not want to manage a user account system. This means anyone can view all pages. This choice affects the service in two ways:

* **Limited personalisation:** Without user accounts, we cannot offer personalised experiences.
* **Repetitive data entry:** Users might have to enter the same information multiple times, as individual user data is not saved.

We are have done some initial research to see how users would react to an email authentication process. 

By following these design principles and understanding our limits, we aimed to build a service that is both easy to use and effective for providing and managing data.

## Related links

[Provider service walkthrough: Part 2](https://submit-planning-data.designhistory.app/provider-service-walkthrough-part-2-walkthrough)
[Provider service walkthrough: Part 3](https://submit-planning-data.designhistory.app/provider-service-walkthrough-part-3-check-flow)

