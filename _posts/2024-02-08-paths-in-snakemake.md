---
layout: post
title:  "Paths in Snakemake"
date:   2024-02-08
categories: bioinformatics snakemake
---

The workflow manager Snakemake is popular in bioinformatics and has an active
community. However, like any open source project that has grown by accretion,
it's got some weird quirks, and I've seen myself how the documentation has
grown to a sprawl over the years.

Something which always tripped me up is how Snakemake handles paths. Depending
on where and how they are specified, they are defined relative to different
reference points, so it's easy to get confused.

So I sat down and combed through the docs to come up with the Definitive Guide
to paths in Snakemake, as of the latest major release, v8, though the following
also apply at least as far back as v6, as far as I can recall. I'm sure I'll
have to come back and refresh my memory again at some point, and hope it will
be useful to anyone else struggling with this.

* The **working directory**, or workdir, is the path where the `snakemake`
  command is called, unless overridden.
* The workdir can be overriden with the command line option `--workdir`, or the
  `workdir:` option in the Snakefile
  ([doc](https://snakemake.readthedocs.io/en/stable/snakefiles/configuration.html#configure-working-directory))
* Within Snakemake rules, the `input:` and `output:` file paths are
  **relative to the workdir**.
* However, within a rule, the paths to an external script under `script:`
  ([doc](https://snakemake.readthedocs.io/en/stable/snakefiles/rules.html#external-scripts))
  and to a Conda environment YAML definition file under `conda:`
  ([doc](https://snakemake.readthedocs.io/en/stable/snakefiles/deployment.html#integrated-package-management))
  are **relative to the Snakefile** containing the rule/directive.
* For example, if the Snakefile containing the rule is located at
  `./workflow/rules/set1.smk`, and a Conda environment file is at
  `./workflow/envs/env1.yaml`, then the path to the Conda YAML file in the rule
  should be: `conda: "../envs/env1.yaml"`.
* `include:` paths for additional Snakefiles are **relative to the including
  Snakefile**, regardless of workdir
  ([doc](https://snakemake.readthedocs.io/en/stable/snakefiles/modularization.html#includes))
* **Avoid using absolute paths**, because they prevent portability and reusability
  of the pipeline (although I think it's fair if one decides that the
  additional effort to make a workflow portable is not worth it)
* Another warning from the docs: "...although it might be tempting, please
  refrain from trying to generate output file paths with string concatenation
  of a central outdir variable or so, as this hampers readability"
