# Copilot Studio Agent-a-thon Kit

Created by **Shenuka Fernando** — Modern Workplace & Cloud Consultant (Microsoft 365, Copilot, Entra ID, Microsoft Purview).

A complete, ready-to-run kit for facilitating a Microsoft Copilot Studio agent-a-thon: a facilitator run-of-show, a self-contained build guide per scenario, and clean sample data — one folder per scenario, drop it on a team and go.

## Folder structure

```
copilot-studio-agentathon-kit/
├── facilitator/            ← shared materials, read these first
├── Sales/
├── Customer-Service/
├── Finance/                ← Function: budget & variance
├── HR/                     ← includes SharePoint list + Adaptive Card templates
├── Marketing/
├── Consumer-Experience/
├── Finance-Audit/          ← Industry: audit & control exceptions
├── Frontline/
├── Healthcare/
├── Legal/
├── Public-Sector/
└── Tech/
```

Every scenario folder contains exactly two files (HR has two extra): the **full build guide PDF** (steps 1–10, current Copilot Studio methods) and the **sample data workbook** for the Knowledge tab. Hand a team the whole folder and they have everything they need.

## What's in each scenario folder

| Folder | Guide | Data file | Step 6 build |
|---|---|---|---|
| `Sales/` | Sales_Pipeline_Copilot_Full_Build_Guide.pdf | Sales_Pipeline_Data.xlsx | Direct Dataverse connector action — no flow needed |
| `Customer-Service/` | Customer_Service_Insights_Copilot_Full_Build_Guide.pdf | Customer_Service_Cases_Data.xlsx | Agent flow → Dynamics 365 + Teams adaptive card |
| `Finance/` | Finance_Budget_Copilot_Full_Build_Guide.pdf | Finance_Budget_Data.xlsx | Agent flow → new SharePoint list + Teams |
| `HR/` | HR_People_Operations_Copilot_Full_Build_Guide.pdf | HR_People_Operations_Data.xlsx | Agent flow → SharePoint list + Teams adaptive card (+ downloadable templates, see below) |
| `Marketing/` | Marketing_Campaigns_Copilot_Full_Build_Guide.pdf | Marketing_Campaigns_Data.xlsx | Agent flow → Planner task + Teams + SharePoint |
| `Consumer-Experience/` | Store_Ops_Daily_Copilot_Full_Build_Guide.pdf | Consumer_StoreOps_Data.xlsx | Agent flow → Teams post + SharePoint archive |
| `Finance-Audit/` | Audit_Reporting_QA_Copilot_Full_Build_Guide.pdf | Finance_Audit_Data.xlsx | Agent flow → new SharePoint list + Teams |
| `Frontline/` | Frontline_Shift_Handover_Copilot_Full_Build_Guide.pdf | Frontline_Shifts_Data.xlsx | Agent flow → new Dataverse table + Teams |
| `Healthcare/` | Patient_Intake_Summariser_Copilot_Full_Build_Guide.pdf | Healthcare_Intake_Data.xlsx | Agent flow → Planner task + Teams |
| `Legal/` | Legal_Contract_Review_Copilot_Full_Build_Guide.pdf | Legal_Contracts_Data.xlsx | Agent flow → DocuSign/Adobe Sign + SharePoint write-back |
| `Public-Sector/` | Public_Sector_Case_Triage_Copilot_Full_Build_Guide.pdf | PublicSector_Cases_Data.xlsx | Agent flow → Word template population + SharePoint |
| `Tech/` | Incident_Postmortem_Copilot_Full_Build_Guide.pdf | Tech_Incidents_Data.xlsx | Agent flow with a loop → Azure DevOps parent + child work items |

Each guide carries the original scenario's verbatim instructions, custom topic, and evaluation content, with **Step 6 rewritten for the current (2026) Copilot Studio experience** — the exact connectors/actions to add, and whether the tool needs an agent flow at all or attaches as a direct connector action. Every guide opens with a "Files & Where They Go" map.

`HR/` additionally ships two downloadable prerequisite files for a fully worked, click-by-click example:
- **LeaveRequests_SharePointList_Template.xlsx** — import via SharePoint's "New → List → From Excel" to create the list the tool writes to.
- **LeaveRequest_AdaptiveCard.json** — Adaptive Card template for the Teams manager-notification action, with `{{Placeholder}}` tokens ready to bind to flow dynamic content.

