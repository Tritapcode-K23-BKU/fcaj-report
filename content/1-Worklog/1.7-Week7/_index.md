---
title: "Week 7"
date: 2026-07-29
weight: 7
chapter: false
pre: " <b> 1.7 </b> "
---

#### Week 7 — Amazon Personalize setup

**Dates:** 13/07 - 19/07/2026

#### Goals

- Create a dataset group and import interaction data
- Train a first recommendation model
- Deploy a campaign for real-time inference
- Wire recommendations into the home page

#### Work carried out

Created a dataset group and defined the schema for the Interactions dataset.
Created an IAM role allowing Personalize to read the data bucket, plus the
corresponding bucket policy.

Generated a first interaction dataset of 4,491 events distributed uniformly at
random. Imported it into Personalize and trained a solution using the
`aws-user-personalization` recipe.

When training finished, the evaluation metrics were poor: Precision@5 of only
0.0889 and MRR@25 of 0.1216.

I deployed the campaign anyway and wired it into the recommendation route in
Lambda to complete the technical path, while beginning to analyse why the results
were so weak.

#### Results

- A complete technical path: Lambda calls the campaign and returns recommendations
- A recommendation block rendering on the home page
- Identified that the problem lay in the data, not the service configuration

#### Difficulties and how they were resolved

I found a subtle bug that produced no error message: DynamoDB does not guarantee
results in the order keys are passed in, so the ranking computed by the model was
being lost. The results had to be re-sorted into the original order after
querying. This was only detectable by carefully comparing the returned output.
