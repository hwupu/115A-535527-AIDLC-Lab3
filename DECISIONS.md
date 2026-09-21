# Decisions Log

## 2026-09-21 — Initial code steward
**What:** 吳普軒 is the initial code steward for the team.
**Why:** volunteered.

## 2026-09-21 — Local Ollama for the deployed discharge-summary prototype
**What:** The deployed prototype will run an open-weight language model locally
through Ollama to create source-linked discharge-summary drafts. Ollama is a
drafting and evidence-finding tool only; a physician must review, edit or reject
the draft and is the only person who can approve a final summary.

**Why:** Local deployment gives the team a controlled environment for the
prototype and avoids sending authorized test inputs to a public generative-AI
service. This does not remove the need for authorization, access control,
de-identification, and privacy review before any clinical data are used.

**Scope:** Only synthetic cases or properly de-identified, explicitly authorized
records may be used in course testing. Ollama must not diagnose, prescribe,
decide discharge readiness, write directly to a production medical record, or
sign a summary. The detailed evaluation and monitoring plan is in
`EVALUATION_PLAN.md`.

**Led by:** 張棨翔, with code-steward and team review required before implementation.
