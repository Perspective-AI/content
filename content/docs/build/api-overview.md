---
title: "API Overview (Draft)"
description: "Authentication, base URLs, and core resources."
nav_order: 2
nav_display: false
---

> Draft placeholder — update once the public API surface is stable.

## Base information

- **Base URL:** `https://api.getperspective.ai/v1` (confirm before publishing)
- **Auth:** Bearer token (workspace-scoped). Generate tokens in Settings → API.
- **Rate limits:** 60 requests/min per token. 429 responses include `Retry-After` header.

## Core resources (planned)

| Resource         | Methods          | Description                                    |
| ---------------- | ---------------- | ---------------------------------------------- |
| `/outlines`      | GET, POST, PATCH | List, create, and update interview outlines.   |
| `/agents`        | GET, POST, PATCH | Manage concierge/interviewer/evaluator agents. |
| `/conversations` | GET              | Fetch transcripts, metadata, trust scores.     |
| `/invites`       | POST             | Trigger invites or send reminders.             |
| `/highlights`    | GET, POST        | Publish or retrieve highlight pages.           |

## Sample request

```bash
curl https://api.getperspective.ai/v1/outlines \
  -H "Authorization: Bearer $PERSPECTIVE_TOKEN" \
  -H "Content-Type: application/json"
```

## Error model

```json
{
  "error": {
    "code": "outline_not_found",
    "message": "Outline 123 not found in workspace abc"
  }
}
```

## Next steps

- Add Postman collection + OpenAPI spec.
- Document pagination/filtering behavior.
- Include examples for each language SDK once published.
