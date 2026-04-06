# sEEG forced two-choice task classification
This repository contains the code and findings of a project carried out during the NeuralStorm Workshop in 2023. On the final day of the workshop, a competition was held to classify choices made in a sEEG Forced Two-Choice Task. Teaming up with Wenqing from CCLAB, we secured a tie for the first place in the competition!

## Overview
We primarily focused on utilizing summary statistics derived from several frequency bands to predict the choices made. Among the different classification algorithms evaluated — Logistic Regression, SVM, Gaussian Naive Bayes, K-Nearest Neighbors, Decision Tree, and Linear Discriminant Analysis — **LDA yielded the best results**.

<p align="center">
  <img src="https://github.com/orhansoyuhos/NeuralStorm-Workshop-2023/assets/44211738/8b07952d-abe4-4de2-9f44-86a8eb3406cd" width="70%">
</p>

## Dataset
The dataset comprises intracranial electroencephalography (iEEG) recordings collected during a sEEG Forced Two-Choice Task. The dataset is available on OpenNeuro: [Dataset Link](https://openneuro.org/datasets/ds004473/versions/1.0.2)

## Competition
The competition was hosted on Kaggle. More details can be found here: [Competition Link](https://www.kaggle.com/competitions/neural-storm-mini-project-day-4-5/)

## Preprocessing
The data preprocessing involved normalizing the signal data, extracting power from 6 frequency bands, and deriving summary statistics — resulting in **11 features** per trial:

**Frequency band powers:**
| Band | Range |
|------|-------|
| Delta | 1–4 Hz |
| Theta | 4–8 Hz |
| Alpha | 8–12 Hz |
| Beta | 12–30 Hz |
| Low Gamma | 30–90 Hz |
| High Gamma | 90–120 Hz |

**Summary statistics:** minimum, maximum, mean, variance, standard deviation
