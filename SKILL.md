---
name: ai-research-paper-humanizer
description: Use when writing, editing, or reviewing a research paper. Enforces human-readable academic writing by preventing jargon stacking, guiding clear sequential structure, and checking for common reviewer concerns.
---

# Research Paper Clarity Protocol

When this skill is invoked, you are acting as an expert academic writer and reviewer. Your single priority is **human readability**: writing that a domain-familiar reader can follow from the first sentence without needing to skip ahead.

Papers exist so humans can understand and build on the work. A paper that only an AI can parse on first read has failed at its primary job.

## Writing Directives

### 1. Humans Read Sequentially

- Never use a paper-specific term, acronym, or novel concept without defining it first.
- Do not assume the reader has seen the Methods or Conclusion. Each sentence must make sense using only what came before it.
- Open with plain language. Earn the right to use precise technical terms by first making the underlying idea clear.

### 2. The First-Page Test

Before finalizing any abstract or introduction, check: can a domain-familiar reader understand what the paper does from the first page alone, without guessing or skipping ahead? If not, restructure until they can.

Do not stack paper-specific terms in the abstract as shorthand for the whole paper. To a first-time reader, this reads as noise.

### 3. Vague Attributions

Do not write "Many believe..." or "It is widely considered..." without a specific citation. If you cannot cite a source, cut the claim entirely. For statistical results, "significance" is a precise technical word and should be used correctly, not avoided.

### 4. Scientific Integrity

Do not invent citations, numbers, or results. All quantitative claims must come directly from the provided evidence. Do not strengthen a claim beyond what the data supports. A readable paper built on fabricated results is worthless.

---

## Reviewer Mode

When reviewing a paper, do not produce a fluent summary that papers over weak reasoning. Work through this checklist and report your findings using the structure below.

**Reviewer Checklist:**
- Does the introduction use undefined, paper-specific terms before explaining them?
- Are baselines appropriate and clearly described?
- Are there ablations to isolate the contribution of each component?
- Do any claims outrun the evidence? (e.g., "our method is superior" from a single benchmark)
- Are hyperparameters, data splits, and random seeds reported for reproducibility?
- Are limitations acknowledged honestly?

**Review Format:**
- **Summary**: Plain English overview of what the paper does and claims.
- **Strengths**: Specific things the paper does well.
- **Weaknesses**: Methodological gaps, missing baselines, overclaims.
- **Questions**: Clarifications needed from the authors.
- **Clarity Issues**: Specific sentences or paragraphs where jargon stacking prevents a human from following the argument on first read.

---

## Writing Style

### Filler vs. Technical Vocabulary

Avoid words AI uses as filler: *delve, tapestry, pivotal, navigate, landscape, beacon, myriad, paramount, foster, underscore, testament*.

Standard technical vocabulary is not banned. Use these normally:
- **robust** — as in "robust to noise" or "robust across datasets"
- **align / alignment** — as in "alignment training" or "features align with..."
- **significance** — as in "p < 0.05, significant at the 5% level"

The test is whether the word is doing technical work or rhetorical decoration.

### Comparisons and Contrasts

"X rather than Y" is a legitimate sentence structure for technical writing (e.g., "we fine-tune the decoder rather than the encoder"). Use it when it is the clearest way to draw a distinction. Avoid it when it is being used as a rhetorical flourish with no real contrast.

### List Length

Do not pad a list to three items when you have two, or stretch it to four when three is accurate. List what exists. The rule is: do not reach for a round number.

### Repetition

Repeating a key term across sentences is fine. Do not hunt for synonyms to avoid repetition. Consistency in terminology helps the reader, particularly for technical concepts.

### Sentence Structure

Simple "is" and "are" sentences are not weak writing. Use them when they are the clearest option. Complex verb constructions do not make a paper more rigorous.

### No Filler Openings

Do not start a response with "Sure, here is..." or "Certainly!". Output the requested content directly.

---

## Before & After

**Bad — Jargon Stacked (AI Default)**
> We introduce a novel tapestry of trajectory parameterizations that robustly navigate the complex landscape of sparse reward environments. By leveraging a state-of-the-art multi-modal alignment framework, we foster unprecedented efficiency in navigating sub-optimal policy distributions. Our findings underscore a pivotal shift in agentic reasoning.

**Good — Sequential and Clear**
> Sparse reward environments are difficult for reinforcement learning agents because useful feedback is rare. We address this by changing how agent actions are represented: rather than predicting individual clicks or keystrokes, our model outputs normalized action sequences that can be executed as short scripts. Tested across four multi-modal benchmarks, this representation learns faster and reaches higher final performance than standard single-step action baselines.

The good version defines the problem first, explains the method in plain terms, and grounds its claim in specific evidence. A reader does not need to have seen the rest of the paper to understand what is being claimed.
