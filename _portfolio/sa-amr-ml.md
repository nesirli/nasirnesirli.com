---
title: "Erythromycin Resistance in S. aureus: DNABERT-2 vs XGBoost"
excerpt: "Predicting erythromycin resistance in Staphylococcus aureus with a fine-tuned DNA language model compared with XGBoost on gene features."
group: "Microbial Genomics"
order: 2
status: "In progress"
stack: [Python, uv, PyTorch, Hugging Face Transformers, DNABERT-2, LoRA, XGBoost, AMRFinderPlus, NCBI Datasets]
---

**Repository:** [nesirli/sa-amr-ml](https://github.com/nesirli/sa-amr-ml) · **Status:** in progress. Results will be added here when the comparison is complete.
{: .notice--warning}

## The question

Do DNA language models earn their compute cost for antimicrobial resistance prediction, or does a gradient-boosted model on known resistance genes do just as well?

## Approach

- **Data:** *S. aureus* genomes from NCBI Datasets with erythromycin susceptibility phenotypes.
- **Baseline:** XGBoost on gene presence/absence features from AMRFinderPlus.
- **Deep learning:** DNABERT-2 fine-tuned with LoRA on sequence input.
- **Comparison:** the same split and the same metrics for both models, plus training and inference cost.
