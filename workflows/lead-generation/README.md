# Lead Generation Shell - Capture, Score, Route

## Purpose
A starting skeleton for capturing a new lead (e.g. from a landing page form), enriching it with extra data, scoring/qualifying it, and routing it to a CRM or notifying sales. Import this and swap the placeholder nodes for real ones as you build out a specific lead-gen flow.

## Trigger
Webhook Trigger, listening at `/new-lead` for a POST request. **The workflow is inactive on import** — activate once the real nodes are wired up, then n8n will give you the live webhook URL to point your form at.

## Nodes / Flow overview
1. **Webhook Trigger** fires when a new lead form is submitted
2. **1. Enrich Lead Data** (placeholder `NoOp`) — replace with an API call (Clearbit, Apollo, etc.) to pull extra info like company size or role
3. **2. Score Lead** (placeholder `NoOp`) — replace with a `Set`/`Code`/`IF` node that applies scoring rules and decides if the lead qualifies
4. **3. Route Lead** (placeholder `NoOp`) — replace with the node that sends the lead onward: a CRM record (HubSpot/Pipedrive), a Slack alert to sales, or a follow-up email

A sticky note on the canvas repeats this so it's visible without opening this README.

## Required credentials & services
_None yet — add these once the placeholder nodes are replaced with real ones (e.g. Clearbit API key, CRM credentials, Slack webhook)._

## Setup instructions
1. In n8n: **Workflows → Import from File** and select `lead-generation-shell.json`
2. Rename the workflow to describe the actual flow (e.g. "New Lead: Landing Page → HubSpot")
3. Replace each numbered placeholder node with a real node
4. Update the webhook path if `/new-lead` isn't right for this flow
5. Test with **Execute Workflow** using a sample payload before activating
6. Activate the workflow once it's working end to end, then wire your form to the live webhook URL

## Notes / gotchas
- The `NoOp` placeholder nodes exist purely to hold position and label on the canvas — they don't do anything. Delete them as you wire in real nodes, keeping the connections intact.
- Webhook workflows only listen while active (or via the test URL while editing) — remember to activate before pointing a real form at it.
