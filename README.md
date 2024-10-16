Here’s a sample README file for your GitHub repository based on the information from your research paper on hate speech detection in Telugu-English code-mixed text:

---

# IIITDWD_SVC-DravidianLangTech-2024

## Breaking Language Barriers: Hate Speech Detection in Telugu-English Code-Mixed Text

This repository contains the code and resources used in our submission to the **DravidianLangTech@EACL-2024** shared task for **Hate Speech Detection** in Telugu-English code-mixed text. Our team, **IIITDWD_SVC**, participated in the competition, and our BERT-based model achieved the **14th rank** with a macro F1 score of **0.6565**.

---

## Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Models Used](#models-used)
- [Results](#results)
- [Installation](#installation)
- [Usage](#usage)
- [Acknowledgements](#acknowledgements)

---

## Overview

Social media platforms are commonly used for communication, but they are also exploited to spread hate and offensive content. The **DravidianLangTech@EACL-2024** task was designed to detect hate speech in Telugu-English (Tenglish) code-mixed text, focusing on classifying social media comments into hate or non-hate categories.

Our approach involved transliteration, translation, and tokenization processes, followed by training on three models:
- **BERT**
- **Hate-BERT**
- **XLM-RoBERTa**

---

## Dataset

The dataset used in this task was provided by the organizers of the **DravidianLangTech@EACL-2024** shared task. It consists of comments collected from YouTube.

### Data Distribution

| Set    | Hate  | Non-Hate | Total  |
|--------|-------|----------|--------|
| Train  | 1939  | 2061     | 4000   |
| Test   | 250   | 250      | 500    |

---

## Methodology

We followed a multi-step approach to preprocess the data and build the classification models:

1. **Transliteration**: Converted Telugu content written in English script to the Telugu script using the IndicXlit model.
2. **Translation**: Translated Telugu text to English using the IndicTrans2 model for compatibility with pre-trained models.
3. **Tokenization**: Tokenized the translated text using the Hugging Face library, with specific tokenizers for each model.

---

## Models Used

### 1. **BERT**
- We utilized the pre-trained **BERT-Base Uncased** model for embedding extraction.

### 2. **Hate-BERT**
- **Hate-BERT**, trained on banned Reddit posts, was used for detecting abusive language.

### 3. **XLM-RoBERTa**
- A cross-lingual RoBERTa model trained on 100 different languages, including Telugu and English.

![Methodology Flow Diagram](path_to_methodology_image)

---

## Results

Our model's performance was evaluated using macro F1 score, and we ranked **14th** in the shared task. Below is a summary of our results compared to other top teams:

| Team       | F1 Score | Rank |
|------------|-----------|------|
| Sandalphon | 0.7711    | 1    |
| IIITDWD_SVC | 0.6565   | 14   |

---

## Installation

To use the code in this repository, follow these steps:

1. Clone this repository:
   ```bash
   git clone https://github.com/Chava-Sai/IIITDWD_SVC-DravidianLangTech-2024.git
   ```
2. Install the necessary packages:
   ```bash
   pip install -r requirements.txt
   ```

---

## Usage

To run the hate speech detection models:

1. **Preprocess the data**:
   ```bash
   python preprocess.py --data_path path_to_data
   ```

2. **Train the models**:
   ```bash
   python train.py --model bert
   ```

3. **Evaluate the model**:
   ```bash
   python evaluate.py --model bert
   ```

---

## Acknowledgements

We would like to thank the organizers of **DravidianLangTech@EACL-2024** for providing the dataset and the opportunity to participate in this shared task. We are also grateful to the Hugging Face community for making available pre-trained models used in this project.

--- 
