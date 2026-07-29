---
title: "Week 11"
date: 2026-07-29
weight: 11
chapter: false
pre: " <b> 1.11 </b> "
---

#### Week 11 — Resource clean-up and wrap-up

**Dates:** 10/08 - 15/08/2026

#### Goals

- Clean up all AWS resources following the checklist
- Confirm no ongoing charges
- Summarise lessons learned

#### Work carried out

Executed the clean-up in the planned priority order: deleted the Personalize
campaign first since it bills per hour of existence, then the solution and
dataset group, disabled and deleted the CloudFront distribution, emptied and
removed both S3 buckets, deleted API Gateway and Lambda, dropped the eight
DynamoDB tables, and finally removed the IAM role and alarms.

Deleted the temporary IAM accounts issued to teammates along with their access
keys.

Verified through the Billing Dashboard and Resource Groups that nothing was left
behind.

Summarised lessons learned and next steps.

#### Results

- All resources deleted, confirmed via the Billing Dashboard
- No unexpected charges incurred
- Internship completed with all deliverables handed over

#### Difficulties and how they were resolved

Deleting Personalize requires the exact order of campaign, solution, dataset,
dataset group, otherwise dependency errors occur. I also had to remember to
disable the solution's automatic retraining before deletion, to avoid triggering
a new training run and incurring cost.
