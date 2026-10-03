# AI Research Paper Humanizer

> A configuration for AI assistants that enforces clear, sequential, human-readable academic writing. Use when writing, editing, or reviewing a research paper.

## The Problem

More research papers are opening with dense, undefined terminology on the first page — terms that only make sense once you have read the whole paper. A human reading linearly cannot follow them. An AI assistant, which sees the entire document at once, has no difficulty. This creates a feedback loop: AI-assisted reviewing may reward papers written this way, those papers get accepted, and models trained on accepted papers learn to write the same way by default.

The loop is a hypothesis, not an established fact. But the readability problem it produces is real and measurable: when a reviewer needs an AI to translate the introduction before they can evaluate the paper, the communication has already failed.

## The Solution

This repository provides a ruleset (`SKILL.md` / `.cursorrules`) that addresses the problem directly. It enforces:

Sequential structure — concepts are introduced in the order a reader needs them, not in the order convenient for an author who already knows the whole paper.

Calibrated claims — claim strength is matched to evidence, with explicit hedging where uncertainty exists.

Clean vocabulary — filler words are avoided without restricting legitimate technical terminology (robust, alignment, significance, navigate, etc.).

A structured reviewer mode — covering baselines, ablations, reproducibility, and overclaims, not just jargon.

## How to Use

**Cursor** — Copy `SKILL.md` into `.cursorrules` at the root of your repository.

**Claude Code** — Save to `~/.claude/skills/ai-research-paper-humanizer/SKILL.md`.

**Antigravity / Gemini CLI** — Save to `~/.gemini/config/skills/ai-research-paper-humanizer/SKILL.md`.

**Custom GPT or Claude Project** — Paste the full `SKILL.md` contents into your system prompt when drafting, editing, or reviewing.

## Contributing

Pull requests that improve the writing directives, extend the reviewer checklist, or add before/after examples for specific section types are welcome. If a rule breaks a real paper you are working on, open an issue with an example and we will fix the rule rather than the paper.
