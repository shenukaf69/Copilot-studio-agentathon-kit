# Store Ops Daily Copilot

Gives store managers today's numbers vs target and drafts/sends the daily stand-up note.

**Guide:** `Store_Ops_Daily_Copilot_Full_Build_Guide.pdf`
**Sample data:** `Consumer_StoreOps_Data.xlsx`
**Also included:**
- `StoreOpsArchive_SharePointList_Template.xlsx` — SharePoint list import template
- `StandupPosted_AdaptiveCard.json` — Teams adaptive card with {{Placeholder}} tokens

## Workloads used

- Microsoft Copilot Studio
- Microsoft Teams
- SharePoint Online

## Licenses required

- Copilot Studio
- Microsoft Teams
- SharePoint Online

## Permissions required

- Environment Maker on the target environment
- Membership in each store's Teams channel (to post as the flow bot)
- Contribute access on the SharePoint site hosting the archive list

## Connectors used in this build

- Microsoft Teams
- SharePoint

> **Note:** Import the SharePoint archive list template via New → List → From Excel — no need to build the list from scratch.

---

Part of the [Copilot Studio Agent-a-thon Kit](../README.md). See the root README for the full prerequisites table across all 12 scenarios.
