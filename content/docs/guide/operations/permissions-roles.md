---
title: "Roles & Permissions"
description: "Who can edit outlines, launch agents, and access transcripts."
nav_order: 2
nav_display: false
---

Use this draft to define access policy before handing Perspective to more teams.

## Default roles

| Role        | Capabilities                                                              | Recommended owners              |
| ----------- | ------------------------------------------------------------------------- | ------------------------------- |
| **Owner**   | Manage billing, create/delete workspaces, generate API/MCP tokens.        | Executive sponsor, head of ops. |
| **Admin**   | Invite users, assign roles, edit any outline/agent, view all transcripts. | Research ops, CX ops.           |
| **Builder** | Create/edit outlines, manage agents they own, view insights.              | Product managers, researchers.  |
| **Analyst** | View transcripts, highlights, dashboards; cannot change outlines.         | Analysts, customer insights.    |
| **Viewer**  | Read-only access to highlights/shared dashboards.                         | Leadership, stakeholders.       |

Adjust names to match your actual RBAC implementation—this page is the placeholder narrative.

## Best practices

1. **Segregate workspaces.** Keep sandbox/testing work separate from production data.
2. **Least privilege.** Default new collaborators to Analyst unless they need edit powers.
3. **Ownership fields.** Document an owner + backup on every outline/agent to avoid abandoned flows.
4. **Transcript privacy.** Limit full transcript access to roles who need PII for QA.
5. **Audit cadence.** Review membership quarterly; auto-remove suspended SSO accounts.

## Implementation checklist

- [ ] Publish an internal policy describing roles + escalation path.
- [ ] Automate provisioning via SCIM/IdP group mapping (if available).
- [ ] Enable alerts when admins generate new API/MCP tokens.
- [ ] Create a shared “Ops” dashboard to monitor launches across workspaces.
