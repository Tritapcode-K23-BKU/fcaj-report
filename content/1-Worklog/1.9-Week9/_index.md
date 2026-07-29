---
title: "Week 9"
date: 2026-07-29
weight: 9
chapter: false
pre: " <b> 1.9 </b> "
---

#### Week 9 — Monitoring, testing and documentation

**Dates:** 27/07 - 02/08/2026

#### Goals

- Set up monitoring and alerting for the system
- Test end to end from browser to model
- Plan resource clean-up
- Complete documentation and the internship report

#### Work carried out

Created an SNS topic and subscribed an email for alerts. Set up two CloudWatch
alarms for Lambda error rate and latency, and verified them by hitting a
non-existent path to generate errors.

Tested end to end layer by layer from the inside out: DynamoDB, API, Personalize,
then the frontend. Two checks in particular: recommendations for two different
users must differ, and an order with a tampered price must be recalculated by the
server.

Built a prioritised clean-up checklist, putting the Personalize campaign first
since it bills per hour it exists.

Wrote the workshop documentation as a step-by-step lab and completed the
internship report on the Hugo platform.

#### Results

- Two working alarms sending email when thresholds are exceeded
- An 8-item end-to-end test checklist, all passing
- Workshop documentation enabling others to rebuild the entire system
- A complete bilingual internship report

#### Difficulties and how they were resolved

Writing the workshop revealed several things I thought I understood but did not.
Guiding someone else through the same build requires explaining every step rather
than glossing over it. This turned out to be a far more effective knowledge check
than self-assessment.
