# ![{{ cookiecutter.name }}](docs/images/{{ cookiecutter.name_noslash }}_logo.png)

**{{ cookiecutter.description }}**.

[![GitHub Actions CI Status](https://github.com/{{ cookiecutter.name }}/workflows/nf-core%20CI/badge.svg)](https://github.com/{{ cookiecutter.name }}/actions)
[![GitHub Actions Linting Status](https://github.com/{{ cookiecutter.name }}/workflows/nf-core%20linting/badge.svg)](https://github.com/{{ cookiecutter.name }}/actions)
[![Nextflow](https://img.shields.io/badge/nextflow-%E2%89%A519.10.0-brightgreen.svg)](https://www.nextflow.io/)

[![install with bioconda](https://img.shields.io/badge/install%20with-bioconda-brightgreen.svg)](https://bioconda.github.io/)
[![Docker](https://img.shields.io/docker/automated/{{ cookiecutter.name_docker }}.svg)](https://hub.docker.com/r/{{ cookiecutter.name_docker }})
[![Get help on Slack](http://img.shields.io/badge/slack-nf--core%20%23{{ cookiecutter.short_name }}-4A154B?logo=slack)](https://nfcore.slack.com/channels/{{ cookiecutter.short_name }})

## Introduction

The pipeline is built using [Nextflow](https://www.nextflow.io), a workflow tool to run tasks across multiple compute infrastructures in a very portable manner. It comes with docker containers making installation trivial and results highly reproducible.

## Quick Start

1. Install [`nextflow`](https://nf-co.re/usage/installation)

2. Install either [`Docker`](https://docs.docker.com/engine/installation/) or [`Singularity`](https://www.sylabs.io/guides/3.0/user-guide/) for full pipeline reproducibility _(please only use [`Conda`](https://conda.io/miniconda.html) as a last resort; see [docs](https://nf-co.re/usage/configuration#basic-configuration-profiles))_

3. Download the pipeline and test it on a minimal dataset with a single command:

    ```bash
    nextflow run {{ cookiecutter.name }} -profile test,<docker/singularity/conda/institute>
    ```

    > Please check [nf-core/configs](https://github.com/nf-core/configs#documentation) to see if a custom config file to run nf-core pipelines already exists for your Institute. If so, you can simply use `-profile <institute>` in your command. This will enable either `docker` or `singularity` and set the appropriate execution settings for your local compute environment.

4. Start running your own analysis!

    <!-- TODO nf-core: Update the example "typical command" below used to run the pipeline -->

    ```bash
    nextflow run {{ cookiecutter.name }} -profile <docker/singularity/conda/institute> --input '*_R{1,2}.fastq.gz' --genome GRCh37
    ```

See [usage docs](docs/usage.md) for all of the available options when running the pipeline.

## Documentation

The {{ cookiecutter.name }} pipeline comes with documentation about the pipeline which you can read at [https://nf-core/{{ cookiecutter.short_name }}/docs](https://nf-core/{{ cookiecutter.short_name }}/docs) or find in the [`docs/` directory](docs).

<!-- TODO nf-core: Add a brief overview of what the pipeline does and how it works -->

## Credits

{{ cookiecutter.name }} was originally written by {{ cookiecutter.author }}.

## Contributions and Support

If you would like to contribute to this pipeline, please see the [contributing guidelines](.github/CONTRIBUTING.md).

For further information or help, don't hesitate to get in touch on the [Slack `#{{ cookiecutter.short_name }}` channel](https://nfcore.slack.com/channels/{{ cookiecutter.short_name }}) (you can join with [this invite](https://nf-co.re/join/slack)).

## Citation

<!-- TODO nf-core: Add citation for pipeline after first release. Uncomment lines below and update Zenodo doi. -->
<!-- If you use  {{ cookiecutter.name }} for your analysis, please cite it using the following doi: [10.5281/zenodo.XXXXXX](https://doi.org/10.5281/zenodo.XXXXXX) -->

You can cite the `nf-core` publication as follows:

> **The nf-core framework for community-curated bioinformatics pipelines.**
>
> Philip Ewels, Alexander Peltzer, Sven Fillinger, Harshil Patel, Johannes Alneberg, Andreas Wilm, Maxime Ulysse Garcia, Paolo Di Tommaso & Sven Nahnsen.
>
> _Nat Biotechnol._ 2020 Feb 13. doi: [10.1038/s41587-020-0439-x](https://dx.doi.org/10.1038/s41587-020-0439-x).
> ReadCube: [Full Access Link](https://rdcu.be/b1GjZ)
