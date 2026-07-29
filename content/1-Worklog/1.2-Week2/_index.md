---
title: "Week 2"
date: 2026-07-29
weight: 2
chapter: false
pre: " <b> 1.2 </b> "
---

#### Week 2 — Serverless architecture

**Dates:** 08/06 - 14/06/2026

#### Goals

- Understand serverless compute and when it is appropriate
- Deploy a first Lambda function
- Connect Lambda to API Gateway to create an Internet-reachable endpoint
- Get familiar with DynamoDB and the NoSQL data model

#### Work carried out

Wrote and deployed a simple Node.js Lambda function, experimenting with
different timeout and memory settings to observe the effect.

Created an HTTP API in API Gateway, wired it to Lambda and tested it with `curl`.
Studied the event structure API Gateway passes to Lambda.

Created a first DynamoDB table and practised PutItem, GetItem, Query and Scan.
Compared the cost and speed of Query versus Scan on the same table.

#### Results

- Deployed a complete API running on the Internet with no servers to manage
- Understood the fundamental difference between Query and Scan in DynamoDB
- Realised NoSQL table design follows access patterns rather than normalisation

#### Difficulties and how they were resolved

I hit a problem where Lambda called DynamoDB and returned a permissions error.
Re-reading the documentation, I learned that Lambda uses an execution role rather
than the creator's credentials. This was the first time IAM felt practical rather
than theoretical.
