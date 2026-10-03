# AI Research Paper Humanizer

> A configuration for AI assistants that enforces clear, sequential, human-readable academic writing. Use when writing, editing, or reviewing a research paper.

## The Core Problem: The AI Feedback Loop

Papers are now being written for machines, not humans.

We are stuck in a loop:
- Authors use AI to draft. The model crams dense jargon upfront as shorthand for the whole contribution.
- Reviewers get stuck on page one and ask AI to summarize it for them.
- The AI reviewer easily parses the jargon (it sees the entire paper at once), passes the paper, and the next generation of models is trained to write in exactly this style.

To a human reading linearly from page one, these papers are difficult to follow. To an AI, they make perfect sense. If readers need AI translation to understand a paper, something has gone wrong at the writing stage.

## The Solution

This repository provides a ruleset (`SKILL.md` / `.cursorrules`) that enforces two core principles:

**Sequential structure**: concepts are introduced in the order a reader needs them. Nothing on page one borrows from page six.

**Plain technical writing**: filler vocabulary and rhetorical decoration are removed without touching legitimate technical terms (robust, alignment, significance, etc.).

The skill also includes a full reviewer checklist covering baselines, ablations, reproducibility, and claims that outrun the evidence — not just jargon.

## How to Use

**Cursor** — Copy `SKILL.md` into `.cursorrules` at the root of your repository.

**Claude Code** — Save to `~/.claude/skills/ai-research-paper-humanizer/SKILL.md`.

**Antigravity / Gemini CLI** — Save to `~/.gemini/config/skills/ai-research-paper-humanizer/SKILL.md`.

**Custom GPT or Claude Project** — Paste the full `SKILL.md` contents into your system prompt when drafting or reviewing.

## Contributing

Pull requests that improve the writing directives or extend the reviewer checklist are welcome. If a rule breaks a real paper you are working on, open an issue with an example and we will fix the rule rather than the paper.
