# Breaking Bias - Evaluating LLM-Judges

## Project Overview

This project is inspired by the Kaggle competition **"LLMs - You Can't Please Them All"**, which explores the robustness of LLM-based judges in essay evaluation. The objective is to examine how adversarial inputs can create scoring discrepancies among various LLMs acting as judges. This project features a **local evaluation pipeline** utilizing open-source small LLMs from Huggingface, enabling faster experimentation and analysis.

To expedite the evaluation process, we utilized **GPUs** in the **Kaggle notebooks** to perform inference efficiently and at no cost. You can access the uploaded Kaggle notebook here:  
[🔗 Evaluation Notebook on Kaggle](https://www.kaggle.com/code/ig0yss/evaluation)

## Features

- **Adversarial Input Testing**: Studies how different prompt-engineered essays impact LLM scoring.
- **Local Evaluation Pipeline**: Simulates the Kaggle judging process using multiple LLMs.
- **Kaggle notebook with GPU Support**: Enables users to run model evaluations efficiently without local hardware constraints.

---

### **Folder Descriptions**

#### `data_generation` : Contains **input.csv**, which provides the dataset of essay topics used for generating adversarial essays.

#### `essay_pipeline/` : Houses the **core implementation** of the essay generation framework.

- `old_versions`: Contains previous iterations of the pipeline.
- `ece324-highest-score.ipynb`: Best performing notebook from the competition.
- `ece324-word-embeddings.ipynb`: Tests embedding-based approaches for essay generation.

#### `eval_judges/` : Contains **the main evaluation notebooks** for scoring essays using LLM judges.

- **`Open_source/`**: Includes notebooks adapted from publicly available Kaggle discussions.
  - `evaluation-metric-approx.ipynb`: Implements an approximation of the Kaggle evaluation metric.
  - `exploring-scoring-metrics.ipynb`: Tests various scoring approaches for judge agreement.
  - `sample-notebook-with-judges.ipynb`: Provides a simple example of LLM-based judging.
- `evaluation.ipynb`: **Main evaluation notebook** that attempts to replicate the LLM-judging process.
- `essay_prompts.csv`: Contains 500 predefined topics for essay generation.
- `Logbook for scores.xlsx`: Recorded scores from the competition.

---
