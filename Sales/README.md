# Sales Pipeline Copilot

Gives sellers and managers pipeline insight and lets them update CRM deal stages in conversation.

**Guide:** `Sales_Pipeline_Copilot_Full_Build_Guide.pdf`
**Sample data:** `Sales_Pipeline_Data.xlsx`

## Workloads used

- Microsoft Copilot Studio
- Microsoft Dataverse (Dynamics 365 Sales)

## Licenses required

- Copilot Studio (message-capacity licensing)
- Dynamics 365 Sales, or a standalone Dataverse database entitlement

## Permissions required

- Environment Maker on the target Power Platform environment
- Read/write access to the Opportunity table in Dataverse

## Connectors used in this build

- Dataverse — used directly as a connector tool, no agent flow required

> **Note:** This is the simplest build in the kit: the tool is a single native connector action, so Step 6 skips flow-building entirely.

---

Part of the [Copilot Studio Agent-a-thon Kit](../README.md). See the root README for the full prerequisites table across all 12 scenarios.
