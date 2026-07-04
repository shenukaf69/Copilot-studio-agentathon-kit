# Audit & Reporting Q&A Copilot

Answers journal/variance/control-exception questions with citations, and lets auditors formally flag findings.

**Guide:** `Audit_Reporting_QA_Copilot_Full_Build_Guide.pdf`
**Sample data:** `Finance_Audit_Data.xlsx`
**Also included:**
- `AuditFindings_SharePointList_Template.xlsx` — SharePoint list import template
- `AuditFindingRaised_AdaptiveCard.json` — Teams adaptive card with {{Placeholder}} tokens

## Workloads used

- Microsoft Copilot Studio
- SharePoint Online
- Microsoft Teams

## Licenses required

- Copilot Studio
- SharePoint Online
- Microsoft Teams

## Permissions required

- Environment Maker on the target environment
- Contribute access on the SharePoint site hosting the "Audit Findings" list
- Permission to post to the Finance Controls Teams channel

## Connectors used in this build

- SharePoint
- Microsoft Teams

> **Note:** Import the SharePoint list template via New → List → From Excel — no need to build the list from scratch.

---

Part of the [Copilot Studio Agent-a-thon Kit](../README.md). See the root README for the full prerequisites table across all 12 scenarios.
