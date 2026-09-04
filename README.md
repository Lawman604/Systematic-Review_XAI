# Explainable Deep Learning for ECG-Based Cardiovascular Diagnosis

This repository contains the data-analysis workflow for a systematic review of explainable deep learning (XAI) methods used in ECG-based cardiovascular diagnosis.

The analysis focuses on the included studies from the systematic review and examines the deep-learning architectures, explainability methods, evaluation strategies, clinical validation, dataset use, predictive performance, and evidence for clinical translation.

## Analysis Objectives

The analysis was designed to:

- Describe publication trends in the included studies.
- Identify the XAI methods used in ECG-based deep-learning studies.
- Summarize the distribution of deep-learning architecture families.
- Examine how XAI explanations were evaluated.
- Assess clinician validation of XAI explanations.
- Examine physiological, external, prospective, clinician-in-the-loop, and real-world validation.
- Explore relationships between XAI methods and clinician validation.
- Explore relationships between deep-learning architectures and clinician validation.
- Examine architecture-XAI method pairings.
- Summarize the ECG datasets used across studies.
- Summarize extractable predictive-performance metrics.
- Identify major evidence gaps related to clinical translation.

## Repository Contents

### `67_xai.py`

Python script containing the systematic-review analysis workflow.

### `ARTICLES21.xlsx`

Structured study-level dataset used for the systematic-review analysis.

## Analysis Workflow

The analysis is organized into six main domains.

### Domain A — Description of the Evidence Base

The analysis summarizes:

- Publication year
- XAI methods
- Deep-learning architecture families

Because a study may use more than one explainability method, XAI methods are analyzed as multi-response data.

### Domain B — Explainability Evaluation

The analysis examines the reported strategies used to evaluate XAI explanations.

Unclear reporting is retained as a separate category rather than automatically being interpreted as absence of evaluation.

### Domain C — Clinical Validation and Translation

Clinical translation is assessed using several domains, including:

- Clinician validation of XAI explanations
- Physiological validation
- External validation
- Prospective validation
- Clinician-in-the-loop evaluation
- Real-world deployment or evaluation

Results are summarized using counts, percentages, and 100% stacked bar charts.

### Domain D — Relationships Between Methods and Clinical Validation

The analysis explores:

- XAI method × clinician validation
- Architecture × clinician validation
- Architecture × XAI method

Heatmaps are used to visualize these relationships.

Where sufficient observations are available, Fisher's exact tests are used to examine associations between individual XAI methods and clinician validation.

### Domain E — Dataset and Predictive-Performance Evidence

The analysis summarizes the datasets used across the included studies.

Predictive-performance metrics are extracted from the coded performance information where possible, including:

- Accuracy
- AUC/AUROC
- F1-score
- Precision
- Recall/Sensitivity
- Specificity

Because the included studies involve heterogeneous datasets, diagnostic tasks, and modeling approaches, predictive performance is summarized descriptively rather than treated as a formal meta-analysis.

### Domain F — Evidence-Gap Analysis

The analysis estimates the proportion of studies reporting positive evidence for important clinical-translation domains.

Wilson 95% confidence intervals are calculated for these observed proportions.

These intervals are used descriptively to characterize uncertainty within the systematic-review evidence base and are not interpreted as causal population estimates.

## Outputs

The analysis automatically generates publication-ready tables and figures.

Outputs include:

- Publication-year summary
- XAI method frequencies
- Deep-learning architecture frequencies
- XAI evaluation categories
- Clinician-validation results
- Clinical-translation evidence
- XAI method × clinician-validation matrix
- Architecture × clinician-validation matrix
- Architecture × XAI method matrix
- Dataset-use frequencies
- Predictive-performance summaries
- Evidence-gap estimates with 95% confidence intervals
- Headline findings
- Analysis datasets used for auditing and reproducibility

Figures include line plots, dot plots, heatmaps, stacked bar charts, boxplots, and confidence-interval plots.

The generated tables and figures are saved in:

`ecg_xai_scientific_outputs/`

The complete output directory can also be exported as:

`ecg_xai_scientific_outputs.zip`

## Software and Python Packages

The analysis was conducted in Python using:

- pandas
- NumPy
- Matplotlib
- SciPy
- IPython

The workflow is compatible with Jupyter/Google Colab environments.

## Reproducibility

The analysis code retains unclear or incompletely reported information as separate reporting categories where appropriate.

The workflow also exports the analyzed study-level dataset and analysis tables to support transparency and reproducibility.


## Citation information for the systematic review will be added following publication.
