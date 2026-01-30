# Empirical Study on the Robustness of Local XAI Methods

## Overview
This repository contains the code used in an empirical study on the robustness of local Explainable Artificial Intelligence (XAI) methods. The study focuses on the reliability of explanations produced by widely used local explanation techniques, namely LIME and SHAP (TreeSHAP and KernelSHAP).

In particular, this work investigates robustness along two complementary dimensions: stability and similarity. Stability captures the consistency of explanations when the same instance is explained repeatedly, while similarity measures the extent to which explanations for similar inputs are themselves similar.

## Objectives
The main objectives of this study are:
- To empirically evaluate the robustness of local explanation methods across different datasets, models, and input characteristics;
- To analyze intra-method explanation stability by isolating explanation-induced variability from model stochasticity;
- To assess inter-instance explanation similarity and its relationship with local data geometry and model confidence;
- To enable comparisons across XAI methods and datasets through a normalized similarity metric.

## Main Findings
The empirical results highlight clear differences in robustness across local XAI methods:
- Deterministic methods such as TreeSHAP produce perfectly stable explanations, as expected;
- KernelSHAP exhibits high stability, with limited sensitivity to input dimensionality and prediction uncertainty;
- LIME shows substantial instability, particularly in non-linear and high-dimensional settings, reflecting known limitations of linear surrogate models;
- Inter-instance analyses reveal that explanation similarity is influenced by local data geometry, decision boundary complexity, and prediction confidence.

These findings suggest that explanation robustness cannot be assumed a priori and should be explicitly evaluated, especially in high-stakes or user-facing applications.

## Repository Structure
empirical-study-robustness-of-local-xai-methods/
- Inter-Instance Explanation Stability.ipynb
- Intra-Method Explanation Stability.ipynb
- README.md


**Intra-Method Explanation Stability.ipynb**: Contains experiments assessing explanation stability when the same input instance is explained multiple times using the same XAI method.

**Inter-Instance Explanation Stability.ipynb**: Contains experiments evaluating explanation similarity across nearby input instances, focusing on the influence of data geometry and model confidence.

## Reproducibility
The notebooks are self-contained and include all steps required to reproduce the reported experiments. Random seeds and experimental conditions are controlled whenever applicable to ensure reproducibility.
