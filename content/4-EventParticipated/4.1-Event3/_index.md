---
title: "Event 3"
date: 2026-07-25
weight: 3
chapter: false
---

## Internal Tech Seminar — Agentic AI on AWS (July 25, 2026)

**Format:** Internal knowledge-sharing session
**Scope:** Agentic AI applications built on AWS (Amazon Bedrock, SageMaker, Multi-Agent systems)
**Number of projects:** 4
**Date:** July 25, 2026
**Location:** 26th Floor, Bitexco Tower, 02 Hai Trieu Street, Saigon Ward, Ho Chi Minh City
**Role:** Attendee

This session focused on Agentic AI — a new generation of AI capable of autonomously analyzing, deciding, and executing business workflows. Four projects illustrated how AWS infrastructure services (Amazon Bedrock, SageMaker) combine with multi-agent architectures to tackle problems ranging from public safety to business strategy and financial compliance.

![Attendance photo](/fcaj-report/images/4-Events/events-seminar-3.jpg)

### Project 1 — S.H.E.P.H.E.R.D (Team 3KA)

Smart crowd monitoring and management for events and public spaces.

**Challenge:** Traditional manual monitoring is slow, hard to scale, and prone to missing incidents when conditions change quickly.

**Solution:** Live video analysis converts footage into operational metrics — crowd density, queue wait-time estimates, and overload forecasting — using YOLO + ByteTrack for object tracking, processed on Amazon SageMaker and Amazon Bedrock AgentCore.

**Agent structure:**
- *Autonomous Monitor* — tracks conditions and raises timely alerts.
- *Operator Copilot* — lets staff query the system in natural language for real-time information.

### Project 2 — SA Professional Native App (Team Plan V)

An AI-native app built to automate routine tasks for Solutions Architects.

**Challenge:** SAs spend significant time manually breaking down requirements, drawing diagrams, estimating cost, and writing Infrastructure-as-Code.

**Solution:**
- Takes natural-language requirements and auto-generates architecture diagrams in Draw.io using standard AWS icons.
- Automatically estimates operating cost for the Singapore region (`ap-southeast-1`).
- Auto-generates IaC.

**Value:** Cuts the time from a blank page to a complete architecture draft down to minutes.

### Project 3 — Signal Scout (Team Dream AI)

A strategic decision-support system that automatically detects and synthesizes business "signals."

**Core value:** Strings together disparate metrics into a coherent narrative, helping leadership decide to "Maintain, Adapt, or Accelerate" based on concrete evidence.

**Key functions:** Early detection of restructuring signals, financial/operational health analysis, and risk-scenario simulation on an executive dashboard.

**Operating cost:** Estimated at $81–$359/month depending on scale, combining AWS infrastructure with third-party tools like Apify and Langfuse.

### Project 4 — Adaptive AML/KYT Workflow Engine

Automates Anti-Money Laundering (AML) and Know-Your-Transaction (KYT) processes for financial institutions.

**Challenge:** Manual review takes an average of 3 hours per shift, with a false-positive rate as high as 90–95%.

**Multi-agent solution:** Specialized agents split responsibilities — a *Profile Checking Agent* (customer profile review) and a *Money Flow Agent* (transaction flow analysis).

**Process & benefits:** Automated flow — Detect → Investigate → Recommend → Execute — with a human-in-the-loop retaining final approval. Cuts processing time down to minutes while maintaining transparency through clear source citations.

---

### Key Takeaways

1. **Multi-agent architecture is key for complex workflows** — splitting a problem across specialized agents (as in AML/KYT or S.H.E.P.H.E.R.D) improves accuracy and reduces errors compared to a single general-purpose LLM.
2. **Human-in-the-loop matters for sensitive domains** — in finance or security, the AI agent gathers, analyzes, and recommends, while a human retains the final decision.
3. **Transparency and citations build trust** — enterprise AI applications need clear evidence trails (data sources in AML/KYT, standard diagrams in the SA app).
4. **Cost optimization** — combining AWS services with third-party tools (as in Signal Scout) keeps monthly costs manageable across different deployment scales.

### Personal Application Plan

1. Study multi-agent design patterns (task decomposition, agent specialization) for potential use in our product recommendation system's request-handling pipeline.
2. Explore Amazon Bedrock AgentCore as a way to add a natural-language operator interface on top of our existing AWS infrastructure.
3. Apply the human-in-the-loop principle when designing any automated decision component that affects real users or real money.
