# Snakemake workflow: Short-read-mapping-and-QC-snakemake-pipeline

[![Snakemake](https://img.shields.io/badge/snakemake-≥6.3.0-brightgreen.svg)](https://snakemake.github.io)
[![GitHub actions status](https://github.com/<owner>/<repo>/workflows/Tests/badge.svg?branch=main)](https://github.com/<owner>/<repo>/actions?query=branch%3Amain+workflow%3ATests)

A Snakemake workflow for read mapping and QC analysis for short read sequencing data. This workflow is under development.This Snakemake workflow includes the following tools to process mutiple samples of the short pair-end sequencing data (WGS).

## Snakemake workflow includes:


![short read Mapping and QC snakemakeworkflow](https://github.com/vkpat/short-read-mapping-and-QC-snakemake-pipeline/assets/143219019/de6b9ac3-bc25-47d4-b350-cb2d1b7aa6be)

FastQC

BWA-MEM

Samtools stats

Mosdepth

Picard collect metrics

MultiQC

## Installation instructions

Download the latest code from Github:

git clone https://github.com/vkpat/short-read-mapping-and-QC-snakemake-pipeline.git

 ## Requirement

Software requirement to install dependencies is conda or mamba. It is best to create a new conda or mamba envirnoment using the provided YAML file:

- mamba env create -f environment.yaml

- mamba activate envirnoment

## Reference genome

You will need to download the reference genome manually before running the workflow. Multiple references such as GRCh38, GRCh37 and CHM13 can be used to run this short-read Mapping and QC workflow 

## Authors

Nate Olson

Vaidehi Patel
