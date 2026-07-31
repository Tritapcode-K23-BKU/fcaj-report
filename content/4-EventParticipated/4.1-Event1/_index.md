---
title: "Event 3"
date: 2026-06-06
weight: 4
---

## Internal Tech Seminar — 6 Topics (June 6, 2026)

**Format:** Internal knowledge-sharing session
**Scope:** Infrastructure, Cloud, AI, Game Dev, Soft Skills
**Number of talks:** 6
**Date:** June 6, 2026

I attended an internal tech seminar covering six presentations spanning infrastructure, applied AI/ML, serverless architecture, application packaging, and team collaboration skills. Below is a summary of the key takeaways from each talk.



### Talk 1 — AWS WAF & ML-based NIDS
**Speaker:** Le Hoang Gia Dai

Traditional WAFs rely on fixed rule sets and often miss zero-day attacks or novel behavioral variants. The speaker trained a LightGBM model on the CSE-CIC-IDS2018 dataset, reaching 0.9586 accuracy in classifying malicious network behavior, and integrated it with AWS Lambda, Kinesis Data Firehose, and Security Hub to analyze traffic and trigger automated security responses in real time.

**Takeaway:** Moving from reactive, rule-based security to proactive AI/ML-driven detection significantly improves zero-day threat coverage on cloud infrastructure.

### Talk 2 — Docker & Containerization
**Speaker:** Bao Huynh

Containers are far lighter than VMs — millisecond startup and shared host kernel keep resource usage minimal. The standard workflow: define the environment in a `Dockerfile` → build an immutable image → run consistent, isolated containers. This underpins microservices architecture and CI/CD pipelines, enabling "build once, run anywhere" and closing the dev/prod environment gap.

**Takeaway:** Containerization is now the baseline standard for packaging, deploying, and scaling modern software.

### Talk 3 — From IT Helpdesk to Senior Sysadmin
**Speaker:** Tran Trung Vinh

A career path from Helpdesk (troubleshooting and user communication) to professional Sysadmin and Cloud/DevOps Engineer. Core sysadmin mindset: automate repetitive work, document processes, and never test directly in production. Moving into cloud/DevOps means shifting from managing physical servers to auto-scaling, pay-as-you-go infrastructure and Infrastructure as Code (IaC). The speaker's advice: prioritize hands-on project experience over collecting certifications.

**Takeaway:** Communication skills, automation mindset, and real-world experience are the keys to sustainable growth in infrastructure roles.

### Talk 4 — Multiplayer with AWS WebSockets in Godot
**Speaker:** Nguyen Quoc Bao

A serverless multiplayer architecture combining the Godot game engine with AWS: API Gateway (WebSocket) for persistent two-way connections, Lambda for game logic, and DynamoDB for player state. The talk compared UDP (fast-paced action games) versus WebSocket (turn-based games, lobbies, in-game chat), and covered practical issues like handling stale connections and minimizing costly DynamoDB scan operations.

**Takeaway:** Serverless plus WebSocket enables multiplayer games with low upfront operating cost and flexible auto-scaling.

### Talk 5 — The Art of Effective Teamwork
**Speaker:** Truong Huy Phuoc

Four golden rules: (1) define a clear, measurable shared goal; (2) place the right person in the role that fits their strengths; (3) communicate openly and listen actively; (4) build individual accountability toward the shared product. The talk also covered tooling for transparent workflow management — Trello, Slack, Discord, ClickUp.

**Takeaway:** Strong technical skill is necessary but not sufficient — collaboration habits and communication discipline are what determine project success.

### Talk 6 — GraphRAG with Amazon Bedrock and Neptune
**Speaker:** Viet Phat

GraphRAG improves on traditional RAG through multi-hop reasoning and by exploiting semantic relationships between entities via a knowledge graph. Two deployment paths on AWS were presented: (1) a managed approach using Amazon Bedrock Knowledge Bases with Neptune Analytics for fast deployment, and (2) a custom pipeline built with LlamaIndex plus Amazon Neptune for deeper customization.

**Takeaway:** Knowledge graphs are a meaningful step up in accuracy and reasoning quality for complex enterprise generative AI applications.

---

### Personal Application Plan

**Short term (1–2 months)**
- Practice packaging personal/current projects with Docker and Docker Compose to standardize the dev environment.
- Apply project management tools (Trello/ClickUp) to team collaboration using the 4 golden rules above.

**Medium term (3–6 months)**
- Study AWS Lambda + API Gateway WebSocket integration for real-time data use cases.
- Explore LightGBM and basic ML models for system log analysis.

**Long term (6–12 months)**
- Build an experimental GraphRAG + LlamaIndex setup for internal knowledge management.
- Build an Infrastructure-as-Code mindset in preparation for a DevOps/Cloud Engineer career path.

![Attendance photo](/fcaj-report/static/images/4-Events/events-seminar-1.jpg)