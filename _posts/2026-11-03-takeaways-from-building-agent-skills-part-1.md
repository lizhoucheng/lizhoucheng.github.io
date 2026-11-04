---
layout: post
title: "Takeaways from Building Agent Skills — Part 1"
date: 2026-11-03 00:00:00 -0800
---

Recently, I dive my head into building some AI skills, and pick up a few observations and learnings along the way:

## 1. Trust Evals, Not Intuition

When building a skill, it's easy to feel that it's useful. But intuition can be misleading.

I've found that the actual improvement from a skill can sometimes be much smaller than expected. I learned this from running evals and compare performance **with and without the skill**.

Beyond task success, it's also worth considering token usage, latency, and execution cost. A skill that improves accuracy slightly but significantly increases cost may not always be worth the added complexity.

Don't just assume a skill adds value just because it is built. Measure the improvement it actually provides.

## 2. Balance Scripts and LLM-Driven Execution

When designing a skill, one decision is which parts of its workflow should be handled by scripts and which should be left to the LLM.

For well-defined, deterministic operations, scripts can reduce unnecessary model interactions, token usage, and execution variability.

However, there are trade-offs:

- **Correctness:** Deterministic doesn't necessarily mean correct. Scripts need to be well-tested, especially for edge cases.
- **Maintenance:** Scripts encode assumptions about APIs and workflows that may become outdated as things evolve.
- **Flexibility:** Hardcoded workflows may limit the LLM's ability to adapt to unexpected situations or explore alternative approaches.

The right balance depends on the task. Sometimes it's better to let the LLM reason through a problem; other times, a script is more efficient and reliable. The goal isn't simply to minimize LLM calls, but to balance reliability, flexibility, execution cost, and maintenance.
