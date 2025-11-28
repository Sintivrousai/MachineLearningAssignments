This repository contains three Machine Learning assignments completed for the university course **Machine Learning**.  
Each assignment focuses on a different ML topic, including supervised learning, unsupervised learning, optimization, and model evaluation.

# Assignment 1 — Exploring AirBnB in Europe

This assignment analyzes AirBnB data from *InsideAirBnB* for 13 major European cities (e.g., Amsterdam, Athens, Barcelona, Berlin, London, Paris).  
We use the latest available 12-month period for each city.

## Tasks
- **Listings per city:** compute and visualize the number of listings.  
- **Density analysis:** listings per 1,000 inhabitants (using external population data).  
- **Activity & income:** estimate bookings and income per listing using review counts.  
- **Cross-check:** compare estimated totals with publicly available tourism statistics.  
- **Visualisation:** recreate InsideAirBnB charts and make them interactive (city dropdown).

## Methods
- Data loading & cleaning (pandas)  
- Aggregation and city-level metrics  
- Plotting (matplotlib / seaborn)  
- Interactive charts (Altair or Plotly)

## Data
InsideAirBnB datasets: `listings.csv`, `reviews.csv` (latest 12 months).

## Technologies
Python · Pandas · NumPy · Matplotlib/Seaborn · Altair/Plotly

# Assignment 2 — Social Media Sanctions & Misinformation Analysis

This project reproduces key parts of the analysis from *Mosleh et al. (Nature, 2024)*, examining whether social media suspensions are politically biased or driven by differences in misinformation sharing.

Using the original dataset from the study, the assignment explores political ideology, misinformation behaviour, and account suspensions through statistical analysis and modelling.

## Main Objectives
- Compare suspension rates between conservative (#Trump2020) and liberal (#VoteBidenHarris2020) users.  
- Analyze distributions of low-quality news sharing using fact-checker and crowdsourced ratings.  
- Quantify differences in misinformation sharing with **t-tests**, **Cohen’s d**, and **Hedges’ g**.  
- Study correlations between political ideology and misinformation behaviour.  
- Predict suspension using **single-variable probit models** and evaluate performance with **AUC + bootstrap CIs**.  
- Build **multi-variable probit and logit regression models**, including PCA-derived features for misinformation, political ideology, harmful language, and valence.  
- Apply **Bonferroni** and **Holm–Bonferroni** corrections for multiple hypothesis testing.

## Techniques Used
- Statistical hypothesis testing (χ² tests, t-tests, effect size metrics)  
- Probit & logit regression modelling  
- Bootstrap resampling  
- Correlation analysis & heatmaps  
- Feature engineering (log transforms, winsorizing, PCA)  
- Data visualization (matplotlib / seaborn)

## Technologies
Python · Pandas · NumPy · SciPy · Scikit-learn · Statsmodels · Matplotlib · Seaborn

---
# Assignment 3 — SemEval 2025 Task 9: Food Hazard Detection

This project implements solutions for **SemEval 2025 Task 9: The Food Hazard Detection Challenge**, focusing on detecting food-related hazards from text. The assignment covers both subtasks and includes full experimentation, validation, and generation of the required `submission.csv`.

## Task Overview

### **ST1 — Text Classification**
Predict:
- the **hazard type**
- the **product category**

### **ST2 — Vector Detection**
Predict:
- the exact **hazard**
- the exact **product**  
as a multi-label problem.

## Approach
The notebook explores multiple NLP and ML methods, leveraging both local experimentation and AWS cloud services for training and evaluation.  
Key components:

- Transformer-based models (BERT-based architectures)
- Multi-label classification for ST2
- Preprocessing, tokenization, and embeddings
- Hyperparameter tuning and model comparison
- Model evaluation using the official SemEval F1 score

## AWS Integration
The project also utilizes **AWS cloud services** for scalable training and experimentation, including:

- **Amazon SageMaker** for running and training models
- **S3** for dataset storage and model outputs
- **EC2 compute instances** for accelerated experimentation

## Evaluation
All models are evaluated using the **SemEval official F1 metric**, on:
- validation data  
- optional testing data, when available

A final `submission.csv` is generated following the required competition format.

## Technologies Used
Python · PyTorch · HuggingFace Transformers · Scikit-learn · Pandas · NumPy  
AWS SageMaker · Amazon S3 · EC2

