[![DOI](https://zenodo.org/badge/1206405908.svg)](https://doi.org/10.5281/zenodo.19489709)

# Practical Guide to Large Language Models for Detecting Information in Behavioral Health Notes
## Synthetic dataset

This repository contains synthetic clinical note datasets used in the paper:

**“Practical Guide to Large Language Models for Detecting Information in Behavioral Health Notes.”**

## Overview

This dataset was created to support reproducible evaluation of large language model (LLM) workflows for clinical information extraction from unstructured text.

The repository includes synthetic clinical notes for two tasks:

- **Self-Injurious Thoughts and Behaviors (SITB) Detection**
- **Antipsychotic Medication Non-Adherence Detection**

Each dataset is paired with ground-truth labels and is designed for controlled benchmarking of prompt-based classification pipelines.

---

## Dataset Design

All notes were synthetically generated using structured specification sheets that define:

- Clinical content requirements  
- Narrative style and variability  
- Label-conditional constraints  

Ground-truth labels were assigned by construction during generation and are stored separately from note text to simulate real-world evaluation workflows.

---

## Intended Use

This dataset is intended for:

- Benchmarking LLM-based clinical NLP pipelines  
- Prompt engineering and evaluation  
- Testing structured outputs (e.g., JSON schema constraints)  
- Educational and research purposes  

---

## Important Limitations

- These are synthetic clinical notes not real patient data  
- They do not contain protected health information (PHI  
- Performance on this dataset does not reflect real-world clinical performance  
- The dataset is designed for controlled workflow validation not deployment  

---

## Reproducibility

This repository accompanies the tutorial paper and is designed to support:

- Reproducible evaluation  
- Transparent prompt development  
- Standardized benchmarking  

All datasets are formatted for straightforward integration into LLM pipelines.

---

## Example Usage

```python
import pandas as pd
notes = pd.read_json("Pediatric_SITB/child_1.json")
print(notes.head())
