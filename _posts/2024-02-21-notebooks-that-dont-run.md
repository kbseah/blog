---
layout: post
title:  "Computational notebooks that don't run"
date:   2024-02-21
categories: bioinformatics
---

Most Jupyter notebooks published alongside research papers [don't
run](https://doi.org/10.1093/gigascience/giad113).

I'm guilty of this myself, most of the notebooks I've published won't run as-is
if you pull them off GitHub.

From the latest [Research Computing Teams
newsletter](https://newsletter.researchcomputingteams.org/archive/rct-176-nurture-your-best-clients-first-plus/)
by Jonathan Dursi:

> There’s a lot of focus in discussions of this work on the fact that 22.5k
> notebooks, only 1.2k ran. I don’t think that’s anything like the biggest
> problem uncovered here.

> For a one-off research paper, the purpose of publishing a notebook is not so
> that someone else can click “run all cells” and get the answer out. That’s a
> nice-to-have. It means that researchers that choose to follow up have an
> already-working starting point, which is awesome, but that’s an efficiency
> win for a specific group of people, not a win for scientific reproducibility
> as a whole.

> There are people saying that we should have higher standards and groups who
> publish notebooks should put more people time into making sure the notebooks
> reliably run on different installs/systems/etc. That’s a mistake. For the
> purposes of advancing science, every person-hour that would go into doing the
> work of testing deployments of notebooks on a variety of systems would be
> better spent improving the papers’ methods section, code documentation, and
> making sure everything is listed in the requirements.txt, and then going on
> to the next project.


Dursi then goes on to say: most research code is effectively only ever run
once, by the people who wrote it. Making code programmatically reproducible is
a lot of work, and for most projects the labor involved simply isn't justified.
He argues that rather than automatic execution being the goal, the priority
should be to fill in the documentation gap, namely those notebooks/projects
that don't declare all their dependencies.

That aligns with my own experience: the notebook is documentation, like a lab
notebook for wet lab experiments. We don't expect to completely reproduce a
physical experiment from a lab notebook, either. A notebook contains relevant
information so that the procedures can be reconstructed later. Of course,
what's "relevant" depends on who's asking.

Better integration of computational notebooks with environment definitions
would improve documentation. At the moment, if I want to spin up a notebook
that uses a specific Conda environment, it's a bit of a faff: I have to create
the environment first, do something involving `ipykernel` that I never remember
off the top of my head, and then tell Jupyter to us this environment for this
notebook. But once I move the notebook somewhere else, or do something to the
environment, everything breaks.

Ideally I want the environment (just the definition, to keep it lightweight) to
be defined in the notebook itself, so that both can be shared together in one
file. The [davos](https://github.com/ContextLab/davos) package seems to offer
this functionality for Python libraries ([arXiv
preprint](https://arxiv.org/abs/2211.15445)). Instead of the usual Python
`import` statement, davos offers an alternative called `smuggle` that will
install and import a specific Python package version automatically into a
virtual environment. Unfortunately this only works for pip-installable
packages, but the authors say they plan to extend it to conda in the future.
