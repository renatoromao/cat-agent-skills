# Copilot Studio Apps: Publish Readiness

**Built for Copilot Studio apps.** In Copilot Studio, publishing and sharing an app are separate steps, and neither one gives users access to the app's data. Most "the app doesn't work for me" messages come from that gap. This skill catches it before you share.

## Before you start

- An app built in **Apps (Preview)** in [Copilot Studio](https://copilotstudio.microsoft.com/), tested in preview.
- A list of who should use it (people or groups) and which data sources it connects to.
- Ideally, a test account with the same permissions as your end users.
- Apps are created in your **personal environment**, and this is a preview feature not meant for production use. Sharing options depend on your admin policies.

## How to use it

Add the skill to your Copilot Studio agent and ask, for example:

> *"Is my expense app ready to share with the Finance team? It uses a SharePoint list and sends Outlook emails."*

The skill:

1. **Asks about the app**: purpose, audience, data sources, connectors, test account, sensitive data.
2. **Runs a checklist** across scenarios, data, permissions, connections, publish and audience, marking each item ✅ / ⚠️ / ❌.
3. **Gives a verdict**: Go, Go with fixes, or No-go.
4. **Drafts the sharing message** for Teams or email, including the first-run consent and data access notes.

## Good to know

- **Publish ≠ Share.** Publish updates the version users run; Share decides who can open it.
- **Share ≠ data access.** Users also need access to the SharePoint list, Dataverse table or workbook.
- **Users connect as themselves.** Two people can see different data in the same app.
- **Republish after changes.** Edits aren't live until you publish again.

Based on the Microsoft Learn documentation for [publishing and sharing an app (preview)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/apps-experience/publish-share-app).

Created by [Renato Romão](https://www.linkedin.com/in/renatoromao/), Microsoft MVP (Copilot Studio & Microsoft Foundry).
