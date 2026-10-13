---
name: copilot-studio-apps-iteration-coach
description: Use this skill when the user has a first draft of an app in the Copilot Studio apps experience and wants to improve it — turning feedback ("make it better", "the form is confusing", a screenshot) into small, ordered change prompts with acceptance criteria and a preview test script.
---

# Copilot Studio Apps: Iteration Coach

Turn feedback on an **Apps (Preview)** draft into a sequence of precise change prompts for the Copilot Studio app chat, each small and testable.

## Input methods to recommend

| Method | Best for |
|---|---|
| **Chat** | Fields, layout, text, behavior, rules |
| **+ Upload a file** | A spreadsheet or document that defines fields or rules |
| **+ Screenshot** | Showing the current state or a reference design |
| **+ Annotate the canvas** | Pointing at the exact control or area to change |

## Workflow

### 1. Collect feedback

Accept notes, a list of complaints, or a screenshot. Ask which role the feedback comes from (for example requester, approver, admin) if it isn't clear.

### 2. Classify each item

- **Data** — fields, validation
- **Logic** — status rules, permissions, calculations
- **UI** — layout, labels, navigation
- **AI** — extraction, summaries, flags
- **Integration** — notifications, connector actions

If an item needs a new data source or connector, mark it **"data decision needed"** and do not guess the source.

### 3. Write one change prompt per item

- One change per prompt; never bundle several changes.
- Name the screen, the control and the expected result.
- Include acceptance criteria.
- Pattern: `On the <screen>, <change>. When <condition>, it should <result>.`
- Example: `On the New expense form, make Receipt required when Amount is over 50. Show the message "Receipt required above 50" under the field.`

### 4. Order the prompts

Data → Logic → UI → AI → Integration. Data changes ripple into everything else.

### 5. Deliver

Return a table, then one closing line:

```
| # | Type | Prompt to paste | How to send | Test it |
```

- **How to send**: the input method from the table above.
- **Test it**: 2–4 preview steps, covering each affected role and one negative case (wrong input or missing permission).

Closing line: "Send them one at a time and test in preview after each. Publish again after testing so users get the changes."
