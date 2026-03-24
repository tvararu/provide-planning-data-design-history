---
title: First prototype
description: |-
  Getting data from local planning authorities LPA and onto our platform is slow.

  For example, we have to:

  - ask users to send us their data
  - check the data...
date: '2023-10-26'
screenshots:
  items:
  - text: check
    src: 01-check.png
  - text: confirmation
    src: 02-confirmation.png
  - text: dataset
    src: 03-dataset.png
  - text: email-address
    src: 04-email-address.png
  - text: errors
    src: 05-errors.png
  - text: exit
    src: 06-exit.png
  - text: has-webpage
    src: 07-has-webpage.png
  - text: lpa
    src: '08-lpa.png'
  - text: name
    src: '09-name.png'
  - text: start-page
    src: 10-start-page.png
  - text: subject
    src: 11-subject.png
  - text: transformations
    src: 12-transformations.png
  - text: upload
    src: 13-upload.png
  - text: webpage
    src: 14-webpage.png
tags: []
---

Getting data from local planning authorities (LPA) and onto our platform is slow.

For example, we have to:

- ask users to send us their data
- check the data meets the requirements
- ask users to make changes (often multiple times)

So we’ve prototyped a new service to allow users to:

- check their data meets the requirements
- send their data to us to publish on the platform

We hope this will:

- reduce the time it takes to get data onto the platform
- help users do more of the work themselves

## How it works

An email will be sent to invite the user to publish their data on our platform.

{email}
Subject: Publish your planning and housing data for England
---
Dear ((name))

You can now use our new service to:

- check your data follows the standard
- get your data published

Publish your planning and housing data:
https://publish.planning-data.dev/start

# Before you check your data

You need to prepare your:

- conservation area data
- listed building data
- article 4 direction data
- tree preservation order data

You may need to create more than one set of data for each subject. You'll find what to include in the [data specifications](https://www.planning.data.gov.uk/guidance/specifications/).

We’ll accept data supplied as either:

  - CSV
  - GeoJSON
  - GML
  - GeoPackage

# Before you can publish your data

You must be able to create or edit a webpage on your local planning authority’s (LPA) website. This will probably have a URL ending in .gov.uk or .org.

If you’re not able to do this, you’ll need to ask the person who updates your website.

The webpage needs to include:

- a summary of what the data is about
- a confirmation that the data is provided under the Open Government License
- the date you created or updated the webpage
- links to your data on this page, for example a CSV

# Get help

Get help, report a problem or give feedback at [digitalland@levellingup.gov.uk](mailto:digitalland@levellingup.gov.uk).
{/email}



Clicking the link will take the user to the start page of the service.

### Start page

![](https://design-history.ams3.digitaloceanspaces.com/9b96ajsoh45socyl4pkp4xixexne)

### Data subject

![](https://design-history.ams3.digitaloceanspaces.com/cywk080vq1t7gylvqynrs9hqhii1)

### Dataset

If the data subject has multiple datasets, the user will be taken to the dataset page.

![](https://design-history.ams3.digitaloceanspaces.com/kty5oh9hltyh4npasmyh362x57ed)

### Upload data

![](https://design-history.ams3.digitaloceanspaces.com/zq1rgw6j9k1q0x55fcyvknbp4ae8)

### Showing errors

If the data contains errors that we cannot fix automatically, the user will be taken to the errors page.

![](https://design-history.ams3.digitaloceanspaces.com/kbmt0ik8g0h3b0x08uw4rlhi69hy)

Users can continue without fixing errors. This allows us to get as much data as possible onto the platform. This will only add the fields without errors to the platform.

### Showing how the data will be changed

When the data is added to the platform, certain data will be changed to meet our requirements.

For example:

- a date in format `DD-MM-YYYY` will be changed to`YYYY-MM-DD`
- x and y coordinates will be swapped to make sure the geometric data is within England
- an entry date will be added and set it to today if it’s not provided
- redundant columns will be removed
- column headings will be changed to lowercase
- column headings will be hyphenated

This means users have to do less work to prepare their data. Therefore more data will be published to the platform.

To tell users about these changes, we show them on a separate page.

![](https://design-history.ams3.digitaloceanspaces.com/n7ic9e8ihwwthsivzqdpmmna7m17)

### Checking if the user has a webpage where their data is published

We’re currently asking LPAs to publish their data on their own website.

We then take the data from the website and put it onto our platform. 

At this point in the journey, users may not have a webpage.  So we ask them if they have a webpage. 

![](https://design-history.ams3.digitaloceanspaces.com/k82htm0uvkfn56cviesiwyqcly96)

If they say ‘Yes’ they can continue. If not, we take them to an exit page with information about how to publish their data on their website.

![](https://design-history.ams3.digitaloceanspaces.com/c7u44icfujqin9ybglv4b1dzpgxl)

### URL where their data is published

![](https://design-history.ams3.digitaloceanspaces.com/tfz489s5ia6d6w2yvg3zezj5dqxu)

### Email address

![](https://design-history.ams3.digitaloceanspaces.com/w2h4pol5dsifg24j46zs7t176bzb)

We ask for this so we can:

- send them a confirmation email
- send them a copy of their transformed data
- tell them when we’ve published the data
- tell them if there’s data they need to fix

### First and last name

![](https://design-history.ams3.digitaloceanspaces.com/zt2szuvcxhzpo81ax1pahewr9q0l)

We ask for this so we can call them by their name when we contact them.

### Local planning authority

![](https://design-history.ams3.digitaloceanspaces.com/qe6or0m9ated58ghg6hzm6508evi)

We ask for this so we know who is sending us their data.

### Check answers page

![](https://design-history.ams3.digitaloceanspaces.com/7gpxzhu5p0t3uxjvrwiyy0084cud)

### Confirmation page

A confirmation email will also be sent containing a link to download their data.

![](https://design-history.ams3.digitaloceanspaces.com/khrd6fm4rrppxx0q6mxg3t0hkvzu)

## Further considerations

We want to consider:

- showing the areas or points on a map
- forcing users to fix their errors before continuing
- only telling users how their data was changed after they send it to us
- splitting up the service into separate journeys for checking and sending the data


