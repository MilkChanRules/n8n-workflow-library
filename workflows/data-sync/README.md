# Data Sync Shell - [Source] to [Destination]

## Purpose
A starting skeleton for any scheduled data-sync workflow: pull data from one system, reshape it, and push it into another. Import this and swap the placeholder nodes for real ones as you build out a specific sync (e.g. CRM → Google Sheets, Airtable → Postgres).

## Trigger
Schedule Trigger, set to run every 1 hour by default. **The workflow is inactive on import** — flip it on once the real nodes are wired up.

## Nodes / Flow overview
1. **Schedule Trigger** fires on the configured interval
2. **1. Fetch Source Data** (placeholder `NoOp`) — replace with whatever pulls from the source (HTTP Request, Google Sheets, Postgres, etc.)
3. **2. Transform / Map Fields** (placeholder `NoOp`) — replace with a `Set` or `Code` node that reshapes the data into the destination's expected format
4. **3. Write to Destination** (placeholder `NoOp`) — replace with the node that writes to wherever the data is going

A sticky note on the canvas repeats this so it's visible without opening this README.

## Required credentials & services
_None yet — add these once the placeholder nodes are replaced with real ones._

## Setup instructions
1. In n8n: **Workflows → Import from File** and select `data-sync-shell.json`
2. Rename the workflow to describe the actual sync (e.g. "Sync: Airtable Leads → Google Sheet")
3. Replace each numbered placeholder node with a real node for your source/destination
4. Update the Schedule Trigger's interval if hourly isn't right for this sync
5. Test with **Execute Workflow** before activating
6. Activate the workflow once it's working end to end

## Notes / gotchas
- The `NoOp` placeholder nodes exist purely to hold position and label on the canvas — they don't do anything. Delete them as you wire in real nodes, keeping the connections intact.
- Since this is a shell, there's nothing to break by importing it — it won't run until both activated and given real logic.
