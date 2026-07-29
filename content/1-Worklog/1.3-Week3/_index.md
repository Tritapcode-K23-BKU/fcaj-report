---
title: "Week 3"
date: 2026-07-29
weight: 3
chapter: false
pre: " <b> 1.3 </b> "
---

#### Week 3 — Topic selection and architecture design

**Dates:** 15/06 - 21/06/2026

#### Goals

- Decide the team's final project topic
- Design the overall architecture and select services
- Allocate work across five team members
- Estimate costs and set a budget alert

#### Work carried out

The team discussed and settled on an e-commerce recommendation system. The
reasons: the problem has clear practical value, it uses several interconnected
AWS services, and it involves machine learning without requiring us to implement
algorithms ourselves.

Designed a two-path architecture: a static path through CloudFront and S3, and a
dynamic path through API Gateway and Lambda. Compared alternatives before
deciding and documented the reasoning behind each choice.

Allocation: I took the Cloud Architect role, responsible for infrastructure and
architectural decisions. The other four covered backend, frontend, machine
learning and data.

Set up AWS Budgets with an alert threshold to avoid unexpected charges.

#### Results

- A complete architecture diagram with justification for each service choice
- A clear work allocation table for the five members
- A working budget alert

#### Difficulties and how they were resolved

The team spent considerable time choosing a topic because we did not know what
scope was realistic in the time available. Our initial idea was much larger and
had to be cut back to ensure we could actually finish.
