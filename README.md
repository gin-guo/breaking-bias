# Breaking Bias - Evaluating LLM-Judges

## Project Overview

This project is inspired by the Kaggle competition **"LLMs - You Can't Please Them All"**, which explores the robustness of LLM-based judges in essay evaluation. The objective is to examine how adversarial inputs can create scoring discrepancies among various LLMs acting as judges. This project features a **local evaluation pipeline** utilizing open-source small LLMs from Huggingface, enabling faster experimentation and analysis.

To expedite the evaluation process, we utilized **GPUs** in the **Kaggle notebooks** to perform inference efficiently and at no cost. You can access the uploaded Kaggle notebooks here:

- [🔗 Essay Generation Notebook on Kaggle](https://www.kaggle.com/code/ginnguo/ece324-essay-generation-pipeline)
- [🔗 Evaluation Notebook on Kaggle](https://www.kaggle.com/code/ig0yss/evaluation-latest)

## Features

- **Adversarial Input Testing**: Studies how different prompt-engineered essays impact LLM scoring.
- **Local Evaluation Pipeline**: Simulates the Kaggle judging process using multiple LLMs.
- **Kaggle notebook with GPU Support**: Enables users to run model evaluations efficiently without local hardware constraints.

### **Directory Descriptions**

---

### `data/`

Contains the dataset used for essay generation and evaluation:

- `input.csv` – Official essay topics from the Kaggle competition.
- `essay_prompts.csv` – 500 randomly generated prompts.
- `generated_essays.csv` – Adversarially generated essays.

#### `data_evaluation/`

Evaluation metrics and visualizations:

- `plotted_graphs/` – Graphs from analysis.
- `data_processing.ipynb` – Code for processing raw data
- `raw_results.pdf` - Compiled raw data.

### `essay_pipeline/`

Core logic for generating essays:

- `essay-generation-pipeline.ipynb` – Pipeline with essay generation strategies.

### `eval_judges/`

Judging logic and evaluation scripts:

- `evaluation.ipynb` – Main notebook for simulating LLM judge committees.
- Uses both **persona-based** (`Phi-4` with prompt conditioning) and **model-based** committees.

### `Archive/`

Legacy or reference materials from open-source resources:

- `evaluation-metric-approx.ipynb` – Reconstructs Kaggle’s hidden evaluation metric.
- `exploring-scoring-metrics.ipynb` – Examines alternative scoring designs.
- `sample-notebook-with-judges.ipynb` – Minimal pipeline prototype.
- `Logbook for scores.xlsx` – Competition score records.

---
