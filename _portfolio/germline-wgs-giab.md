---
title: "Germline WGS Benchmarked on GIAB"
excerpt: "FASTQ to ACMG-classified variants, benchmarked on seven GIAB genomes (HG001–HG007), with GATK and DeepVariant compared side by side."
group: "Clinical Genomics"
order: 1
status: "In progress"
stack: [Nextflow, Docker, BWA-MEM2, GATK, DeepVariant, hap.py, VEP, Exomiser]
---

**Repository:** [nesirli/germline-wgs-giab](https://github.com/nesirli/germline-wgs-giab) · **Status:** in progress. Results will be added here when the benchmark is complete.
{: .notice--warning}

## Why it matters

Germline variant calling is the core of every genetics diagnostic lab. Validating a pipeline the way ISO 15189 expects means measuring accuracy against reference materials, broken down by genomic context, not just quoting one overall F1.

## Benchmark design

- **Truth:** GIAB v4.2.1 small-variant benchmarks for HG001–HG007 (GRCh38), with GIAB genome stratifications (low mappability, segmental duplications, homopolymers, tandem repeats, MHC, GC extremes) and the HG002 T2T-Q100 benchmark for harder regions.
- **Reads:** GIAB Illumina 2×150 PCR-free WGS. HG002 as a full genome (~30×), the other six on chr20.
- **Metrics:** SNV and indel precision, recall and F1 per sample and per caller, stratified by region type, plus runtime and cost per sample.

## Pipeline

fastp → BWA-MEM2 → MarkDuplicates and BQSR → QC (mosdepth, VerifyBamID2, somalier sex check, Ti/Tv) → GATK HaplotypeCaller **and** DeepVariant → hap.py against GIAB truth → VEP with gnomAD, ClinVar, REVEL and SpliceAI → Exomiser with HPO terms → semi-automatic ACMG/AMP evidence → clinical-style PDF report.

## Demo case

HG002 with a heterozygous *LDLR* variant spiked in silico (fictional familial hypercholesterolaemia case). The report states that the data are public and the patient details are fictional.
