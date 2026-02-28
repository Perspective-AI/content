---
title: "Data Retention & Privacy"
description: "Draft policy for transcripts, highlights, and exports."
nav_order: 4
---

Use this page to align legal, security, and research teams on how Perspective data is stored.

## Retention defaults (adjust once product team confirms)

- **Transcripts:** 365 days rolling. Archive or delete sooner for high-sensitivity programs.
- **Highlights & charts:** Persist until manually removed; tag with owner + review date.
- **Uploads (participant lists, CSVs):** Deleted automatically after processing.
- **API/Webhook logs:** 30 days for troubleshooting.

## Recommended controls

1. **Tag PII at ingestion.** Use outline instructions to keep sensitive responses in structured fields.
2. **Use workspace-level encryption keys** if BYOK is available.
3. **Restrict exports** to S3 buckets with lifecycle policies; avoid email attachments.
4. **Document DSAR process**: how to locate/delete an individual’s transcript when requested.
5. **Schedule trust reviews** monthly to spot spam/bot responses before they hit downstream systems.

## Compliance references

- SOC 2 Type II + ISO 27001 attestations are stored in `/assets/compliance/` (link here once public).
- Data Processing Agreement template: link TBD.

## Incident response basics

| Step | Owner |
| --- | --- |
| Identify abnormal access/export | Security/ops monitors | 
| Lock affected workspace (read-only) | Admin | 
| Notify legal + impacted customers | Exec sponsor | 
| Document in incident log | Security | 

Fill in the exact owners and tooling once the security team finalizes the playbook.
