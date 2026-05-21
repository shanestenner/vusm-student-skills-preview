# Installing in the Claude desktop app (Mac or Windows)

The Claude desktop app supports custom skills with the same flow as
claude.ai web. **Anthropic's official guide is the canonical source** and
covers any UI differences as they evolve:

> **[Anthropic — Use Skills in Claude (Add and Use Custom Skills)](https://support.claude.com/en/articles/12512180-use-skills-in-claude#h_a4222fa77b)**

The desktop app's menu paths can differ slightly between releases, so
the article is what to trust if anything below looks wrong.

---

## The short version

1. **Prerequisites — three Capabilities settings (one-time):**
   - Open the desktop app's settings (menu bar → Claude → Settings… on
     Mac, or the gear icon on Windows).
   - Toggle **"Code execution and file creation"** on.
   - Toggle **"Allow network egress"** on.
   - Scroll to **Domain allowlist** → **Additional allowed domains**,
     paste `vusm-curriculum-api.shanestenner.workers.dev`, click **Add**.
     The default "Package managers only" mode blocks our API unless the
     hostname is listed. (Setting the dropdown to **"All domains"** also
     works.)

2. **Open the Skills configuration:**
   - **Customize → Skills** (same path as the web app).

3. **Upload the bundles — do this twice:**
   - Click the **"+"** at the top of the Skills list.
   - Choose **"+ Create skill"** → **"Upload a skill"**.
   - Select `student-coach-<your-name>.zip`, then repeat for
     `student-tutor-<your-name>.zip`.

4. **Verify:**
   - Both **Student Coach** and **Student Tutor** appear in the list,
     each with a toggle (default: on).

5. **Try them:**
   - New chat → *"What should I study before my renal block exam?"*
     (Coach) or *"Quiz me on acid-base at an application level."* (Tutor).
   - Coach gives VUSM-specific study guidance; Tutor makes you reason
     first instead of handing over answers.

---

## If your desktop app's UI looks different

The desktop app updates frequently and menu wording shifts:

- No **Customize**? Look for **Settings** or a gear icon, then **Skills**.
- Different button labels (e.g., "Add skill")? Follow what your app
  shows — the goal is the same: upload each ZIP.
- No Skills section at all? Use [claude.ai](https://claude.ai) in your
  browser instead — same account, same setup.

When in doubt, **Anthropic's [official guide](https://support.claude.com/en/articles/12512180-use-skills-in-claude#h_a4222fa77b) is more current than this page.**

---

## Troubleshooting

**"Code execution must be enabled" error.**
You missed the prerequisite. Settings → Capabilities → "Code execution
and file creation."

**Upload says "Skill not valid" or similar.**
Upload the `.zip` file (not the unzipped folder). The zips are named
`student-coach-<your-name>.zip` and `student-tutor-<your-name>.zip`.

**Claude says it can't reach the API / "request failed."**
Most common cause: **the API hostname isn't in your Domain allowlist.**
Settings → Capabilities → **Additional allowed domains** → confirm
`vusm-curriculum-api.shanestenner.workers.dev` is listed, and
**"Allow network egress"** is on.

If both are set, it's likely transient — retry in 30 seconds. The
desktop app sometimes needs a restart after sleep/wake.

**I want to remove a skill.**
Customize → Skills → (the skill) → Remove. The bundle is deleted from
your app; the API key is still issued server-side, so you could
re-upload the same zip later — or email Shane to fully revoke the key.
