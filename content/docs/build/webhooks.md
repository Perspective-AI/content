---
title: "Webhooks & Automations"
description: "Subscribe to conversation and highlight events."
nav_order: 3
nav_display: false
---

> Draft placeholder — verify payloads before publishing externally.

## Event types

| Event                    | Trigger                                                |
| ------------------------ | ------------------------------------------------------ |
| `conversation.completed` | Interview or concierge session ends.                   |
| `highlight.published`    | A highlight page is set to public or updated.          |
| `trust.alert`            | Conversation flagged for low-quality or risky content. |

## Configure a webhook endpoint

1. Create an HTTPS endpoint that accepts POST requests.
2. In Perspective → Settings → Automations → Webhooks, add the URL and select events.
3. Copy the signing secret; store as `PERSPECTIVE_WEBHOOK_SECRET`.

## Payload example

```json
{
  "id": "evt_123",
  "type": "conversation.completed",
  "created": "2026-02-27T19:10:00Z",
  "data": {
    "conversation_id": "conv_abc",
    "outline_id": "outline_xyz",
    "agent_type": "concierge",
    "participant": {
      "email": "alex@example.com"
    },
    "summary_url": "https://getperspective.ai/highlights/abc"
  }
}
```

Verify signatures using `X-Perspective-Signature` header (HMAC-SHA256 of the raw body). Reject requests older than 5 minutes.

## Retry logic

- Perspective retries failed deliveries for 24 hours with exponential backoff.
- Return `2xx` to acknowledge; any other status schedules a retry.

## Common recipes

- Push concierge leads into HubSpot/CRM.
- Create Jira tickets when evaluator scores drop below threshold.
- Trigger Slack alerts for `trust.alert` to let humans review.
  More automation examples are tracked in [Automation Recipes](/docs/build/automation-recipes) (coming soon).
