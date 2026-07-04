# Incident Postmortem Copilot

Drafts blameless engineering postmortems and files them as Azure DevOps work items with child action items.

**Guide:** `Incident_Postmortem_Copilot_Full_Build_Guide.pdf`
**Sample data:** `Tech_Incidents_Data.xlsx`
**Also included:**
- `PostmortemFiled_AdaptiveCard.json` — Teams adaptive card with {{Placeholder}} tokens

## Workloads used

- Microsoft Copilot Studio
- Azure DevOps
- Microsoft Teams

## Licenses required

- Copilot Studio
- Azure DevOps (Basic access — free for the first 5 users on most plans, paid beyond that)
- Microsoft Teams

## Permissions required

- Environment Maker on the target environment
- Project-level permission in Azure DevOps to create work items
- An authorized Azure DevOps connection in the flow
- Permission to post to the owning team's Teams channel

## Connectors used in this build

- Azure DevOps
- Microsoft Teams

> **Note:** Confirm your Azure DevOps project has (or can add) an "Incident Postmortem" work item type before Step 6 — the flow also uses a loop to file one child work item per action item.

---

Part of the [Copilot Studio Agent-a-thon Kit](../README.md). See the root README for the full prerequisites table across all 12 scenarios.
