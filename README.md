# n8n Workflow Library

A curated collection of production-ready n8n workflows built for AI-powered business automation — lead generation, content automation, client onboarding, and data syncing.

Each workflow is exported as a ready-to-import `.json` file, documented with its trigger, node breakdown, and setup steps, so anyone can drop it into their own n8n instance and adapt it.

## Why this exists

Built as part of my AI automation agency work — this repo doubles as proof-of-work for clients/recruiters and a personal reference library so I'm not rebuilding the same automations from scratch.

## Structure

```
workflows/
  lead-generation/      # Capturing, scoring, and routing new leads
  content-automation/   # Repurposing and scheduling content across channels
  client-onboarding/    # Automated onboarding sequences for new clients
  data-sync/            # Keeping data consistent across tools (CRM, sheets, etc.)
docs/
  workflow-template.md  # Template used to document each workflow
```

## How to use a workflow

1. Open the workflow's folder and read its `README.md` for what it does and what credentials/services it needs.
2. In n8n: **Workflows → Import from File** and select the `.json`.
3. Update credentials and any hardcoded IDs (webhook URLs, sheet IDs, etc.) to match your own setup.

## Workflows

| Workflow | Category | Status |
|---|---|---|
| [Data Sync Shell](workflows/data-sync/data-sync-shell.json) | data-sync | Shell (placeholders, ready to extend) |
| [Lead Generation Shell](workflows/lead-generation/lead-generation-shell.json) | lead-generation | Shell (placeholders, ready to extend) |
| [Content Automation Shell](workflows/content-automation/content-automation-shell.json) | content-automation | Shell (placeholders, ready to extend) |
| [Client Onboarding Shell](workflows/client-onboarding/client-onboarding-shell.json) | client-onboarding | Shell (placeholders, ready to extend) |

## Roadmap

- [x] Shell workflow added for each of the four categories (data-sync, lead-generation, content-automation, client-onboarding)
- [ ] Replace placeholder nodes in at least one shell with a fully working, real-world version
- [ ] Add a short demo GIF/screenshot per completed workflow

## License

MIT
