# Copilot Studio Apps: Data Advisor

**Built for Copilot Studio apps.** Apps generated in Copilot Studio can use sample data, the browser, or organizational sources like SharePoint, Dataverse and Excel. Picking the wrong one is the most common reason an app "loses" data or works for the maker but not for anyone else. This skill picks the right one and tells you exactly what to type.

## Before you start

- Access to [Copilot Studio](https://copilotstudio.microsoft.com/) with the **New experience** toggle on and the **App (Preview)** tile visible.
- An app draft, or at least a clear idea of what it tracks.
- Available data sources depend on your environment, admin data policies, licenses and permissions. This is a preview feature.

## How to use it

Add the skill to your Copilot Studio agent and ask, for example:

> *"Where should my expense app store its data? Approvals need to be visible to managers."*

> *"My app data disappears when I reload. Why?"*

The skill:

1. **Asks a few questions**: is this exploration or real use, must data be shared, does it already exist, who edits what.
2. **Recommends a data approach** (sample, browser-local, SharePoint list, existing Dataverse table, Excel table, file upload or none) with the reason.
3. **Writes the prompt** to paste in the app chat to apply it.
4. **Lists who needs data access**, because sharing an app never shares its data.
5. **Tells you how to verify** the source in **Data** and **Connections**.

For problems, it matches the symptom (data disappears, others can't see records, source not selectable, schema changed) to the cause and the fix.

## Good to know

- **Start with sample data**, then connect real data once the design is right.
- **Don't copy existing data.** If it already lives in SharePoint or Dataverse, connect to it.
- **SharePoint vs Dataverse:** SharePoint for straightforward team lists; Dataverse when you already have a governed data model with relationships and security roles.
- **An attached spreadsheet is context, not a connection.** Use the Excel connector for live workbook data.

Based on the Microsoft Learn documentation for [data in your app (preview)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/apps-experience/data-and-connections).

Created by [Renato Romão](https://www.linkedin.com/in/renatoromao/), Microsoft MVP (Copilot Studio & Microsoft Foundry).
