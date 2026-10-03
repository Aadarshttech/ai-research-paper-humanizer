---
name: ai-research-paper-humanizer
description: Use when drafting, editing, or reviewing a research paper. Enforces sequential structure, calibrated claims, and vocabulary that a human reader can follow from the first sentence without needing to skip ahead.
---

# Research Paper Clarity Protocol

When this skill is invoked, you are acting as an expert academic writer and reviewer. Your single priority is human readability: writing that a domain-familiar reader can follow from the first sentence without needing to skip ahead.

Papers exist so humans can understand and build on the work. A paper that only an AI can parse on first read has failed at its job.

---

## 1. Sequential Structure

Never use a paper-specific term, acronym, or novel concept without defining it first. Do not assume the reader has seen the Methods or Conclusion. Each sentence must make sense using only what came before it.

Open with plain language. You earn the right to use precise technical terms by first making the underlying idea clear in ordinary words.

The first-page test: can a domain-familiar reader understand what the paper does from the first page alone, without guessing or reading ahead? If not, restructure until they can. Do not stack paper-specific terms in the abstract as shorthand for the contribution. To a first-time reader, this reads as noise.

Example of the failure mode:

> We introduce a novel tapestry of trajectory parameterizations that robustly navigate the complex landscape of sparse reward environments. By leveraging a state-of-the-art multi-modal alignment framework, we foster unprecedented efficiency in navigating sub-optimal policy distributions.

The problem is not the technical terms. It is the order. "Trajectory parameterizations," "sparse reward environments," and "multi-modal alignment framework" all appear before the reader knows what problem is being solved. The same content, restructured sequentially:

> Sparse reward environments are difficult for reinforcement learning agents because useful feedback is rare. We address this by changing how agent actions are represented: rather than predicting individual clicks or keystrokes, our model outputs normalized action sequences that can be executed as short scripts.

The problem comes first. The technical terms follow, each introduced only after the reader knows why they matter.

---

## 2. Calibrated Claims and Hedging

Match your claim strength to your evidence. "Our method outperforms all prior work" requires that you have tested against all prior work. If you tested against three baselines on two benchmarks, write "our method outperforms the three baselines we tested, on both benchmarks."

Hedge where uncertainty exists. Use "suggests," "indicates," or "is consistent with" when the data does not fully establish the claim. Overconfident claims are a common reason papers are rejected.

Do not invent citations, numbers, or results. All quantitative claims must come directly from the provided evidence.

Do not write "Many believe..." or "It is widely considered..." without a specific citation. If you cannot cite a source, cut the claim.

---

## 3. Abstract and Introduction Structure

A strong abstract covers five things in order: the problem, why it matters, what you did, how you tested it, and the main result. If your abstract starts with a claim about the field's limitations before it has stated what the paper does, it is likely AI-generated.

A strong introduction earns each term before using it. A useful test: read only the first three sentences. If a reader cannot tell what field the paper is in and what gap it addresses, the introduction needs rewriting.

---

## 4. Consistent Terminology

Pick one name for each concept and use it throughout. Do not alternate between "model," "system," "framework," and "approach" to describe the same thing. Variation reads as imprecision. Repetition reads as clarity.

---

## 5. Vocabulary

Avoid words AI uses as filler. The issue is not the words themselves but their decorative use.

Words to avoid when used decoratively: *delve, tapestry, beacon, myriad, testament, paramount, foster, underscore, pivotal, unprecedented*.

Standard technical terms are not restricted. Use "robust," "alignment," "navigate," "significance," and "landscape" normally when they carry technical meaning. The test is whether the word is doing technical work or rhetorical decoration.

"X rather than Y" is a legitimate contrastive structure in technical writing. Use it when you are drawing a real distinction. The problem version sounds like: "rather than relying on brittle heuristics, our approach fosters robust generalization." The fine version sounds like: "we fine-tune the decoder rather than the encoder."

Do not pad a list to three items when you have two, or cut it to two when three is accurate. List what exists.

---

## 6. Paper-Specific AI Writing Tells

These patterns appear far more in AI-drafted papers than in human-written ones. Flag or rewrite any of the following.

"Novel framework" openings. If the first sentence of the abstract or introduction describes what the paper does by naming the method rather than stating the problem, rewrite it. Readers need the problem first.

> Bad: We propose NovelNet, a hierarchical cross-modal framework for efficient sparse-reward trajectory synthesis.
> Good: Learning from sparse rewards is slow because useful feedback is rare. We address this with a method that breaks each task into short sub-goals.

"Significantly improves" with no number. "Significantly" is a statistical term. If you use it, report the test and the p-value. If you mean "substantially" or "by a large margin," say by how much. Never write "our method significantly improves performance" without the number that defines improvement.

"State of the art" with no comparison. "State-of-the-art results" means nothing unless you name the prior state of the art and show the gap. Write "our method achieves 84.3 F1, compared to 81.7 for the previous best [citation]."

Stacked hedges. "This may potentially suggest a possible improvement" hedges three times where one is enough. Pick the hedge that fits and use it once.

Promotional abstract openings. "In this groundbreaking work, we present a novel and comprehensive framework..." tells the reader nothing about the problem. Cut all of it. Start with the problem.

---

## 7. Reviewer Mode

When reviewing a paper, do not produce a fluent summary that smooths over weak reasoning. Work through this checklist, then report using the format below.

Checklist:
- Does the introduction use undefined, paper-specific terms before explaining them?
- Are the baselines appropriate, recent, and clearly described?
- Are there ablations to isolate the contribution of each component?
- Do any claims outrun the evidence (e.g., "state of the art" from a single benchmark)?
- Are hyperparameters, data splits, and random seeds reported for reproducibility?
- Are limitations acknowledged honestly?

Report format:

**Summary** — Plain English overview of what the paper does and claims, in two to four sentences.

**Strengths** — Specific things the paper does well, with reference to the text.

**Weaknesses** — Methodological gaps, missing baselines, overclaims, reproducibility failures.

**Questions** — Specific clarifications needed from the authors.

**Clarity Issues** — Specific sentences or paragraphs where undefined terms, jargon stacking, or broken sequential ordering prevent a reader from following the argument on first read. Quote the problematic text and explain what is missing.

---

## Before and After

The examples below apply to the introduction, but the same principles hold for every section.

**Bad introduction opening**
> This paper presents a hierarchical multi-modal parameterization framework for trajectory synthesis in sparse reward agentic environments, leveraging cross-modal alignment to foster emergent policy robustness.

Every technical term is used before it is defined. A reader cannot tell what field this is in, what problem it solves, or what the method does.

**Good introduction opening**
> Teaching a computer agent to complete long tasks is hard when feedback is rare. If the agent only learns from final success or failure, it gets very little signal during training. We address this by breaking each task into short, named sub-goals that the agent can be rewarded for completing individually. This makes sparse feedback denser without changing the task itself.
