# Customer Service Insights Copilot

Lets agents triage and escalate cases in conversation while giving managers real-time SLA/CSAT visibility.

**Guide:** `Customer_Service_Insights_Copilot_Full_Build_Guide.pdf`
**Sample data:** `Customer_Service_Cases_Data.xlsx`
**Also included:**
- `CaseEscalated_AdaptiveCard.json` — Teams adaptive card with {{Placeholder}} tokens

## Workloads used

- Microsoft Copilot Studio
- Dynamics 365 Customer Service
- Microsoft Teams
- Microsoft Entra ID (manager lookup)

## Licenses required

- Copilot Studio
- Dynamics 365 Customer Service
- Microsoft Teams (included in most Microsoft 365 plans)

## Permissions required

- Environment Maker on the target environment
- Read/write access to the incident table in Dynamics 365
- Permission to post to the on-call manager in Teams

## Connectors used in this build

- Dynamics 365
- Office 365 Users (Get manager)
- Microsoft Teams

> **Note:** Step 6 builds an agent flow (not a direct connector) because escalation needs two actions: updating the case record and notifying a manager.

---

Part of the [Copilot Studio Agent-a-thon Kit](../README.md). See the root README for the full prerequisites table across all 12 scenarios.
