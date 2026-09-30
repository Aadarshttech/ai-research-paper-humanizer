# AI Research Paper Humanizer ✍️🤖 ➡️ 🧑‍🔬

[![GitHub stars](https://img.shields.io/github/stars/Aadarshttech/ai-research-paper-humanizer.svg?style=social&label=Star)](https://github.com/Aadarshttech/ai-research-paper-humanizer) 

**The ultimate system prompt and skill for Cursor, Claude Code, and Antigravity to write and review research papers like a human.**

Are you tired of AI writing academic papers packed with dense, undefined terminology that only machines can understand? This repository contains a professional-grade prompt/skill (`SKILL.md` / `.cursorrules`) that forces LLMs to write sequential, easily readable, and humanized research papers.

## 🚀 Why This Matters (The Problem)

**Papers are now being written for machines, not humans.** 

More and more research papers open with undefined, paper-specific terms that only make sense once you've read the whole document. A human reading linearly from page one can't follow them, but an AI—with the entire paper in its context window—explains them instantly. 

We are stuck in an optimization loop:
1. **Reviewers** increasingly rely on AI to read and assess submissions.
2. **Dense, jargon-heavy papers** score higher with AI because they look sophisticated, even if they are unreadable to humans.
3. **Accepted papers** train the next generation of models, teaching them to write the same way by default.
4. **Authors** draft with those models, and the cycle continues.

If readers need an AI to translate every paper, we've outsourced understanding itself. 

## 💡 The Solution: Human-First Academic Writing

This skill file fixes the problem by enforcing two core rules:
1. **Humans Read in Order**: The AI must earn the right to use complex jargon by explaining foundational concepts in plain language first.
2. **The Humanizer Protocol**: Strips away predictable AI cadence (e.g., words like *delve, testament, tapestry, pivotal*) and forces a natural, authentic academic tone.

## ⚙️ How to Use

### For Cursor Users
Copy the contents of `SKILL.md` into your `.cursorrules` file at the root of your research paper repository.

### For Claude Code / Antigravity Users
Save `SKILL.md` into your local skills directory (e.g., `~/.gemini/config/skills/ai-research-paper-humanizer/SKILL.md`).

### As a Custom GPT / Claude Project Prompt
Simply paste the entire `SKILL.md` content into your system instructions when drafting or reviewing a paper.

## 🔍 SEO Keywords (For Discoverability)
*Write research paper with AI, AI research paper humanizer, academic writing AI prompt, bypass AI detection research paper, Claude research paper prompt, ChatGPT academic writer, Cursor rules for research papers, humanize AI text academic, write like a human AI.*

## 🤝 Contributing
Read your paper as a stranger would. If an AI has to guess what your first page means, a human can't understand it either. Pull requests to improve the humanizer constraints are welcome!
