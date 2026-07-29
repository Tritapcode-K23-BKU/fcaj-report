---
title: "Week 6"
date: 2026-07-29
weight: 6
chapter: false
pre: " <b> 1.6 </b> "
---

#### Week 6 — Frontend integration with the live API

**Dates:** 06/07 - 12/07/2026

#### Goals

- Connect the entire React frontend to the live API
- Resolve the data contract mismatch between frontend and backend
- Deploy the frontend to S3 and CloudFront
- Verify the business flows end to end

#### Work carried out

During integration I found that the frontend and backend, developed in parallel,
had divergent data contracts: payment methods, order statuses, price field names
and voucher identifiers all differed.

I weighed three options: change the backend, change the frontend, or insert an
adapter layer. I chose the third because it preserves the already-tested work on
both sides. All translation was concentrated in a single file, converting data in
both directions.

Built the frontend, uploaded it to S3 and created a CloudFront invalidation.
Verified the flows: registration, login, product browsing, add to cart, discount
codes, checkout and order history.

#### Results

- A complete website on CloudFront covering all business flows
- An adapter layer resolving the contract mismatch, making the boundary explicit
- The server recalculates order totals rather than trusting the browser

#### Difficulties and how they were resolved

The effort required to connect components written by different people was far
greater than expected. The lesson: data contracts between layers must be agreed
in writing at the start, before anyone begins coding.
