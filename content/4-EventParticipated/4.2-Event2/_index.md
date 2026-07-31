---
title: "Event 1"
date: 2026-07-11
weight: 2
---

## Internal Tech Seminar — AWS Ecosystem: Governance, Security & Optimization (July 11, 2026)

**Format:** Internal knowledge-sharing session
**Scope:** AWS certification foundations, AI-driven application security, SLA & monitoring
**Number of talks:** 3
**Date:** July 11, 2026

I attended a second internal seminar focused on the AWS ecosystem, covering the AWS Cloud Practitioner (CLF-C02) certification path, AI-driven application security automation, and operational monitoring practices built around SLAs.



### Talk 1 — AWS Cloud Practitioner (CLF-C02) Roadmap

The exam has 65 multiple-choice questions (90 minutes), with a passing score of 700/1,000, split across four domains: Cloud Concepts (24%), Security & Compliance (30%), Technology & Services (34%), and Billing & Support (12%).

Key foundational concepts covered:
- **Shared Responsibility Model:** AWS secures the cloud (infrastructure, physical layer); the customer secures what's in the cloud (data, configuration).
- **Six core cloud benefits:** trading CapEx for OpEx, benefiting from economies of scale, no longer guessing capacity, increased speed and agility, saving on data center running costs, and going global in minutes.
- **AWS Well-Architected Framework:** six pillars — Operational Excellence, Security, Reliability, Performance Efficiency, Cost Optimization, and Sustainability.

Exam strategy shared: process of elimination, mapping keywords to services (e.g. "decouple" → SQS), and defaulting to the simplest correct answer.

### Talk 2 — Web Application Security with an AWS Security Agent

Introduced **Frontier Agent**, a generative-AI-based (Amazon Bedrock) security automation tool.

**Problem it addresses:** manual penetration testing is costly, slow, and inconsistent.

**Key capabilities:**
- *Design Review* — evaluates architecture docs or Infrastructure-as-Code (Terraform) before implementation begins.
- *Code Security* — automatically scans GitHub/GitLab pull requests and proposes patches.
- *Automated Pentesting* — attacks a running application to confirm real vulnerabilities (XSS, IDOR) with concrete evidence.

**Cost & limitations:** 2 months free trial (400 hours/month), then $50 per task-hour. Automated tasks can be blocked by layers like MFA, biometrics, and mTLS, and struggle to catch deep business-logic flaws.

### Talk 3 — SLAs and Risk Monitoring

The core shift discussed: from "the system is up" to "the user is satisfied."

- **SLA (Service Level Agreement):** a formal commitment between a service provider and its customers on service quality.
- **Monitoring pyramid:** monitoring should be built bottom-up — Infrastructure → Application → Business → Customer Experience.
- **Core message:** infrastructure reporting healthy (e.g. HTTP 200 OK) doesn't guarantee a good user experience if a hidden failure exists underneath (e.g. login failures from a database bottleneck).
- **Risk & alerting process:** a 4-step cycle — Identify → Monitor → Respond → Improve. Custom metrics (e.g. login failure rate) trigger a **CloudWatch Alarm**, which pushes a notification via **SNS** to email/Slack for the ops team.

**Takeaway:** Move from monitoring servers alone to monitoring the actual end-user experience.

---

### Personal Application Plan

1. Systematize core knowledge around the AWS Well-Architected Framework and review key service terminology in preparation for the CLF-C02 exam.
2. Experiment with integrating automated source-code scanning into the CI/CD pipeline (GitHub/GitLab) to catch vulnerabilities before release.
3. Review the current monitoring metric set and build user-behavior metrics (e.g. failed transaction rate) instead of relying only on CPU/RAM, paired with CloudWatch Alarm and SNS for instant notification.

![Attendance photo](/fcaj-report/static/images/4-Events/events-seminar-2.jpg)