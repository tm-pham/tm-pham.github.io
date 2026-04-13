---
layout: archive
title: "Resources"
permalink: /resources/
author_profile: true
---

Over the years, I've collected books, papers, tutorials, and tools that have helped me grow as a researcher. Some of these I discovered through coursework or colleagues; others I stumbled on while trying to figure something out on my own. This page is an attempt to organize and pass them on.

The collection reflects my own path and interests, so it leans toward infectious disease modeling, epidemiological methods, and the practical side of academic life. It's not meant to be exhaustive. I've tried to highlight resources that I've personally found useful or that I'd recommend to a student or collaborator who asked me where to start.

I've split things into two sections. **Research practice** covers the "how" of doing science day to day: navigating AI tools thoughtfully, improving your writing, giving better talks, and staying organized. **Methods** covers quantitative tools I use in my own work and that come up often in infectious disease epidemiology.

This page is a work in progress. If you have suggestions for resources I should add, I'd love to [hear from you](mailto:{{ site.author.email }}).

---

## I. Research Practice

### AI in Science

Generative AI has arrived faster than we were able to develop frameworks for it. The question is no longer *if* we incorporate these tools into our work, but *how*. What concerns me is that the pace of change is outrunning our ability to respond.

This matters because generative AI is not just changing how we work; it is changing how we teach and how students learn. People increasingly ask whether a PhD is still worth pursuing in a world where AI can write code, draft manuscripts, and summarize literature. I think the question itself is valuable, because it forces a more philosophical reckoning with what the PhD is really for. My view is that it is fundamentally about developing reasoning skills: learning to think independently, navigate ambiguity, and build scientific judgment in a confusing, chaotic world. Generative AI does not diminish the importance of these skills. If anything, it makes it even more important.

But that is not an argument for rejecting these tools. It is an argument for being deliberate about how and when we use them, particularly during training.

If you are navigating this as a PhD student, postdoc, or mentor, I highly recommend the resources below by Arjun Krishnan, which offer both a principled framework and practical, task-specific guidance for incorporating generative AI into research training.

- Krishnan, A. (2026). [Build expertise first: why PhD training must sequence AI use after foundational skill development](https://doi.org/10.5281/zenodo.18649847). *Zenodo*.
- Krishnan, A. (2026). [Expertise before augmentation: a practical guide to using generative AI during research training](https://zenodo.org/records/18452320). *Zenodo*.

### Academic Writing

My colleague Stephen Kissler has put together an excellent guide on writing academic manuscripts, covering everything from structuring a paper to navigating the revision process.

- Kissler, S. [A guide to writing academic manuscripts](https://kisslerlab.github.io/guides/manuscripts/).

### Academic Presentations

Dan Larremore's guide on giving academic talks is one of the best I've come across. It's very practical and useful whether you're preparing your first conference talk or your fiftieth.

- Larremore, D. [Guide to giving academic presentations](https://drive.google.com/file/d/13efH6iA6toPtJ91KBt_QCeAyQBcSN7SA/view).

### Organizational Tools

There's no shortage of opinions about the "best" tools for note-taking and organization. In my experience, the best tool is the one you'll actually use. Which one that is depends on your workflow, your preferences, and how much you're willing to spend. Don't expect to get it right on the first try. Expect to switch tools at some point. Trial and error is how most people land on what works for them. Here are just some of my suggestions:

- **[Notion](https://www.notion.so/)** and **[Obsidian](https://obsidian.md/)** for note-taking and organization
- **[GitHub](https://github.com/)** for code and project management
- **[Zotero](https://www.zotero.org/)** and **[Mendeley](https://www.mendeley.com/)** for reference management

---

## II. Methods

### Causal Inference

Causal inference is a large and rapidly growing field, and it can be hard to know where to start. Brady Neal's website does a nice job of mapping out the landscape and helping you pick a book based on your background.

- Neal, B. [Which causal inference book should you read?](https://www.bradyneal.com/which-causal-inference-book)

For a hands-on, example-driven introduction, I've found Scott Cunningham's *Causal Inference: The Mixtape* particularly accessible. It's freely available online and also published as a book.

- Cunningham, S. [Causal Inference: The Mixtape](https://mixtape.scunning.com/).

### Bayesian Statistics

If you're new to Bayesian statistics, Richard McElreath's *Statistical Rethinking* is one of the best places to start. It requires relatively little prior background in statistics, and the lectures and code are freely available online.

- McElreath, R. (2020). *Statistical Rethinking*, 2nd Edition. Chapman and Hall. [GitHub](https://github.com/rmcelreath/stat_rethinking_2e)

For those with a stronger statistics background, Gelman et al.'s *Bayesian Data Analysis* is a classic and goes much deeper:

- Gelman, A., Carlin, J.B., Stern, H.S., Dunson, D.B., Vehtari, A. & Rubin, D.B. (2013). *Bayesian Data Analysis*, 3rd Edition. Chapman and Hall/CRC. [R demos](https://avehtari.github.io/BDA_R_demos/)

Finally, this paper by Gelman, Vehtari, and colleagues lays out a principled Bayesian workflow from start to finish. A book version is expected in June 2026.

- Gelman, A., Vehtari, A., Simpson, D., et al. [Bayesian Workflow](https://arxiv.org/abs/2011.01808). *arXiv*. See also: [Bayesian Workflow book](https://avehtari.github.io/Bayesian-Workflow/).

### Mathematical Modeling of Infectious Diseases

These are the textbooks I return to most often. Each one takes a somewhat different angle — from applied simulation to formal mathematical analysis to data-driven modeling in R.

- Keeling, M.J. & Rohani, P. *Modeling Infectious Diseases in Humans and Animals*. A comprehensive guide covering practical applications, simulation techniques, and model analysis. [Website](https://www.math.uconn.edu/~rohani/book/)
- Diekmann, O. & Heesterbeek, J.A.P. *Mathematical Epidemiology of Infectious Diseases*. Focuses on model building, analysis, and interpretation; suited for a more formal mathematical approach. [Springer](https://www.springer.com/gp/book/9780471986829)
- Anderson, R.M. & May, R.M. *Infectious Diseases of Humans: Dynamics and Control*. A foundational text in the field, often cited for its deep theoretical treatment of host–pathogen dynamics.
- Bjørnstad, O.N. *Epidemics: Models and Data using R*. Combines epidemic modeling with practical implementation in R — a good entry point if you want to learn by doing. [Springer](https://www.springer.com/gp/book/9783319974866)

### Coding

Most of us in epidemiology and infectious disease modeling are largely self-taught programmers. These resources fill gaps that formal training often leaves behind.

#### R programming and visualization

- Wilke, C.O. [*Fundamentals of Data Visualization*](https://serialmentor.com/dataviz/). A thoughtful guide to designing clear, effective figures — useful well beyond R.

#### General coding

- Athalye, A., Zhu, J. & Hålaj, A. [The Missing Semester of Your CS Education](https://missing.csail.mit.edu/). Covers the practical tools — the shell, version control, debugging, and more — that most curricula skip over but that you'll use every day.
