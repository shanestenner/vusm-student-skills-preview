# Screenshots

Reference shots used in the install walkthroughs:
[`../../README.md`](../../README.md),
[`../../INSTALL_CLAUDE_AI.md`](../../INSTALL_CLAUDE_AI.md),
[`../../INSTALL_DESKTOP.md`](../../INSTALL_DESKTOP.md).

> **Provenance note.** These images were captured during the *faculty*
> Curriculum Intelligence pilot install. The claude.ai install **flow**
> is skill-agnostic, so the navigation/Capabilities shots
> (`01`, `02`, `web-prereq-*`, `web-00*`, `web-01`, `web-02`, `web-03`)
> are accurate as-is. The skill-specific shots — `03-skill-activated.png`,
> `web-04-skill-enabled.png`, `web-05-try-query.png`,
> `web-06-try-response.png` — still show "curriculum-intelligence" and a
> faculty query. **Retake these against Student Coach / Student Tutor**
> when convenient; the install steps work regardless.

The desktop app's UI is similar but not pixel-identical; use Anthropic's
[current support article](https://support.claude.com/en/articles/12512180-use-skills-in-claude#h_a4222fa77b)
if the desktop labels drift.

## Generic walkthrough (README.md)

- `01-customize-skills.png` — Customize → Skills with the "+" button
- `02-upload-skill.png` — Upload skill dialog ("Drag and drop or click to upload")
- `03-skill-activated.png` — Skill installed with toggle on + detail pane *(faculty shot — retake)*

## claude.ai web detailed walkthrough (INSTALL_CLAUDE_AI.md)

Pre-step navigation:

- `web-prereq-01-profile-menu.png` — Profile menu showing Settings
- `web-prereq-02-settings-sidebar.png` — Settings → Capabilities highlighted

Capabilities configuration:

- `web-00-capabilities-toggles.png` — "Code execution and file creation" + "Allow network egress" both on
- `web-00b-domain-allowlist.png` — Domain allowlist showing `vusm-curriculum-api.shanestenner.workers.dev` in Additional allowed domains

Skill upload flow:

- `web-01-customize-skills.png` — Customize → Skills with "+" button and "Add skill" tooltip
- `web-02-add-menu-cascade.png` — Full menu cascade: "+" → "+ Create skill" → "Upload a skill"
- `web-03-upload-dialog.png` — Upload skill modal ("Drag and drop or click to upload")
- `web-04-skill-enabled.png` — Skills list with the skill installed + detail pane *(faculty shot — retake)*

Optional "Try it" / success illustrations:

- `web-05-try-query.png` — Chat composer with the skill invoked + a sample query *(faculty shot — retake with a Coach/Tutor example)*
- `web-06-try-response.png` — Example response showing VUSM-specific evidence *(faculty shot — retake)*

## Capture notes

When refreshing these (UI drift, retaking the skill-specific shots, etc.):

- Blur or crop out: account email, profile photo, session sidebar items,
  any other personally-identifying information.
- For the student pilot, the "try" shots ideally show a Student Coach
  study-planning answer or a Student Tutor hint-first exchange.
- The `web-00b-domain-allowlist.png` shot deliberately shows the API
  hostname pre-populated; that's the key install step testers hit if a
  skill installs but queries fail.

The canonical install flow lives in Anthropic's article (linked above).
If their UI changes substantively, that page updates before this one does.
