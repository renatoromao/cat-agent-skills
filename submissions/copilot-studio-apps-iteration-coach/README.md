# Copilot Studio Apps: Iteration Coach

**Built for Copilot Studio apps.** Copilot Studio gives you a working app draft from a prompt. Getting from draft to done depends on how you ask for changes. "Make it better" gets you a guess. This skill turns feedback into small, precise change prompts you can send one by one.

## Before you start

- An app draft in **Apps (Preview)** in [Copilot Studio](https://copilotstudio.microsoft.com/).
- Feedback in any form: notes, a list of complaints, or a screenshot.
- Each build and preview can consume **Copilot Credits**. Small, precise prompts waste fewer runs than vague, bundled ones.

## How to use it

Add the skill to your Copilot Studio agent and paste your feedback, for example:

> *"Managers say the approval screen is confusing, the receipt field should be required for big amounts, and finance wants a monthly total."*

The skill:

1. **Classifies each item** as data, logic, UI, AI or integration.
2. **Writes one change prompt per item**, naming the screen, the control and the expected result, with acceptance criteria.
3. **Orders them** data → logic → UI → AI → integration, since data changes ripple into everything else.
4. **Recommends how to send each one**: chat, file upload, screenshot, or canvas annotation.
5. **Adds a test script** per change, with one negative case.

Items that need a new data source are flagged instead of guessed. Use the *Copilot Studio Apps: Data Advisor* skill for those.

## Good to know

- **One change per prompt.** It's easier to test, and easier to undo.
- **Annotate when you can.** Pointing at a control beats describing it.
- **Prefer chat over code edits.** The agent keeps data model, logic and UI in sync.
- **Publish again after testing.** Changes aren't live for users until you republish.

Based on the Microsoft Learn documentation for [creating an app in Copilot Studio (preview)](https://learn.microsoft.com/en-us/microsoft-copilot-studio/apps-experience/create-app).

Created by [Renato Romão](https://www.linkedin.com/in/renatoromao/), Microsoft MVP (Copilot Studio & Microsoft Foundry).
