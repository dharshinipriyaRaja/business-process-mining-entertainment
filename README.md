# Application of Business Process Mining in Entertainment Content Production

## Overview

This project investigates the application of Business Process Mining, Machine Learning and Explainable AI (XAI) to analyse and predict delays in entertainment content production.

The project focuses on short-film production workflows and uses a synthetic event log representing production activities from idea generation through to release. Process Mining techniques are used to discover and analyse workflow patterns, while Machine Learning models are developed to estimate remaining process time and predict potential delays. Explainable AI is then applied to understand the factors contributing to model predictions.

## Project Objectives

The main objectives of the project were to:

- Analyse entertainment content production workflows using Process Mining.
- Discover common process paths and workflow variants.
- Identify bottlenecks and rework patterns within the production process.
- Estimate the remaining time required to complete a production case.
- Predict whether a production case is likely to experience delays.
- Apply Explainable AI to improve the interpretability of machine learning predictions.

## Dataset

A synthetic event log was created to represent short-film production processes because a suitable publicly available event log for this specific domain was not identified.

The dataset contains multiple production cases and records activities such as:

- Idea Generation
- Script Writing
- Planning
- Shooting
- Editing
- Review
- Release

Each event contains process and contextual information used for Process Mining and Machine Learning analysis.

## Methodology

### 1. Process Mining

Process Mining techniques were applied using PM4Py to analyse the event log and understand the underlying production workflow.

The analysis included:

- Directly-Follows Graph (DFG) analysis
- Process discovery
- Workflow variant analysis
- Bottleneck identification
- Rework analysis
- Token replay and process conformance analysis

Multiple process discovery approaches were explored, including:

- Alpha Miner
- Inductive Miner
- Heuristics Miner

### 2. Machine Learning

Machine Learning models were developed for two predictive tasks:

#### Remaining Time Estimation

Regression models were used to estimate the remaining time required to complete a production case.

The models were evaluated using:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² score

#### Delay Prediction

Classification models were used to predict whether a production case was likely to be delayed.

Classification performance was evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC

Group-based data splitting was used to reduce the risk of information leakage between events belonging to the same production case.

### 3. Explainable AI

SHAP (SHapley Additive exPlanations) was used to investigate the contribution of input features to machine learning predictions.

This helped provide interpretable insights into which process characteristics were most influential in the model's predictions.

## Key Findings

The Process Mining analysis identified a predominantly sequential production workflow with variations caused by rework.

Editing and Review were particularly important stages in identifying repeated process cycles, while Shooting showed a high average activity duration.

The Machine Learning analysis demonstrated that process-related features such as cumulative time and activity position provided useful information for estimating remaining production time and predicting delays.

SHAP analysis was used to further investigate feature contributions and improve the interpretability of the predictive models.

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- PM4Py
- SHAP
- Jupyter Notebook
- SQL
- Matplotlib
- Graphviz

## Project Structure

The repository contains the notebooks, source code, figures, results and supporting files used during the project.

## Academic Context

This project was completed as part of an MSc Artificial Intelligence dissertation at Aston University.

## Author

**Dharshini Priya Raja**

MSc Artificial Intelligence Graduate  
Aston University, Birmingham, UK
