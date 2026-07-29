---
title: "Self-evaluation"
date: 2026-07-29
weight: 6
chapter: false
pre: " <b> 6. </b> "
---

#### Self-evaluation summary

| Criterion | Level | Comment |
|---|---|---|
| Knowledge | Good | Solid on serverless, weaker on networking and containers |
| Learning ability | Strong | Reads primary documentation rather than hunting for ready answers |
| Initiative | Strong | Proposed the data improvement when the model underperformed |
| Discipline | Good | Kept to schedule, though the first two weeks lacked direction |
| Communication | Good | Able to explain infrastructure concepts to non-specialists |
| Teamwork | Fair to good | Fell short on agreeing data conventions at the start |
| Problem solving | Good | Clear improvement in diagnosing faults layer by layer |
| Contribution to the project | Strong | Owned all infrastructure and architectural decisions |

#### Detailed comments

**Knowledge — Good**

Before the internship my understanding of cloud computing stopped at the
conceptual level. By the end I had deployed a complete system of seven
interconnected AWS services, and more importantly I could explain **why** each
service was chosen over the alternatives. For instance, I can argue why DynamoDB
suited this problem better than RDS, and why the CLIP model could not go on
Lambda.

My weak area is networking. The serverless architecture meant I barely touched
VPCs, subnets or security groups. This is a gap I need to close myself.

**Learning ability — Strong**

The programme runs on self-study with no step-by-step guidance. I found this hard
at first, being used to detailed instructions, but it forced me to read official
AWS documentation instead of looking for ready-made answers.

I also came to see the difference between making a system work and understanding
why it works. There were parts I built by following a guide where everything ran
correctly, yet when something broke I had no idea where to start. I then spent
time re-reading the code and rebuilding small components myself.

**Initiative — Strong**

When the first recommendation model performed poorly, I did not simply report the
numbers. I analysed the cause, found the problem lay in the uniformly random
data, and proposed and implemented a regenerated dataset simulating real
behaviour. Metrics improved by 2.8 to 5.9 times.

I also set up budget alerts and ran a security review without being asked.

**Discipline — Good**

I kept to the planned schedule and hit the milestones on time. However, my first
two weeks of study lacked direction because no project had been chosen yet,
wasting time. If I did this again I would settle the topic sooner so the learning
had focus.

**Communication — Good**

The Cloud Architect role required working with teammates from different
specialities. I had to explain infrastructure concepts in plain language to
someone unfamiliar with AWS terminology, and conversely understand requirements
from the frontend and data sides. This is a skill I can perform but have not yet
mastered.

**Teamwork — Fair to good**

What I did well was spotting early that the frontend and backend data contracts
had diverged, and choosing an adapter layer rather than making both sides patch
each other, preserving the tested work on both sides.

What I did poorly was failing to agree data conventions with the whole team from
the start. As a result our data engineer's pipeline produced identifiers that did
not match the real catalogue, so its output could not be loaded into the model,
and she had to raise it before I noticed. This was my shortcoming as architect,
since defining the data interfaces between components was my responsibility.

**Problem solving — Good**

Early on, when something failed I would try things at random until it worked, and
still not know why. Over time I built the habit of reading error messages
carefully, identifying which layer had failed, then testing each layer from the
inside out.

One example: after uploading a new build to S3 the site rendered blank. I spent a
long time checking code before realising CloudFront was serving a cached old
version. Next time I saw those symptoms, I checked cache first.

A harder example: DynamoDB does not guarantee results in the order keys are
passed in, so the model's ranking was being lost. This produced no error message
and was only detectable by carefully comparing the returned data.

**Contribution to the project — Strong**

I owned the entire AWS infrastructure and the architectural decisions, deployed
my teammates' code to the live environment, built the adapter layer resolving the
data contract mismatch, set up and improved the recommendation engine, and
managed security and cost.

The contribution I value most is not the number of services deployed, but
identifying that the problem lay in the data rather than the algorithm, and
proving it with quantitative evidence.

#### Development plan

I plan to study towards the **AWS Solutions Architect Associate** certification
and rebuild a small project from scratch to test what I have learned. For my weak
areas I will focus on AWS networking and container services such as ECS and EKS.
