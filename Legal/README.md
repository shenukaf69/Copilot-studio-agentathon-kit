# Legal Contract Review Copilot

Triages contract renewal exposure and kicks off e-signature envelopes in conversation.

**Guide:** `Legal_Contract_Review_Copilot_Full_Build_Guide.pdf`
**Sample data:** `Legal_Contracts_Data.xlsx`

## Workloads used

- Microsoft Copilot Studio
- SharePoint Online
- Microsoft Teams
- DocuSign or Adobe Sign (external SaaS)

## Licenses required

- Copilot Studio
- SharePoint Online
- Microsoft Teams
- An active DocuSign or Adobe Sign subscription
- A Power Platform premium plan (per-user or per-app) — DocuSign/Adobe Sign are premium connectors

## Permissions required

- Environment Maker on the target environment
- Edit access on the SharePoint contracts library
- API/account access to your DocuSign or Adobe Sign tenant
- Permission to post to the Legal Operations Teams channel

## Connectors used in this build

- SharePoint
- DocuSign or Adobe Sign (premium)
- Microsoft Teams

> **Note:** Check licensing first — this is the only scenario in the kit needing a premium connector, and it's the most likely to block a team mid-build if not sorted in advance.

---

Part of the [Copilot Studio Agent-a-thon Kit](../README.md). See the root README for the full prerequisites table across all 12 scenarios.
