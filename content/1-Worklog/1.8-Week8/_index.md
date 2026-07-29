---
title: "Week 8"
date: 2026-07-29
weight: 8
chapter: false
pre: " <b> 1.8 </b> "
---

#### Week 8 — Data improvement and retraining

**Dates:** 20/07 - 26/07/2026

#### Goals

- Analyse why the model performed poorly
- Build a dataset simulating realistic shopping behaviour
- Retrain and compare metrics across both versions
- Handle a security incident arising during code handover

#### Work carried out

Re-examined the first dataset and identified the cause: collaborative filtering
works by finding groups of users who behave alike. If everyone interacts at
random, no such groups exist. Changing the algorithm would not solve this.

Rewrote the data generator to simulate five properties of real behaviour:
browsing sessions, a view to add-to-cart to purchase funnel, a power-law
distribution, time-of-day rhythms, and user segments with different tastes. The
result was 23,377 interactions across 200 users.

Retrained on the same recipe and compared metrics against the previous version.
Switched the campaign to the new solution version.

During code handover, I discovered a source archive shared through cloud storage
contained a config file with an AWS access key. I revoked the key immediately and
changed the handover process.

#### Results

Metrics improved substantially across every measure:

| Metric | Data v1 | Data v2 | Improvement |
|---|---|---|---|
| Precision@5 | 0.0889 | 0.4348 | 4.9x |
| NDCG@10 | 0.1799 | 0.6512 | 3.6x |
| MRR@25 | 0.1216 | 0.7130 | 5.9x |
| Coverage | 0.8218 | 0.9505 | +15.7% |

Conclusion: training data quality determines model performance more than
algorithm choice.

#### Difficulties and how they were resolved

The leaked access key was the most memorable lesson. The impact was low because
the key was read-only, which was itself the result of applying least privilege
from the start. The lesson: the principle does not prevent mistakes, but it
determines how much damage they cause. The team moved to centralised source
control on Git instead of sharing archives.
