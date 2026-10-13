---
name: copilot-studio-apps-publish-readiness
description: Use this skill before the user publishes or shares an app built in the Copilot Studio apps experience — to run a go/no-go readiness check on scenarios, data, connections, permissions, consent and audience, and to draft the message announcing the app to its users.
---

# Copilot Studio Apps: Publish Readiness

Run a go/no-go check before an **Apps (Preview)** app reaches real users, then draft the sharing message.

## Rules to apply in the check

- **Publish** makes the latest version available to people the app is shared with. Later changes need a new publish.
- **Share** grants people, Microsoft 365 or security groups, or an environment-permitted link permission to open the app. It does not grant edit rights to the design.
- Apps access data **as the signed-in user**. Sharing the app never shares the underlying data, and users may need to consent to connections on first run.
- Available sharing options depend on environment and admin policy.

## Workflow

### 1. Intake

Ask, in one batch, only what is unknown: app purpose, intended audience (people or groups), data sources, connectors used, whether a test account with end-user permissions exists, and whether the data is sensitive.

### 2. Run the checklist

Mark each item ✅ / ⚠️ / ❌ with a one-line reason. Mark ⚠️ when the user hasn't confirmed it.

**Scenarios**
- Main scenario tested in preview for every role
- At least one negative case tested (bad input, missing permission)

**Data**
- Real records don't rely on sample data
- Shared records don't use browser-local storage
- **Data** and **Connections** views reviewed; sources are the intended ones

**Permissions**
- Every target user or group can access each underlying list, table or workbook
- Tested with an account that has end-user permissions
- Users can't delete or change what they shouldn't

**Connections**
- Each connector is allowed by data policy
- Users know they may be asked to consent on first run

**Publish**
- Validation messages (build, connections, policy, settings) resolved
- Published URL opened and checked after publishing

**Audience**
- Shared with a group rather than a long list of individuals, where possible
- Users know who to contact for issues

### 3. Deliver

Return, in this order:
1. **Checklist** with marks and reasons.
2. **Verdict**: **Go**, **Go with fixes** (list them), or **No-go** (list blocking items).
3. **Sharing message** for Teams or email: what the app does, a `[app link]` placeholder, a first-run consent note, a data access note, and a support contact placeholder.

## Guardrails
- Never suggest granting broader data access just to make the app work; adjust the audience or data permissions deliberately.
- If the data is sensitive, include "Confirm with your admin before sharing beyond your team" in the fixes.
