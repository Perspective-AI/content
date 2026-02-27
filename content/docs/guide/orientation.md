---
title: "Perspective in an Hour"
description: "High-level mental model of agents, outlines, insights, and governance."
nav_order: 0
---

Use this checklist to understand how Perspective fits together before you dive into individual guides.

## 1. Core building blocks

| Concept | What it is | Why it matters |
| --- | --- | --- |
| **Outlines** | Structured prompts and logic that define each interview/concierge flow. | Keeps conversations on-brand and compliant. |
| **Agents** | Runtime personalities (Concierge, Interviewer, Evaluator) that deliver the outline. | Each one is optimized for a specific job and routing. |
| **Insights** | Highlight pages, charts, exports, and downstream triggers. | Converts raw interviews into artifacts a team can act on. |
| **Governance** | Workspaces, roles, data policies. | Ensures the right people can launch/edit while keeping PII protected. |

## 2. Typical program lifecycle

1. **Define the moment.** Decide whether you need intake triage, research depth, or evaluation scoring.
2. **Clone/author an outline.** Start from a template, add guardrails, and note required fields.
3. **Choose the agent.** Match the outline to Concierge (forms), Interviewer (research), or Evaluator (post-interaction scores).
4. **Invite/route participants.** Upload a list, embed in-product, or trigger via automation.
5. **Monitor conversations live.** Spot-check transcripts, trust scores, and completion metrics.
6. **Synthesize.** Use highlights, dashboards, and shared links to circulate learning.
7. **Close the loop.** Trigger CRM tasks, Jira issues, or email follow-ups using automations/Webhooks.

## 3. Implementation roles

- **Program owner (Product/CX).** Owns outlines, QA, and outcomes.
- **Research ops / Enablement.** Standardizes templates, maintains tags, trains new teams.
- **Developers.** Wire Perspective into existing systems (auth, embeds, MCP, data plane).
- **Admins.** Manage workspaces, billing, and compliance reviews.

Understanding who does what up front avoids “shadow launches” and keeps data clean.

## 4. Environment map

- **Production workspace** for live traffic.
- **Sandbox workspace** for experimentation (clone outlines here first).
- **API/MCP tokens** scoped per workspace; rotate every 90 days.

## 5. Success checklist

- [ ] Single source of truth for outlines (versioning + owners)
- [ ] Alerting on failed invites, agent errors, or webhook retries
- [ ] Quarterly review of highlight library (archive stale ones)
- [ ] Documented “human takeover” rules for concierge agents
- [ ] Privacy review covering transcript retention + export policy

Once you grasp this map, jump into [Getting Started](/docs/guide/getting-started/) to launch your first flow.
