# Changelog — VUSM Student Skills

The skills run a quiet version check on the first response of each
conversation. If the deployed version is newer than the one in your
installed bundle, you'll see a one-line "newer version available" note —
email Shane for a refreshed bundle.

## v1.1.0 — 2026-10-28

### New
- **When you first met a topic.** Ask about a concept and Student Coach
  now shows the first dated session in the 2025-26 calendar where it
  appears, the earliest few sessions after that, and the phases they fall
  in. These are calendar facts, labeled with the academic year. For
  2024-25 the skill says no dated session was found.
- **One step to the answer.** Concept questions start with a single
  lookup that brings back coverage, passages, links and prior exposure
  together, so answers come back faster.

### Changed
- **No prerequisite claims.** The curriculum data has no "you must know A
  before B" links, so the skills no longer say one topic is a
  prerequisite for another or that a topic "builds on" an earlier one.
  They say "earlier" only when the session dates show it, and describe
  phases that run at the same time as concurrent.
- **Student Tutor reads before it asks.** On your first turn the tutor
  quietly looks up the topic in the curriculum, so its questions match
  what was taught. It still won't give you the answer before you've tried.

### Privacy
- **Less kept about what you look up.** For student keys, the API's
  access log stores the kind of request, not the topic you asked about,
  and keeps it for 30 days instead of 90.
- **No names in the log.** Each student key is tied to a random ID, not
  your name. Only Shane's private roster links the two.

### Improved
- **26 more slide decks.** Decks the indexer couldn't read before (for
  example `.ppsx` and `.ppsm` files) are now part of the curriculum
  evidence.
- The version check now also reports which data build answers come from
  (UMLS release, MedEdO version and build date).

### Migration
Bundles for v1.1.0 are available on request. It replaces v1.0.0 with
nothing to change in your settings. Older bundles show a "newer version
available" note on their first answer.

## v1.0.0 — 2026-05-21

Initial private preview.

- **Student Coach** (`student-coach`) — curriculum study planner.
- **Student Tutor** (`student-tutor`) — practice tutor; withholds
  answers, hints and elicits reasoning first.
- Both carry a personalized read-only API key and an in-skill
  pilot-feedback path (say "feedback" to get a pre-filled REDCap form).
