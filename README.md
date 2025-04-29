# Neural Project (Classification of Correct and Incorrect Responses)
## By: Paul Wanczuk & Udaya Sankar Nadendla
### Problem Statement

Neuronal decoding bridges neural signals to cognitive or behavioral outcomes, playing a vital role in brain-computer interfaces (BCIs), which significantly enhance quality of life for individuals with cognitive or motor impairments [1]. Recent research underscores the potential of decoding neural activity from the medial temporal lobe (MTL)—including the hippocampus and entorhinal cortex—in visual working memory tasks. However, traditional Support Vector Machines (SVM) yield limited decoding accuracy (~55%) [2]. 

To address this, this project aims to significantly improve decoding accuracy using optimized Gradient Boosting models, leveraging their ability to manage nonlinear relationships, noisy data, and provide interpretable feature importance [3].

The study will:
- Examine three neuronal data grouping strategies
- Optimize the Gradient Boosting approach
- Statistically validate performance gains over SVMs

By the end of this project, we aim to accomplish two main goals:
1. **Achieve a classification accuracy of at least 75%** by the Gradient Boosting Model for all brain regions (Hippocampus, Entorhinal cortex, and Amygdala) with respect to participant performance during memory tasks.
2. **Identify which phase of the task (Encoding, Maintenance, Test)** neural firing rate is most deterministic of participant performance.
# Data Files Description

The `.csv` files provided in this repository are **preprocessed datasets** that are ready for direct use with the decoding models described in this project. Each file contains organized neuronal data corresponding to specific brain regions, trial types, and task phases.

## File Naming Convention

Each file name encodes information about the dataset it contains, following this structure:

- **Brain Region**:
  - `Hippo` — Hippocampal Head
  - `PH` — Hippocampal Body
  - `Amyg` — Amygdala
  - `ECL` — Entorhinal Cortex

- **Trial Type**:
  - `4` — 4-square trial
  - `6` — 6-square trial

- **Task Phase**:
  - `m` — Memorization (Encoding)
  - `r` — Retention (Maintenance)
  - `p` — Probe (Test)

## Example

A file named: Patient1_Amyg_4m.csv


---
# Findings

## Aim 1: Classification Accuracy

With respect to **Aim 1**, we successfully achieved a classification accuracy of at least 75% using the Gradient Boosting Model for the following brain regions:
- **Hippocampal Head**: 83% accuracy
- **Hippocampal Body**: 75% accuracy
- **Amygdala**: 75% accuracy

However, we did not achieve the target accuracy for the **Entorhinal Cortex**, which reached a maximum accuracy of only **67%**.

## Aim 2: Task Phase Determinism

With respect to **Aim 2**, we were unable to differentiate participant performance based on task phases. The average classification accuracies for each phase were:
- **Encoding**: 55%
- **Maintenance**: 58%
- **Test**: 56%

These variations were minimal and thus inconclusive regarding which phase was most deterministic of participant performance.

## Additional Observations

The results highlight the critical importance of structured data organization as described in the Methods section. Proper control for factors such as **Trial Difficulty**, **Brain Region**, and **Trial Time** was essential, as these parameters introduced substantial variation in neuronal firing unrelated to the memory errors targeted for classification. Notably, there were extreme differences in model performance across these factors, emphasizing the need for careful experimental design and data partitioning.

# Dataset

The neural recording dataset used in this project is available at:  
[DANDI Archive Dataset 000575](https://dandiarchive.org/dandiset/000575/0.231010.1811)

---

# References

[1] Lebedev, M. A., & Nicolelis, M. A. (2006). Brain–machine interfaces: past, present and future. *Trends in Neurosciences*, 29(9), 536-546.

[2] Kaminski, J., et al. (2017). Persistently active neurons in human medial frontal and medial temporal lobe support working memory. *Nature Neuroscience*, 20(4), 590–595.

[3] Friedman, J. H. (2001). Greedy function approximation: a gradient boosting machine. *Annals of Statistics*, 1189–1232.