For the other 11 scenarios, prerequisite SharePoint lists / Dataverse tables / Word templates are described inline in each guide's Step 6 (columns, field names, setup steps) rather than shipped as separate files.

> **Note on the data files:** the original sample workbooks shipped with rights-management (IRM) encryption from their source tenant, unopenable outside it. These are clean, unencrypted replacements with the same column schema as each scenario's build deck, seeded with the specific record IDs each guide's sample and evaluation queries reference (so those demo prompts return real results) — synthetic data, not a recovery of the original rows.

## Facilitator materials

- **`facilitator/agentathon-run-of-show.html`** — 90-minute session timeline, the 10-step build framework, a scenario picker table for all 12 tracks, and facilitator pitfalls to watch for.
- **`facilitator/Copilot_Studio_Tools_Actions_Update.pdf`** — general current-state reference for building tools in Copilot Studio (agent flows, the natural-language flow builder, attaching a flow as a tool, posting Teams adaptive cards). Useful background even though each scenario guide's Step 6 already covers this for its own tool.

## Prerequisites — licenses & permissions

### Every scenario needs
- **Microsoft Copilot Studio** license or trial (message-capacity licensing; check your tenant's entitlement before a multi-team session — every test-pane run and every agent flow action consumes capacity).
- **Environment Maker** role (or higher) on the target Power Platform environment — needed to create the agent, topics, and flows.
- A **Microsoft 365 account** with standard licensing (Teams, SharePoint, and Planner are included in most Business/E-plans — confirm your attendees actually have these apps provisioned, not just Copilot Studio).
- **Publishing is separate from building**: Teams and Microsoft 365 Copilot channels require **tenant admin approval** before real users see the agent. Don't plan on this landing inside a single workshop session — the Test pane is the realistic finish line on the day.

### Extra requirements by scenario

| Scenario | Extra connector / license | Extra permission needed |
|---|---|---|
| Sales | Dataverse (standard Dynamics 365 Sales app) | Read/write access to the Opportunity table |
| Customer Service | Dynamics 365 Customer Service | Read/write access to the `incident` table |
| Finance | SharePoint Online (standard) | Contribute access on the site hosting the "Variance Notes" list |
| HR | SharePoint Online (standard) | Contribute access on the site hosting the "Leave Requests" list |
| Marketing | Microsoft Planner (standard) | Owner/member on the Marketing Campaign Requests plan |
| Consumer Experience | SharePoint Online + Teams (standard) | Contribute access on the archive site; membership in each store's Teams channel |
| Finance (Audit) | SharePoint Online (standard) | Contribute access on the site hosting the "Audit Findings" list |
| Frontline | **Dataverse custom table** | **System Customizer** (or higher) role in Power Apps to create the "SafetyIncidents" table |
| Healthcare | Microsoft Planner (standard) | Owner/member on the Clinical Review Tasks plan; confirm data handling meets your org's health-data policy even though this dataset is synthetic |
| Legal | **DocuSign or Adobe Sign** — premium connector | Active DocuSign/Adobe Sign account with API access, **and** a Power Platform premium/per-user plan that covers premium connector usage |
| Public Sector | **Word Online (Business)** connector | OneDrive for Business / SharePoint storage for the template; author the `.docx` template with named content controls before Step 6 |
| Tech | Azure DevOps | Project-level permission to create work items; an authorized Azure DevOps connection in the flow |

If you're running this as a multi-team session, check the **Legal** and **Frontline** rows first — DocuSign/Adobe Sign premium connector licensing and Dataverse System Customizer access are the two most likely to block a team mid-build if not sorted in advance.

## How to use this kit

1. Read `facilitator/agentathon-run-of-show.html` first to plan session timing and pick which scenarios your teams will build.
2. Check the **Prerequisites** section above against your tenant — sort licensing/permission gaps before the session starts, not during it.
3. Hand each team their scenario's whole folder — the guide is self-contained, teams don't need anything outside it plus a browser and Copilot Studio access.
4. `facilitator/Copilot_Studio_Tools_Actions_Update.pdf` is optional extra background reading on the current tool-building experience.
5. For a fully worked example with downloadable prerequisite files, use `HR/` — it's the one scenario with a ready-made SharePoint list template and Adaptive Card JSON alongside its guide.

---

Built for a Microsoft Copilot Studio Build-Along / Agent-a-thon session, 2026.
