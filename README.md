# AI Research Paper Humanizer

> A comprehensive system prompt and configuration designed to enforce natural, sequential, and human-readable academic writing across AI assistants (Cursor, Claude Code, Antigravity).

## 🚀 The Core Problem: The AI Feedback Loop

**Papers are now being written for machines, not humans.** 

We are stuck in an optimization loop:
1. **Authors** use AI to draft, which crams dense jargon upfront as an "efficient summary."
2. **Reviewers** get stuck on page one, so they use AI to read and assess it.
3. **The AI Reviewer** easily parses the jargon (because it sees the whole context window at once), passes the paper, and new models are trained to write in this exact unreadable style.

To a human reading linearly from page one, these papers are unreadable. To an AI, they make perfect sense. If readers need an AI to translate every paper, we've outsourced understanding itself. 

## 💡 The Solution

This repository provides a professional-grade ruleset (`SKILL.md` / `.cursorrules`) that fixes the problem by enforcing two core rules:
1. **Humans Read in Order**: The AI must earn the right to use complex jargon by explaining foundational concepts in plain language first. No more context borrowing from page six on page one.
2. **The Humanizer Protocol**: Strips away predictable AI cadence (e.g., filler words like *delve, testament, tapestry, pivotal*) and forces a natural, authentic academic tone without breaking legitimate technical ML vocabulary (like *robust* or *alignment*).

## ⚙️ How to Use

### For Cursor Users
Copy the contents of `SKILL.md` into your `.cursorrules` file at the root of your research paper repository.

### For Claude Code Users
Save `SKILL.md` into your local skills directory (e.g., `~/.claude/skills/ai-research-paper-humanizer/SKILL.md`).

### For Antigravity Users
Save `SKILL.md` into your global config directory (e.g., `~/.gemini/config/skills/ai-research-paper-humanizer/SKILL.md`).

### As a Custom GPT / Claude Project Prompt
Simply paste the entire `SKILL.md` content into your system instructions when drafting, editing, or reviewing a paper.

## 🤝 Contributing
Read your paper as a stranger would. If an AI has to guess what your first page means, a human can't understand it either. Pull requests to improve the humanizer constraints are welcome!
