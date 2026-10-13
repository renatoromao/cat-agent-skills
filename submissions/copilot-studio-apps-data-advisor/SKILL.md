---
name: copilot-studio-apps-data-advisor
description: Use this skill when the user is building an app in the Copilot Studio apps experience and must decide where the app's data lives — sample data, browser-local storage, a SharePoint list, an existing Dataverse table, an Excel table, or another connected source — or when app data disappears, isn't shared with other users, or a connection is missing.
---

# Copilot Studio Apps: Data Advisor

Recommend the right data approach for an app built with **Apps (Preview)** in Copilot Studio and return the exact chat prompt to apply it.

## Options

| Approach | Use when | Watch out |
|---|---|---|
| **Sample data** | Exploring the idea, refining screens | Changes can reset on reload or regeneration. Not for business records. |
| **Browser-local** | Personal, self-contained tools | Not shared across users, devices or browsers; not governed as org data. |
| **SharePoint list** | List-shaped team data: trackers, requests, inventories | Users need site/list permissions. Creating a new site may not be available in the current preview. |
| **Dataverse (existing table)** | Related records, governed processes, existing data model | Connects to existing tables; creating new tables may not be available. Security roles apply. |
| **Excel table (connector)** | Data already lives in a workbook | Must be a defined Excel table. An attached file is context only, not a live connection. |
| **File upload in the app** | Users process an Excel/CSV at runtime | Not a shared or synced data source. |
| **No storage** | Calculators, converters | — |

Connector actions (send an Outlook email, post in Teams, create a calendar event) extend behavior but **do not store records**.

## Workflow

### 1. Intake

Ask, in one batch, only what is unknown:
- Is this exploration, or will real people use it?
- Must records be shared across users or devices?
- Does the data already exist? Where (SharePoint, Dataverse, Excel, SQL)?
- Who reads vs. who creates, updates or deletes?
- If starting from a spreadsheet: is it context, live data, or something end users upload?

### 2. Decide

- Exploring → sample data.
- One person, one browser → browser-local may be enough.
- Shared, central or cross-device → organizational source.
- Data already exists → connect to it; never create a copy.
- New storage needed, list-shaped → SharePoint list.
- Existing relational model or Dataverse security → Dataverse.

### 3. Deliver

Return, in this order:
1. **Recommendation** with a one-sentence reason.
2. **Prompt to paste** in the app chat, in a code block, e.g. `Connect this app to the existing SharePoint list "Expense Requests" on the Finance site and stop using sample data.`
3. **Permission check**: who needs access to the underlying list, table or workbook. Sharing the app does not share the data.
4. **Verify step**: select the app name in the command bar → **Data** and **Connections** to confirm the source.

## Troubleshooting

When the user reports a problem, match it and return the cause and the fix:

| Symptom | Likely cause | Fix |
|---|---|---|
| Changes disappear on reload | Sample or temporary data | Ask the agent to connect an org source |
| Data persists but others can't see it | Browser-local storage | Move to SharePoint or Dataverse |
| Source not selectable | Policy, missing connection, permission or license | Ask the admin which connectors are allowed |
| User opens app but sees no data | No access to the underlying source or no consent | Grant data access; user consents on first run |
| Edited attached file not reflected | Attachment is context only | Connect the Excel table via connector |
| Source schema changed | Stale generated connection | Ask the agent to refresh or re-create the connection |

Never advise editing generated connection code by hand; ask the agent to update the connection.
