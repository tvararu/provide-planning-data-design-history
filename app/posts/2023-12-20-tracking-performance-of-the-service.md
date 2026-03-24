---
title: Tracking performance of the service
description: |-
  To make sure the service is working well, we’ll track:

  - completion rate
  - completion time
  - form validation error rate
  - data specification error rate
  - sa...
date: '2023-12-20'
tags: []
---

To make sure the service is working well, we’ll track:

- completion rate
- completion time
- form validation error rate
- data specification error rate
- satisfaction score
- support request rate

## Examples

### Completion rate

Between January 2024 and February 2024:

- 1000 users started to use the service
- 900 out of 1000 (90%) completed the service
- 100 out of 1000 (10%) did not get past the error page

### Completion time

Between January 2024 and February 2024:

- 900 users completed the service
- 10% of users (90) took less than 2 minutes
- 20% of users (180) took between 2 to 5 minutes
- 80% of users (720) took over 5 minutes

### Form validation error rate

Between January 2024 and February 2024:

| Field       | Error message                                                    | Error count | Unique error count |
| ----------- | ---------------------------------------------------------------- | ----------- | ------------------ |
| Dataset     | Select dataset                                                   | 8           | 6                  |
| Upload data | Select a file                                                    | 2           | 1                  |
| Upload data | The selected file must be a CSV, GeoJSON, GML or GeoPackage file | 10          | 5                  |

### Dataset error rate

Between January 2024 and February 2024:

| Dataset             | Field     | Error message               | Error count | Unique error count |
| ------------------- | --------- | --------------------------- | ----------- | ------------------ |
| Conservation area   | Geometry  | Geometry column is missing  | 147         | 101                |
| Conservation area   | Geometry  | Geometry must be in England | 34          | 27                 |
| Article 4 direction | Reference | Reference column is missing | 25          | 21                 |

### Satisfaction score

Between January 2024 and February 2024:

- 90% of users said they were delighted
- 5% of users said they were satisfied
- 5% of users said they were unhappy

### Support request rate

Between January 2024 and February 2024 we received 25 support requests.

