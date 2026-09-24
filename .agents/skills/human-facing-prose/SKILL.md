---
name: human-facing-prose
description: >-
  Agent-only wording checklist for natural human-facing prose on allowlisted surfaces.
  Use before composing a substantial captain-facing chat outcome, escalation, or decision ask, a public Relay reply or completion follow-up, /bearings chat-line wording, human-facing prose paragraphs in README, VISION, or operator docs, or the human-facing summary of a scout report or PR description.
  Never applies to code, tests, schemas, commands, records, or any other precision, replay, or enforcement text.
user-invocable: false
metadata:
  internal: true
---

# human-facing-prose

This skill is the single owner of Firstmate's human-facing prose wording checklist.
It adapts discourse-level findings about AI-typical prose (StoryScope, arXiv:2604.03136) into an allowlisted anti-pattern checklist; it is not a detector, scorer, or rewriting pipeline, and it runs no StoryScope code, models, or cloud calls.
Existing contracts remain authoritative wherever they overlap: `AGENTS.md` section 9 owns captain etiquette and outcome translation, `fmx-respond` owns public safety and reply brevity, `bearings` owns its chat-response structure, and every existing communication-approval rule is unchanged.
This checklist only tunes wording inside those contracts and never relaxes them.

## Eligible surfaces

Apply this checklist only to:

- Captain-facing chat outcomes, escalations, and decision asks.
- Public Relay replies and completion follow-ups, inside `fmx-respond`'s public-safety list and length cap.
- `/bearings` chat lines: wording inside a line only, never the four-section structure or a required field.
- Human-facing product prose paragraphs in `README.md`, `VISION.md`, and operator docs, when explicitly writing those.
- The human-facing summary at the top of a scout report or PR description, when that summary is meant for a person.

When eligible and excluded material share one document, rewrite only the human-facing summary and leave every evidence block, table, command, and citation byte-for-byte intact.

## Hard exclusions

Never apply this checklist to:

- Code, comments-as-contracts, tests, schemas, CLIs, commands, flags, patches, or commit messages.
- Status lines, metadata, wake records, backlog machine fields, briefs' Firstmate spec, acceptance criteria, or audit evidence.
- `AGENTS.md` safety rules, skill procedures, safety contracts, or script headers.
- File and line citations, and commands or URLs that must be copied verbatim: copy them exactly and do not restyle the path.
- Any other text whose job is precision, replay, or enforcement.

## Checklist

Do:

- Lead with the outcome; never announce the theme, narrate the journey, or state what the work "means".
- Prefer named specifics - the reader's nouns, project names, concrete results, full `https://` URLs - over vague allusion such as "the work" or "the usual path".
- Name real uncertainty and leftover risk plainly instead of resolving it into a tidy lesson.
- Trust the reader: state a thing once and do not recap the recap.
- Preserve every required fact, citation, decision, approval boundary, and authority limit exactly.
- Keep the specified Firstmate voice: address per section 9, optional light seasoning only when it fits, dropped for bad news.

Do not:

- Add sensory metaphor, weather-as-mood, body-sensation emotion, or "show don't tell" flourishes.
- Add flashbacks, subplots, dream sequences, invented stakes, or any other fiction device.
- Invent agency: never change who decided, approved, or did what.
- Optimize for an AI-detector score or any "human rarity" target.
- Conceal AI assistance or any required authorship disclosure.
- Impersonate a specific human author beyond the already specified Firstmate persona.
- Add length: this checklist removes padding, so when applying it would make the text longer, keep the shorter version.

## Revert path

Delete this skill directory and remove its trigger pointers - `AGENTS.md` section 13, the `fmx-respond` Voice section, and the `bearings` chat-response contract - to turn the guidance off completely.
No runtime, daemon, spawn path, or configuration reads this skill, so removal changes nothing but the loaded instructions.
