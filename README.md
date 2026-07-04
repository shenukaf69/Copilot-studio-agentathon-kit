# Copilot Studio Agent-a-thon Kit

Created by **Shenuka Fernando** — Modern Workplace & Cloud Consultant (Microsoft 365, Copilot, Entra ID, Microsoft Purview).

A complete, ready-to-run kit for facilitating a Microsoft Copilot Studio agent-a-thon: a facilitator run-of-show, per-scenario build guides, and clean sample data for every scenario.

## What's in this kit

### Facilitator materials
- **`facilitator/agentathon-run-of-show.html`** — 90-minute session timeline, the 10-step build framework, a scenario picker table for all 12 tracks, and facilitator pitfalls to watch for.
- **`facilitator/Copilot_Studio_Tools_Actions_Update.pdf`** — current (2026) reference for building tools in Copilot Studio: agent flows, the natural-language flow builder, attaching a flow as a tool, and posting Teams adaptive cards. Written to replace outdated "HTTP trigger" wording from the original scenario decks.

### Full build guides — all 12 scenarios
Each guide walks every step (1–10) to build that scenario's agent from a blank Copilot Studio environment: the original verbatim instructions, topic, and evaluation content from that scenario's Build-Along deck, plus a **Step 6 rewritten for the current (2026) Copilot Studio experience** — agent flows, the exact connectors/actions to add, and whether the tool needs a flow at all or attaches as a direct connector action. Each guide opens with a "Files & Where They Go" map.

| File | Scenario | Step 6 build |
|---|---|---|
| `guides/Sales_Pipeline_Copilot_Full_Build_Guide.pdf` | Sales | Direct Dataverse connector action — no flow needed |
| `guides/Customer_Service_Insights_Copilot_Full_Build_Guide.pdf` | Customer Service | Agent flow → Dynamics 365 + Teams adaptive card |
| `guides/Finance_Budget_Copilot_Full_Build_Guide.pdf` | Finance (Function) | Agent flow → new SharePoint list + Teams |
| `guides/HR_People_Operations_Copilot_Full_Build_Guide.pdf` | HR | Agent flow → SharePoint list + Teams adaptive card |
| `guides/Marketing_Campaigns_Copilot_Full_Build_Guide.pdf` | Marketing | Agent flow → Planner task + Teams + SharePoint |
| `guides/Store_Ops_Daily_Copilot_Full_Build_Guide.pdf` | Consumer Experience Industries | Agent flow → Teams post + SharePoint archive |
| `guides/Audit_Reporting_QA_Copilot_Full_Build_Guide.pdf` | Finance (Industry / Audit) | Agent flow → new SharePoint list + Teams |
| `guides/Frontline_Shift_Handover_Copilot_Full_Build_Guide.pdf` | Frontline | Agent flow → new Dataverse table + Teams |
| `guides/Patient_Intake_Summariser_Copilot_Full_Build_Guide.pdf` | Healthcare | Agent flow → Planner task + Teams |
| `guides/Legal_Contract_Review_Copilot_Full_Build_Guide.pdf` | Legal | Agent flow → DocuSign/Adobe Sign + SharePoint write-back |
| `guides/Public_Sector_Case_Triage_Copilot_Full_Build_Guide.pdf` | Public and Regulated | Agent flow → Word template population + SharePoint |
| `guides/Incident_Postmortem_Copilot_Full_Build_Guide.pdf` | Technology & Digital Economy | Agent flow with a loop → Azure DevOps parent + child work items |

### HR scenario — reference templates
The HR guide is the one scenario with downloadable prerequisite artifacts built alongside it, for teams who want a fully worked, click-by-click example:
- **`templates/LeaveRequests_SharePointList_Template.xlsx`** — import via SharePoint's "New → List → From Excel" to create the list the agent's tool writes to.
- **`templates/LeaveRequest_AdaptiveCard.json`** — Adaptive Card template for the Teams manager-notification action, with `{{Placeholder}}` tokens ready to bind to flow dynamic content.

For the other 11 scenarios, the prerequisite SharePoint lists / Dataverse tables / Word templates are described inline in each guide's Step 6 (columns, field names, and setup steps) rather than shipped as separate downloadable files.

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
2. Distribute the matching **full build guide** from `guides/` and the matching **data file** from `data/` for each team's chosen scenario — the guide is self-contained, teams don't need the original repo's Build-Along PDF.
3. `facilitator/Copilot_Studio_Tools_Actions_Update.pdf` is a general reference for the current tool-building experience, useful background even though each guide's Step 6 already covers this for its specific scenario.
4. For a fully worked example with downloadable prerequisite files (SharePoint list template, Adaptive Card JSON), use the HR scenario — `guides/HR_People_Operations_Copilot_Full_Build_Guide.pdf` plus the two files in `templates/`.

---

Built for a Microsoft Copilot Studio Build-Along / Agent-a-thon session, 2026.
