---
title: "Week 10"
date: 2026-07-29
weight: 10
chapter: false
pre: " <b> 1.10 </b> "
---

#### Week 10 — Finalising documentation and handover

**Dates:** 03/08 - 09/08/2026

#### Goals

- Complete the bilingual internship report
- Hand over source code and documentation to the team
- Review the full security configuration

#### Work carried out

Completed the English translation of the entire report, reviewing it to ensure
the meaning carried across rather than translating mechanically.

Tidied the GitHub repository: wrote a README describing the architecture and how
to run the system, moved analysis documents into a `docs` folder, and extended
`.gitignore` to exclude config files and build directories.

Ran a final security review: confirmed no access keys existed anywhere in the Git
history, re-checked the IAM role permissions, and verified the S3 bucket was not
directly reachable.

#### Results

- A complete bilingual report covering all seven required sections
- A clean repository with a README and technical documentation
- No sensitive information remaining in the source code

#### Difficulties and how they were resolved

Translation took longer than expected because many technical terms needed careful
word choice. I avoided automated translation for the architectural reasoning,
where it easily distorts meaning.
