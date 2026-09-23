# Client Onboarding Shell - New Client Kickoff

## Purpose
A starting skeleton for onboarding a new client the moment they sign: create their record, send a welcome sequence, and spin up the standard onboarding task checklist for the team. Import this and swap the placeholder nodes for real ones as you build out a specific onboarding flow.

## Trigger
Webhook Trigger, listening at `/new-client` for a POST request (e.g. fired from a signed-contract or payment event). **The workflow is inactive on import** — activate once the real nodes are wired up, then n8n will give you the live webhook URL.

## Nodes / Flow overview
1. **Webhook Trigger** fires when a new client signs / pays
2. **1. Create Client Record** (placeholder `NoOp`) — replace with a CRM or project-tool node (HubSpot, Notion, Airtable) that creates the client's record
3. **2. Send Welcome Sequence** (placeholder `NoOp`) — replace with an Email/Gmail node sending a welcome email with next steps and kickoff info
4. **3. Create Onboarding Tasks** (placeholder `NoOp`) — replace with a project-management node (Asana, ClickUp, Trello) that creates the standard onboarding checklist for the team

A sticky note on the canvas repeats this so it's visible without opening this README.

## Required credentials & services
_None yet — add these once the placeholder nodes are replaced with real ones (e.g. CRM API key, email account, project tool credentials)._

## Setup instructions
1. In n8n: **Workflows → Import from File** and select `client-onboarding-shell.json`
2. Rename the workflow to describe the actual flow (e.g. "New Client Onboarding: Contract Signed → HubSpot + Asana")
3. Replace each numbered placeholder node with a real node
4. Update the webhook path if `/new-client` isn't right for this flow
5. Test with **Execute Workflow** using a sample payload before activating
6. Activate the workflow once it's working end to end, then wire whatever fires it (a form, e-signature tool, payment webhook) to the live webhook URL

## Notes / gotchas
- The `NoOp` placeholder nodes exist purely to hold position and label on the canvas — they don't do anything. Delete them as you wire in real nodes, keeping the connections intact.
- If this fires from a payment or e-signature provider, double check their webhook payload shape before mapping fields into the downstream nodes.
