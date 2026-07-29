---
title: "Self-Assessment"
date: 2026-07-29
weight: 6
chapter: false
pre: " <b> 6. </b> "
---

#### Overview

The internship at First Cloud AI Journey was my first time working with real
cloud infrastructure, where every mistake has real consequences. I have written
this self-assessment honestly, covering both what went well and what did not.

#### Technical knowledge

Before the internship, my understanding of cloud computing stopped at the
conceptual level: I knew the cloud meant renting someone else's servers and I
recognised a few service names, but I had never built a complete system.

By the end, I had deployed a live system on the Internet built from seven
interconnected AWS services. More important than the number of services is that
I understand **why** each one was chosen over the alternatives. For example, I
can explain why DynamoDB rather than RDS suited this problem, and why the CLIP
model could not be deployed to Lambda.

My weakest area is networking. The project used a serverless architecture, so I
barely touched VPCs, subnets or security groups. This is a gap I need to close
on my own.

#### Problem-solving

This is where I improved the most, and also the hardest thing to prove with a
certificate.

Early on, when something failed I would try things at random until it worked,
and afterwards I still would not know why. Over time I built the habit of
reading error messages carefully, identifying which layer the failure belonged
to, then testing each layer from the inside out.

A concrete example: after uploading a new build to S3, the website rendered
blank. I spent a long time checking the source code before realising CloudFront
was still serving the cached old version. The next time I saw similar symptoms,
cache was the first thing I checked.

#### Self-directed learning

The programme runs on self-study with no step-by-step guidance. At first I found
this difficult because I was used to detailed instructions. But it forced me to
read the official AWS documentation instead of hunting for ready-made answers.

I also came to recognise the difference between **making a system work** and
**understanding why it works**. There were parts I built by following a guide
where everything ran correctly, yet when something broke I had no idea where to
start. Later I spent time re-reading the code and rebuilding small components
myself, and my troubleshooting ability improved noticeably.

#### Teamwork

I served as Cloud Architect in a five-person team, responsible for the
infrastructure and architectural decisions, and for deploying my teammates' code
to the live environment.

What I did well was spotting early that the frontend and backend data contracts
had diverged, and choosing an adapter layer rather than making both sides patch
each other. That preserved the already-tested work on both sides.

What I did poorly was **failing to agree on data conventions with the whole team
at the start**. As a result, our data engineer's pipeline produced identifiers
that did not match the real catalogue, so its output could not be loaded into
the model. She had to raise it with me before I noticed. If I did this again, I
would spend the first session of the project writing down the data formats
exchanged between components.

#### Security and cost awareness

While handing over source code, the team accidentally leaked an AWS access key
inside an archive shared through a cloud storage service. The impact was low
because that key had read-only permissions, but it was still a real security
incident.

I took away a lesson that theory cannot teach: the principle of least privilege
does not prevent human error, but it determines how much damage that error
causes. After the incident we moved to centralised source control on Git and
issued individual, scope-limited accounts.

On cost, I learned that not every service bills by usage. A Personalize campaign
bills per hour it exists regardless of query volume. That changed how I think
about cleaning up resources.

#### Self-rating

| Criterion | Level | Notes |
|---|---|---|
| Core AWS service knowledge | Good | Solid on serverless, weak on networking |
| Architecture design | Good | Can weigh trade-offs, no large-scale experience |
| Troubleshooting | Good | Clear improvement over the term |
| Self-directed learning | Strong | Proactively reads primary documentation |
| Teamwork | Fair to good | Fell short on agreeing conventions early |
| Security awareness | Good | Right instincts, needs more care when sharing files |

#### Next steps

I plan to study towards the **AWS Solutions Architect Associate** certification
and to rebuild a small project from scratch to test what I have learned. For my
weak areas, I will focus on AWS networking and container services.
