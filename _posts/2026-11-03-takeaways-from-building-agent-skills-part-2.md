---
layout: post
title: "Takeaways from Building Agent Skills — Part 2"
date: 2026-11-03 00:01:00 -0800
---

## 3. Domain Knowledge and Mental Models May Add More Value Than Documentation

During skill evaluation, I noticed an interesting pattern: **the largest improvements often came from tasks requiring domain knowledge or specific mental models**, rather than straightforward API lookups.

My hypothesis is that LLMs can already retrieve much of the API information they need through existing tools, such as MCP servers. Simply repeating that information in a skill may not provide much incremental value.

What seems more valuable is encoding knowledge that helps the agent approach problems differently. The domain-specific reasoning and practical insights that aren't easily found in API references.

Focus on knowledge that meaningfully extends the agent's existing capabilities, rather than simply providing more information.

## 4. Evaluate with Realistic User Prompts

When writing evals, it's tempting to craft prompts that clearly describe the intended task or explicitly mention the skill.

But real users don't necessarily know which skills exist, and they may describe their problems in unexpected ways.

If eval prompts are overly tailored to trigger a skill, the results may overestimate its real-world usefulness.

It's important to evaluate **whether the skill gets triggered appropriately** aside from its functional gain.

Realistic user prompts, along with carefully designed edge cases, can help reveal issues that idealized tests might miss.
