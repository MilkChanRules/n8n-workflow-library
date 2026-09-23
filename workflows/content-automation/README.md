# Content Automation Shell - Repurpose and Schedule

## Purpose
A starting skeleton for a scheduled content-repurposing pipeline: pull a piece of source content, reformat it for another channel, and queue/publish it. Import this and swap the placeholder nodes for real ones as you build out a specific repurposing flow.

## Trigger
Schedule Trigger, set to run once a day by default. **The workflow is inactive on import** — activate once the real nodes are wired up.

## Nodes / Flow overview
1. **Schedule Trigger** fires on the configured interval
2. **1. Fetch Source Content** (placeholder `NoOp`) — replace with a node pulling the next piece due for repurposing (blog RSS, a content calendar sheet, a Notion database, etc.)
3. **2. Repurpose Content** (placeholder `NoOp`) — replace with a `Code` or AI node that reformats the content (e.g. blog post → tweet thread, LinkedIn post, or newsletter blurb)
4. **3. Schedule and Publish** (placeholder `NoOp`) — replace with the node that queues or publishes it (Buffer, a social platform's API, or a `Set` node for manual review before posting)

A sticky note on the canvas repeats this so it's visible without opening this README.

## Required credentials & services
_None yet — add these once the placeholder nodes are replaced with real ones (e.g. Buffer API key, social platform credentials, OpenAI key)._

## Setup instructions
1. In n8n: **Workflows → Import from File** and select `content-automation-shell.json`
2. Rename the workflow to describe the actual flow (e.g. "Blog → LinkedIn + Twitter Repurposer")
3. Replace each numbered placeholder node with a real node
4. Update the Schedule Trigger's interval if daily isn't right for this flow
5. Test with **Execute Workflow** before activating
6. Activate the workflow once it's working end to end

## Notes / gotchas
- The `NoOp` placeholder nodes exist purely to hold position and label on the canvas — they don't do anything. Delete them as you wire in real nodes, keeping the connections intact.
- If repurposing uses an AI node, consider adding a manual-review step before publishing rather than posting fully automated content straight to a public channel.
