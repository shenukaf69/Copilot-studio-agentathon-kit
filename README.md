# Copilot Studio Agent-a-thon Kit

Created by **Shenuka Fernando** — Modern Workplace & Cloud Consultant (Microsoft 365, Copilot, Entra ID, Microsoft Purview).

A complete, ready-to-run kit for facilitating a Microsoft Copilot Studio agent-a-thon: a facilitator run-of-show, per-scenario build guides, and clean sample data for every scenario.

## What's in this kit

### Facilitator materials
- **`facilitator/agentathon-run-of-show.html`** — 90-minute session timeline, the 10-step build framework, a scenario picker table for all 12 tracks, and facilitator pitfalls to watch for.
- **`facilitator/Copilot_Studio_Tools_Actions_Update.pdf`** — current (2026) reference for building tools in Copilot Studio: agent flows, the natural-language flow builder, attaching a flow as a tool, and posting Teams adaptive cards. Written to replace outdated "HTTP trigger" wording from the original scenario decks.

### HR scenario — full worked example
- **`guides/HR_People_Operations_Copilot_Full_Build_Guide.pdf`** — every step (1–10) to build the HR People Operations Copilot from a blank Copilot Studio environment, including a complete file map of what goes where.
- **`templates/LeaveRequests_SharePointList_Template.xlsx`** — import via SharePoint's "New → List → From Excel" to create the list the agent's tool writes to.
- **`templates/LeaveRequest_AdaptiveCard.json`** — Adaptive Card template for the Teams manager-notification action, with `{{Placeholder}}` tokens ready to bind to flow dynamic content.

### Clean sample data — all 12 scenarios
The original sample workbooks shipped with rights-management encryption (IRM) from their source tenant, which made them unopenable outside that tenant. These are clean, unencrypted replacements with the same column schema as each scenario's build deck, seeded with the specific record IDs each deck's sample and evaluation queries reference (so those demo prompts return real results):

| File | Scenario |
|---|---|
| `data/Sales_Pipeline_Data.xlsx` | Sales |
| `data/Customer_Service_Cases_Data.xlsx` | Customer Service |
| `data/Finance_Budget_Data.xlsx` | Finance (Function) |
| `data/HR_People_Operations_Data.xlsx` | HR |
| `data/Marketing_Campaigns_Data.xlsx` | Marketing |
| `data/Consumer_StoreOps_Data.xlsx` | Consumer Experience Industries |
| `data/Finance_Audit_Data.xlsx` | Finance (Industry) |
| `data/Frontline_Shifts_Data.xlsx` | Frontline |
| `data/Healthcare_Intake_Data.xlsx` | Healthcare |
| `data/Legal_Contracts_Data.xlsx` | Legal |
| `data/PublicSector_Cases_Data.xlsx` | Public and Regulated |
| `data/Tech_Incidents_Data.xlsx` | Technology & Digital Economy |

> Note: this is synthetic data matching each scenario's documented schema — not a recovery of the original encrypted rows, which weren't recoverable without the source tenant's rights-management access.

## How to use this kit

1. Read `facilitator/agentathon-run-of-show.html` first to plan session timing and pick which scenarios your teams will build.
2. Distribute the matching data file from `data/` for each team's chosen scenario, along with that scenario's original Build-Along PDF.
3. Use `facilitator/Copilot_Studio_Tools_Actions_Update.pdf` alongside Step 6 of any scenario deck — it documents the current way to build tools, regardless of which scenario a team picked.
4. For a fully worked example end-to-end (including the SharePoint list and Teams adaptive card setup), follow `guides/HR_People_Operations_Copilot_Full_Build_Guide.pdf`.

---

Built for a Microsoft Copilot Studio Build-Along / Agent-a-thon session, 2026.
