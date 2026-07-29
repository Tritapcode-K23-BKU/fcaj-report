---
title: "Week 4"
date: 2026-07-29
weight: 4
chapter: false
pre: " <b> 1.4 </b> "
---

#### Week 4 — Storage and database layers

**Dates:** 22/06 - 28/06/2026

#### Goals

- Create S3 buckets for the frontend and for training data
- Configure CloudFront with Origin Access Control
- Create the 8 designed DynamoDB tables
- Seed sample data for 100 products

#### Work carried out

Created two S3 buckets with separate roles. The frontend bucket stays fully
private, accessible only by CloudFront through Origin Access Control rather than
being made public as many older guides suggest.

Configured CloudFront: enabled HTTP to HTTPS redirection, set `index.html` as the
default root object, and added custom error responses mapping 403 and 404 to
`index.html` so the single-page app works when sub-paths are opened directly.

Created 8 on-demand DynamoDB tables. The Reviews and Orders tables use composite
keys so they can be queried rather than requiring a full table scan.

Wrote a seeding script for 100 products across 8 categories.

#### Results

- Static frontend served through CloudFront over HTTPS
- S3 bucket verified as inaccessible directly from the Internet
- 8 DynamoDB tables ready with sample data

#### Difficulties and how they were resolved

After uploading a new build to S3, the site rendered blank. I spent a long time
checking the source code before discovering CloudFront was still serving the
cached old version. From then on I remembered the rule: every upload to S3 must
be followed by an invalidation.
