# nf-core/ampliseq
**16S rRNA amplicon sequencing analysis workflow using QIIME2**

[![Build Status](https://travis-ci.org/nf-core/ampliseq.svg?branch=master)](https://travis-ci.org/nf-core/ampliseq)
[![Nextflow](https://img.shields.io/badge/nextflow-%E2%89%A518.10.1-brightgreen.svg)](https://www.nextflow.io/)

[![install with bioconda](https://img.shields.io/badge/install%20with-bioconda-brightgreen.svg)](http://bioconda.github.io/)
[![Docker](https://img.shields.io/docker/automated/nfcore/ampliseq.svg)](https://hub.docker.com/r/nfcore/ampliseq)
![Singularity Container available](
https://img.shields.io/badge/singularity-available-7E4C74.svg)

### Introduction
**nfcore/ampliseq** is a bioinformatics analysis pipeline used for 16S rRNA amplicon sequencing data.

The workflow processes raw data from FastQ inputs ([FastQC](https://www.bioinformatics.babraham.ac.uk/projects/fastqc/)), trims primer sequences from the reads ([Cutadapt](https://journal.embnet.org/index.php/embnetjournal/article/view/200)), imports data into [QIIME2](https://qiime2.org/), generates amplicon sequencing variants (ASV, [DADA2](https://www.nature.com/articles/nmeth.3869)), classifies features against the [SILVA](https://www.arb-silva.de/) [v132](https://www.arb-silva.de/documentation/release-132/) database, excludes unwanted taxa, produces absolute and relative feature/taxa count tables and plots, plots alpha rarefaction curves, computes alpha and beta diversity indices and plots thereof, and finally calls differentially abundant taxa ([ANCOM](https://www.ncbi.nlm.nih.gov/pubmed/26028277)). See the [output documentation](docs/output.md) for more details of the results.

The pipeline is built using [Nextflow](https://www.nextflow.io), a workflow tool to run tasks across multiple compute infrastructures in a very portable manner. It comes with docker / singularity containers making installation trivial and results highly reproducible.


### Documentation
The nf-core/ampliseq pipeline comes with documentation about the pipeline, found in the `docs/` directory:

1. [Installation](docs/installation.md)
2. Pipeline configuration
    * [Local installation](docs/configuration/local.md)
    * [Adding your own system](docs/configuration/adding_your_own.md)
3. [Running the pipeline](docs/usage.md)
4. [Output and how to interpret the results](docs/output.md)
5. [Troubleshooting](docs/troubleshooting.md)
