---
layout: archive
title: "Using AI in Research"
permalink: /resources/ai-in-research/
author_profile: true
---

{% include toc %}

This is my personal, evolving guide to using AI in research: practical workflows for literature review and agentic coding in computational epidemiology, with an accompanying example repository. It reflects how I actually work, not a definitive prescription. The tools are changing quickly, and so is this page.

A principle runs through everything below: AI can accelerate the work, but scientific judgment and validity remain the responsibility of the researcher. The goal is to use these tools deliberately, in ways that strengthen rather than shortcut the reasoning that makes research trustworthy.

[← Back to Research Practice](/resources/research-practice/)

---

## Literature Review Workflows

AI tools are genuinely useful for navigating literature, especially when entering an unfamiliar field or scoping a new project. I treat them as a way to orient faster, not as a substitute for reading.

**Identifying relevant papers and research directions.** When starting in a new area, I ask AI to map the landscape: foundational papers, key authors, competing approaches, and open problems. This gives me a scaffold to read into. The references it produces must be verified, since models routinely invent plausible-looking citations.

**Building search strategies.** Translating a research question into a structured search is something AI does well. It can help draft Boolean queries, suggest synonyms and MeSH terms for PubMed, and surface terminology used across different subfields, which is helpful for systematic-review-style searches.

**Summarizing papers efficiently.** Feeding in a paper and asking for a structured summary (question, data, methods, key findings, stated limitations) is a fast way to triage what is worth a careful read. I use this for breadth, never as a replacement for reading the papers that matter.

**Comparing methods across studies.** In modeling, approaches to the same question can differ enormously. AI can help draft a comparison table across several studies, such as model structure, assumptions, data sources, and inference method, which I then correct and refine. It is a starting point for synthesis, not the synthesis itself.

**Creating annotated bibliographies.** Generating draft annotations to edit is faster than writing each from scratch. The judgment about what each paper contributes, and how it relates to my own work, stays with me.

**Generating research questions.** AI is a useful brainstorming partner for identifying gaps and framing questions. Deciding which questions are actually worth pursuing is where domain expertise is irreplaceable.

### A note on limitations

AI-generated summaries should always be checked against the original paper. Models can miss methodological nuances, misinterpret results, or hallucinate findings. The risk is highest exactly where it matters most: the assumptions, caveats, and subtle design choices that determine whether a study's conclusions hold. Use AI to read faster, not to avoid reading.

---

## Agentic Coding for Research Projects

For research code, I increasingly work with coding agents rather than writing everything by hand. What differentiates this from "just letting AI write code" is the structure around it: a clear specification, work delivered in reviewable phases, and validation built in from the start.

The high-level workflow I follow:

```
Research Question
       ↓
Project Specification
       ↓
Agent-Assisted Development
       ↓
Testing & Validation
       ↓
Human Review
       ↓
Research Output
```

### Planning

Good agentic coding is mostly good planning. The time spent here pays off many times over.

- **Write a project specification.** I capture the research question, data, modeling assumptions, and intended outputs in a `project_spec.md` file, and I make it very specific. Vague specifications produce vague (and often wrong) code. This file becomes the shared reference for both me and the agent.
- **Define modeling assumptions explicitly.** Infectious disease models encode many choices, including transmission structure, compartments, parameter priors, and what is held fixed versus estimated. Stating these in the spec forces clarity and makes the assumptions reviewable rather than buried in code.
- **Decide the folder structure upfront.** This varies from project to project, but it is worth thinking through early. Crucially, plan what should *not* be committed to GitHub. Data is the common case, both for privacy and for size, and belongs in a `.gitignore`d directory from the very first commit.
- **Break the project into tasks.** Decompose the work into discrete, testable pieces rather than one monolithic build.

### Development

- **Build in phases.** Asking an agent to build the whole repository in one shot produces a large amount of unverified code that is hard to trust or review. Working phase by phase keeps each piece small enough to actually check.
- **Generate code, tests, and documentation together.** Tests and docs written alongside the code (not bolted on later) are how I keep the agent's output honest and the project understandable.
- **Iterate.** Refine in tight loops, reviewing and correcting as you go rather than at the end.
- **Use a branch.** I let the agent work on a dedicated branch and only commit and push after I have reviewed the changes myself. Nothing reaches the main branch without human review.

### Reproducibility and Validation

For infectious disease modeling this section matters most, because it is what separates accelerated implementation from accelerated mistakes.

- **Version control** with Git/GitHub for every change.
- **Automated testing** so that behavior is checked continuously, not just once.
- **Reproducible environments**, using containers where possible, so results can be regenerated by others (and by future you).
- **Sensitivity analyses** to understand how conclusions depend on assumptions and parameters.
- **Benchmarking against known results** to confirm the implementation behaves correctly on cases with established answers.
- **Independent verification of model outputs**, ideally with a separate check rather than trusting the first result.
- **Human review of all scientific assumptions**, which is never delegated to the agent.

> AI can accelerate implementation, but scientific validity remains the responsibility of the researcher.

---

## Example Project

To make this concrete, I'm putting together a fully documented example that walks through the entire workflow:

- project specification
- agent-assisted development
- testing workflow
- validation procedures
- reproducible execution

**GitHub Repository:** *coming soon.*
