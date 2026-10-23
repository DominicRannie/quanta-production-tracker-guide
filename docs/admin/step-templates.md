# Step templates

Everything the tracker knows about a workflow is in one table, **Step templates**: one row per step per content type. Change a row and every piece scheduled from then on follows it; pieces already scheduled pick the change up the next time their date or people change.

## What a row says

| Column | Meaning |
|---|---|
| **Step** | the step's name as it appears on pieces |
| **Content type** | which type gets this step |
| **Order** | where it sits in the list |
| **Track** | Editorial, Lede art, Secondary art, Graphics, Production or Audience |
| **Owner role** | who owns it: a role that is a field on the piece (Editor, Host, Top editor, Fact-checker, Copyeditor, Image researcher, Staging and publishing, Graphics designer), or a team (Art editors, Audience team, Production team, PRX) |
| **Default owner** | the person or people who own it when the piece's field is blank, or when the role is a team. Several people can be listed |
| **Due offset / Offset unit** | how far from the publish date: a negative number of *weeks*, *days* or *working days*; *after publication* means undated |
| **Due-back offset** | how long after the due date the work comes back, in the same unit; blank for no due-back |
| **Dated from** | *Draft due* on the one row that should take the piece's Draft due date |
| **Applies when** | *Always*; *Graphics needed* or *Photo shoot* (only when the piece has that tick); *Manual* (never generated — added by hand) |
| **Kind** | *Step* generates steps. *Automation* and *Computed* rows are documentation of things the tracker does itself and generate nothing |
| **Active** | untick to retire a row without deleting it |

## Common changes

**Move a deadline.** Change *Due offset*. Nine working days before publication is `-9` with unit *working days*.

**Change who does something by default.** Change *Default owner*. For a role the piece names, the piece's field still wins when filled.

**Add a step to a type.** Add a row with the type, an order number, a track, a role and an offset, tick *Active*, set *Applies when* to *Always*. Scheduled pieces gain it the next time they are touched.

**Retire a step.** Untick *Active*. Existing steps stay on their pieces.

!!! warning
    Role names in *Owner role* and the *Draft due* option must match exactly — the tracker reads them by name. Don't rename those options.
