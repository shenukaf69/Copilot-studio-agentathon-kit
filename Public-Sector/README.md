# Public Sector Case Triage Copilot

Triages new citizen cases by category/priority/SLA and drafts plain-language acknowledgement letters.

**Guide:** `Public_Sector_Case_Triage_Copilot_Full_Build_Guide.pdf`
**Sample data:** `PublicSector_Cases_Data.xlsx`

## Workloads used

- Microsoft Copilot Studio
- Word for the web
- SharePoint Online
- Microsoft Teams

## Licenses required

- Copilot Studio
- Microsoft 365 (Word, SharePoint)
- Microsoft Teams

## Permissions required

- Environment Maker on the target environment
- Contribute access on the SharePoint library holding the letter template and drafts
- Permission to post to the case officer's Teams channel

## Connectors used in this build

- Word Online (Business)
- SharePoint
- Microsoft Teams

> **Note:** You need to author the .docx letter template yourself first, with named content controls (CitizenRef, Category, SLA, OfficerName, PersonalisationNote) — see Step 6a in the guide.

---

Part of the [Copilot Studio Agent-a-thon Kit](../README.md). See the root README for the full prerequisites table across all 12 scenarios.
