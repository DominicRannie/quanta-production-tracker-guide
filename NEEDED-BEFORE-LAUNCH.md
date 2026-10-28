# What this starter still needs

The scaffold, navigation, deploy config and the core articles are in place. Three things take it to launch.

## 1. Confirm the interface links — checked 2026-10-28

All four page IDs resolve to published pages of `Production tracker (demo)` (read through the API on 2026-10-28). Re-check if the interface is renamed or pages rebuilt.

Pages link straight to the tracker's screens with URLs built from the base's IDs (`https://airtable.com/appFlJWmSk0RDIf1U/pbdMlP776N9XQeREM/{page}`). Open each once from **Quick links** and confirm it lands. If the interface is renamed from *Production tracker (demo)* or pages are rebuilt, the IDs may change — update `docs/quick-links.md` and the pages that link to each screen (search `pag` under `docs/`).

| Screen | Page ID |
|---|---|
| My work | pagH9V6ux14ZXhxhl |
| Timeline | pag2Lck56OEnw9CxY |
| Pipeline | pagTU2JvGpMKJK4jc |
| Art requests | pagcK8rOZFtdfgdEn |

Open question: whether readers should get the editor links (need base access) or published/shared interface links.

## 2. Screenshots

Each article has a dashed placeholder where a screenshot goes. Save the image into `docs/assets/` and replace the placeholder with `![caption](../assets/filename.png)`; every screenshot needs a one-line caption.

| Article | Suggested filename |
|---|---|
| Where to find things — the four screens | `tracker-menu.png` |
| Where to find things — a piece's page | `piece-page.png` |
| Your day — morning list in Slack | `morning-list.png` |
| Schedule a piece — steps just created | `piece-scheduled.png` |
| Who does what — people fields | `people-fields.png` |
| Tick a step — Done and Done on | `step-done.png` |
| Request art — a request with items | `art-request.png` |
| Graphics — tick and Commission infographic step | `graphics-needed.png` |
| Change alert wording — Slack message box | `slack-message-box.png` |

## 3. Pages waiting on design decisions

- **Add a pitch** — the new-piece form and the backlog page grouped by subject area are being designed with Samir. Rewrite once they exist.
- **Where to find things** — add the Backlog page when it exists; confirm the names of the record pages.
- **Content types** — Newsletters and Articles – Social Exclusive have no steps yet; Video, podcasts and galleries have offsets pending.
- **Alerts** — once the Slack connection moves to the Quanta workspace and test mode is off, remove the `testNote` row from the token table if the token is deleted from the blocks.
- Review every page against the real interface from an end user's point of view — round 1 done 2026-10-28 (vault: `Specifications/2026-10-28 - User guide review against the interface.md`): guide corrected for My work (team list grouped by person), Timeline, Pipeline tabs, pitch creation, subject names, ad-hoc steps. Repeat after each designer pass.
