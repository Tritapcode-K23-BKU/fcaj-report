---
title: "Week 5"
date: 2026-07-29
weight: 5
chapter: false
pre: " <b> 1.5 </b> "
---

#### Week 5 — API layer deployment

**Dates:** 29/06 - 05/07/2026

#### Goals

- Create a least-privilege IAM role for Lambda
- Deploy the backend developer's API code to Lambda
- Configure API Gateway with 22 routes
- Enable CORS so the frontend can call the API

#### Work carried out

Created a dedicated IAM role for Lambda granting only read/write access to the 8
DynamoDB tables and `personalize:GetRecommendations` on a single campaign. No
broad managed policies were used.

Packaged the backend developer's code and its dependencies into a zip and
uploaded it to Lambda. Raised the timeout to 30 seconds and memory to 512 MB,
since the 3-second default is not enough when calling external services.

Created an HTTP API with a catch-all `/{proxy+}` route, letting the code handle
routing internally. This keeps the API Gateway configuration simple across 22
routes.

Configured CORS so the frontend on the CloudFront domain can call the API on a
different domain.

#### Results

- The API works, is reachable from the Internet and returns real DynamoDB data
- The IAM role follows least privilege
- All 22 routes verified from the command line

#### Difficulties and how they were resolved

The frontend reported it could not reach the server while `curl` worked fine.
Opening Developer Tools revealed a CORS error. I learned that CORS errors only
appear in the browser, so debugging must happen in the same environment real
users experience.
