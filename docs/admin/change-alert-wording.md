# Change the wording of an alert

The text of every Slack alert lives in the automation that sends it, in the Slack step's message box — not in code. Change it there and the next message uses the new wording.

## Where

In the base, open **Automations** and the one you want: *[Alerts] Morning list*, *[Steps] Notify the owner when a step is reassigned*, *[Content] Graphics cue when Graphics needed is ticked*, or, for the new-steps notice, *[Content] Generate steps from template* and *[Content] Regenerate steps…* (both send it, so change both). Inside the repeating group, click the **Send a Slack message** step. The message is in its **Message** box.

<span class="screenshot-placeholder">Screenshot to add: a Slack step's message box with tokens in it</span>

## How the message is built

The box holds plain text with **tokens** dropped in — blue chips such as `slug`, `when`, `stepUrl`. The tokens are filled by the tracker for each message; the text around them is yours. You can move tokens, delete them, or change every word between them. Slack formatting works: `*bold*`, `_italic_`, and links written as `<url|words to show>`.

| Token | What it becomes |
|---|---|
| `testNote` | a test-mode line while the tracker is being set up; empty afterwards. Leave it or delete it |
| `slug` | the piece's name |
| `countLabel`, `stepList` | "3 steps", and one bullet per step with its date (new-steps notice) |
| `stepName`, `when`, `stepUrl` | the step, its dates, a link to it (reassignment notice) |
| `editor`, `pieceUrl` | the piece's editor and a link to the piece (graphics cue) |
| `firstName`, `dateLabel`, `summary` | "Good morning Simon", "Fri 24 Oct", "2 due today, 1 overdue" (morning list) |
| `dueToday`, `dueBackToday`, `overdue`, `writersDrafts` | the four sections of the morning list, each a heading and its bullets, or nothing when empty |

Click **Update** at the top of the automation to publish the change.

!!! note "Two things you can't change in the box"
    The four section headings of the morning list (*Due today*, *Due back today*, *Overdue*, *Writers' drafts due*) are set in the script step that builds the sections, because an empty section has to disappear. And a new token — say, the piece's subject area — needs the script step to supply it. Ask for either.
