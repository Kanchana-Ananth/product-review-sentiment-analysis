# Product Review Sentiment Analysis using RoBERTa

An NLP-based sentiment analysis project that analyzes Amazon Fine Food Reviews using a pretrained RoBERTa model and compares its performance with VADER, a traditional lexicon-based sentiment analysis approach.

## Project Overview

Customer reviews contain valuable information about customer opinions and satisfaction.

In this project, I analyze Amazon product reviews and classify them into:

- Positive
- Neutral
- Negative

The project compares two different approaches:

1. **VADER** – A lexicon-based sentiment analysis method used as a baseline.
2. **RoBERTa** – A pretrained transformer-based model used for contextual sentiment analysis.

The goal is to understand whether a modern transformer-based model can perform better than a traditional sentiment analysis approach.

## Dataset

The project uses the **Amazon Fine Food Reviews** dataset.

The dataset contains customer reviews along with information such as:

- Product ID
- User ID
- Rating (`Score`)
- Review Summary
- Review Text
- Helpfulness information
- Review date

Due to the large size of the dataset, a sample of **5,000 reviews** was used for the computationally intensive sentiment comparison.

The original dataset is not included in this repository.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- NLTK
- Scikit-learn
- PyTorch
- Hugging Face Transformers
- RoBERTa
- Google Colab

## Project Workflow

```text
Amazon Fine Food Reviews
          ↓
    Data Loading
          ↓
 Exploratory Data Analysis
          ↓
    Data Cleaning
          ↓
     NLP Processing
          ↓
 ┌─────────────────────┐
 │                     │
 VADER              RoBERTa
 │                     │
 └──────────┬──────────┘
            ↓
     Model Evaluation
            ↓
     Model Comparison
            ↓
 Sentiment Visualization
            ↓
    Custom Prediction

```
## NLP Processing

The project demonstrates basic Natural Language Processing techniques using NLTK:

- Tokenization
- Part-of-Speech (POS) tagging
- Named Entity Recognition (NER)

These techniques help transform and analyze raw review text.

## Sentiment Label Creation

The original dataset contains ratings from 1 to 5.

For evaluation, the ratings were converted into three sentiment categories:

| Rating | Sentiment |
|--------|-----------|
| 1–2 | Negative |
| 3 | Neutral |
| 4–5 | Positive |

These labels were used as reference labels for evaluating the sentiment models.

## VADER Sentiment Analysis

VADER (Valence Aware Dictionary and sEntiment Reasoner) is a lexicon-based sentiment analysis method.

It produces:

- Negative score
- Neutral score
- Positive score
- Compound score

VADER was used as the baseline because it is simple, fast, and does not require model training.

## RoBERTa Sentiment Analysis

RoBERTa is a transformer-based language model that can understand contextual relationships between words.

In this project, a pretrained RoBERTa sentiment-analysis model was used.

The model was used for inference rather than being trained from scratch.

The same 5,000-review sample was used for both VADER and RoBERTa to make the comparison consistent.

## Model Comparison

| Model | Accuracy |
|-------|----------|
| VADER | 80.34% |
| RoBERTa | 81.38% |

RoBERTa achieved a slightly higher accuracy than VADER on the evaluated sample.

The difference was approximately 1.04 percentage points.

Accuracy was analyzed together with classification metrics and confusion matrices to better understand model performance.

## Exploratory Analysis

The project also explores sentiment patterns through:

- Rating distribution
- Sentiment distribution
- Review text analysis
- Word frequency
- Positive review word clouds
- Negative review word clouds
- Review helpfulness analysis

These visualizations help identify patterns in customer feedback.

## Custom Review Prediction

The project includes an interactive section where a new customer review can be entered.

The review is analyzed using both:

- VADER
- RoBERTa

This allows the predictions of the two approaches to be compared on new review text.

## Repository Contents

```text
product-review-sentiment-analysis/
│
├── Sentiment_Analysis_Project.ipynb
└── README.md
