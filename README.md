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

## Roadmap

- [ ] Migrate first existing agency workflow into this structure
- [ ] Add 2–3 more workflows across different categories
- [ ] Add a short demo GIF/screenshot per workflow

## License

MIT
