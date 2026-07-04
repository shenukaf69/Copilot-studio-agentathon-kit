# HR People Operations Copilot

Lets employees self-serve HR questions and book leave in conversation; gives HR partners workforce insight.

**Guide:** `HR_People_Operations_Copilot_Full_Build_Guide.pdf`
**Sample data:** `HR_People_Operations_Data.xlsx`
**Also included:**
- `LeaveRequests_SharePointList_Template.xlsx` — SharePoint list import template
- `LeaveRequest_AdaptiveCard.json` — Teams adaptive card with {{Placeholder}} tokens

## Workloads used

- Microsoft Copilot Studio
- SharePoint Online
- Microsoft Teams
- Microsoft Entra ID (manager lookup)

## Licenses required

- Copilot Studio
- SharePoint Online
- Microsoft Teams

## Permissions required

- Environment Maker on the target environment
- Contribute access on the SharePoint site hosting the "Leave Requests" list
- Permission to post to the employee's manager in Teams

## Connectors used in this build

- SharePoint
- Office 365 Users (Get manager)
- Microsoft Teams

> **Note:** This is the one scenario with ready-made downloadable prerequisites: LeaveRequests_SharePointList_Template.xlsx (import via SharePoint's "New → List → From Excel") and LeaveRequest_AdaptiveCard.json (paste into the Teams action).

---

Part of the [Copilot Studio Agent-a-thon Kit](../README.md). See the root README for the full prerequisites table across all 12 scenarios.
