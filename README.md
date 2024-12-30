# Swahili News Classification Using XGBoost

This repository contains the implementation for building a Swahili news classification model, inspired by the [Zindi Swahili News Classification Challenge](https://zindi.africa/competitions/swahili-news-classification). The goal is to classify Swahili news articles into predefined categories using machine learning techniques.

## Why Swahili?

Swahili is widely spoken in East Africa, with millions of speakers, yet it remains underrepresented in Natural Language Processing (NLP) tools. Developing a Swahili text classification model showcases the richness of the language and contributes to bridging the gap in NLP for underrepresented languages.

## Dataset Overview

The dataset consists of Swahili news articles categorized into topics like National, International, Business, Sports, and Entertainment. The distribution of articles is imbalanced, presenting additional challenges during training.

- Categories:
  - `Kitaifa` (National)
  - `Kimataifa` (International)
  - `Biashara` (Business)
  - `Michezo` (Sports)
  - `Burudani` (Entertainment)
- Source: [Zindi Swahili News Classification Challenge](https://zindi.africa/competitions/swahili-news-classification)

## Repository Structure

- `code.ipynb`: Main Jupyter Notebook detailing the project workflow, including data preprocessing, exploratory data analysis (EDA), model training, and evaluation.
- `train.csv`: File of the training dataset (please download from Zindi, for up to date data).
- `stopwords-sw.txt`: Swahili stopwords file used during preprocessing.

## Key Steps

### 1. Data Preprocessing

- **Text Normalization:** Lowercasing, removing special characters, numbers, and extra spaces.
- **Stopwords Removal:** Utilizing a Swahili stopwords collection from [stopwords-iso/stopwords-sw](https://github.com/stopwords-iso/stopwords-sw).
- **Encoding:** Transforming text data using TF-IDF and categories using label encoding.

### 2. Model Selection and Training

We use **XGBoost**, a robust and efficient gradient boosting framework, for multi-class classification.

#### Hyperparameter Optimization
Bayesian Optimization is employed to fine-tune hyperparameters, ensuring the model achieves optimal performance.

### 3. Evaluation

The model is evaluated using metrics like F1-score, precision, and recall. Despite challenges like dataset imbalance, the final model achieved an F1-score of **0.79** (macro average).

## Results

| Metric          | Value |
|------------------|-------|
| **Final F1**     | 0.79  |
| **Best Parameters** | Optimized using Bayesian Optimization |

## Challenges Encountered

- **Language Complexity:** Tokenization and segmentation in Swahili present unique challenges.
- **Dataset Imbalance:** Required careful handling to prevent bias toward larger classes.

## Areas for Improvement

- **Balancing the Dataset:** Techniques like oversampling or generating synthetic data could improve performance.
- **Feature Selection:** Employing methods like Chi-squared tests for feature selection.
- **Exploring Alternative Models:** Trying approaches like Word2Vec or BERT for better contextual understanding.

## How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/Sabri-blm/Building-a-Text-Classification-Model-for-Swahili-News-using-XGBoost.git

