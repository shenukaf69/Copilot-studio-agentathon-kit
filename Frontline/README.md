# Frontline Shift Handover Copilot

Captures shift handovers and logs safety incidents in conversation, built for hand-held devices.

**Guide:** `Frontline_Shift_Handover_Copilot_Full_Build_Guide.pdf`
**Sample data:** `Frontline_Shifts_Data.xlsx`
**Also included:**
- `SafetyIncidents_DataverseImport_Template.xlsx` — Dataverse table import template
- `SafetyIncidentLogged_AdaptiveCard.json` — Teams adaptive card with {{Placeholder}} tokens

## Workloads used

- Microsoft Copilot Studio
- Microsoft Dataverse (custom table)
- Microsoft Teams

## Licenses required

- Copilot Studio
- Dataverse database entitlement (a Power Apps per-app or per-user plan may be required for a custom table, depending on your tenant)
- Microsoft Teams

## Permissions required

- Environment Maker on the target environment
- System Customizer role (or higher) in Power Apps — needed to create the "SafetyIncidents" table
- Permission to post to the site Safety Officer in Teams

## Connectors used in this build

- Dataverse
- Microsoft Teams

> **Note:** This is the only scenario requiring a brand-new Dataverse table (not just a SharePoint list). Use the provided workbook with Power Apps' Tables → New table → Import from Excel to create it in one step.

---

Part of the [Copilot Studio Agent-a-thon Kit](../README.md). See the root README for the full prerequisites table across all 12 scenarios.
