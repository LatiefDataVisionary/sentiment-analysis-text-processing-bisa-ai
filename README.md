# Sentiment Analysis with Foundational Text Processing

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Python Version: 3.x](https://img.shields.io/badge/Python-3.x-brightgreen.svg)](https://www.python.org/)
[![Technologies: Pandas | NLTK | Seaborn](https://img.shields.io/badge/Technologies-Pandas%20%7C%20NLTK%20%7C%20Seaborn-ff69b4)](https://github.com/)

![Project Banner](https://user-images.githubusercontent.com/7065401/52227183-6ce80000-28a1-11e9-9154-106d87175443.png)

This repository contains the final assignment for the **Basic Text Processing** course from **Bisa AI**. It is a comprehensive demonstration of a foundational Natural Language Processing (NLP) pipeline, where raw text data from three distinct sources is meticulously cleaned, processed, and prepared for a sentiment analysis task.

## 📋 Table of Contents
- [Project Overview](#-project-overview)
- [Dataset](#-dataset)
- [Methodology](#-methodology)
- [Key Findings & Results](#-key-findings--results)
- [Installation and Setup](#-installation-and-setup)
- [Repository Structure](#-repository-structure)
- [License](#-license)
- [Acknowledgements](#-acknowledgements)

## 🚀 Project Overview

The primary goal of this project is to apply a systematic text preprocessing workflow to a sentiment-labelled dataset. This process is crucial for transforming noisy, unstructured text into a clean, standardized format, making it suitable for feature extraction and machine learning modeling.

The core text processing techniques implemented include:
*   **Case Folding:** Standardizing text to lowercase to ensure consistency.
*   **Noise Removal:** Eliminating punctuation, numbers, and special characters.
*   **Filtering (Stopword Removal):** Removing common, low-value words to focus on meaningful terms.
*   **Tokenization:** Breaking down sentences into individual words (tokens).
*   **Stemming:** Reducing words to their root form (e.g., *loved* → *love*) using the Porter Stemmer algorithm.

## 📊 Dataset

The project utilizes the **"Sentiment Labelled Sentences Data Set"** from Kaggle, which contains 2,748 sentences sourced from three distinct online platforms:
*   **IMDb.com:** Movie reviews
*   **Amazon.com:** Product reviews for mobile phones
*   **Yelp.com:** Restaurant reviews

Each sentence in the dataset is annotated with a binary sentiment label: `1` for a positive review and `0` for a negative one.

[**➡️ Download the Dataset Here**](https://www.kaggle.com/datasets/marklvl/sentiment-labelled-sentences-data-set/data)

## 🔬 Methodology

The project follows a structured NLP pipeline, implemented within a single Google Colab notebook:

1.  **Data Acquisition & Consolidation:** The three separate data files were downloaded, loaded into Pandas DataFrames, and merged into a single, unified dataset.
2.  **Exploratory Data Analysis (EDA):** A thorough analysis was conducted to understand the dataset's characteristics, including its size, structure, and the balance of sentiment classes.
3.  **Data Quality Assessment:** The dataset was checked for missing values and duplicate entries. Duplicates were identified and subsequently removed.
4.  **Sequential Text Preprocessing:** A five-step text cleaning pipeline was applied to each sentence to prepare it for analysis.
5.  **Data Export:** The final, cleaned dataset was exported to a new CSV file (`sentiment_labelled_sentences_cleaned.csv`), ready for downstream tasks.

## ✨ Key Findings & Results

### Exploratory Data Analysis
- The consolidated dataset consists of **2,748 rows** and 2 columns (`sentence`, `sentiment`).
- Initial checks found and removed **17 duplicate entries**, resulting in a final dataset of **2,731 unique sentences**.
- The sentiment classes are highly balanced, with **50.4% Positive** and **49.6% Negative** reviews, which is ideal for a classification task.

<p align="center">
  <img src="https://i.imgur.com/2U54cIu.png" alt="Sentiment Distribution" width="500">
</p>

### The Impact of Text Preprocessing

The text processing pipeline significantly transformed the raw sentences into a clean and standardized format. The following table showcases a "before-and-after" comparison for a sample sentence:

| Processing Stage       | Result                                                                     |
| ---------------------- | -------------------------------------------------------------------------- |
| **Original Sentence**  | *"Wow... Loved this place."*                                                |
| **1. Case Folding**    | *"wow... loved this place."*                                                |
| **2. Noise Removal**   | *"wow loved this place"*                                                   |
| **3. Stopword Removal**| *"wow loved place"*  *(No stopwords to remove in this example)*             |
| **4. Tokenization**    | `['wow', 'loved', 'place']`                                                |
| **5. Stemming**        | `['wow', 'love', 'place']`                                                 |

This demonstrates how the text is stripped of non-essential information and standardized, resulting in clean tokens ready for machine learning.

## 🛠️ Installation and Setup

To run this project locally, please follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/sentiment-analysis-text-processing.git
    cd sentiment-analysis-text-processing
    ```

2.  **Create a virtual environment (recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3.  **Install the required dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Launch Jupyter Notebook:**
    ```bash
    jupyter notebook
    ```
    Then, navigate to `notebooks/` and open `1.0-data-preprocessing-and-eda.ipynb`.

## 📂 Repository Structure

```
sentiment-analysis-text-processing/
├── .gitignore                # Specifies files for Git to ignore
├── LICENSE                   # Project's open-source license
├── README.md                 # This file
├── requirements.txt          # Project dependencies
├── data/
│   ├── raw/                  # Original, untouched data
│   └── processed/            # Final cleaned dataset
└── notebooks/
    └── notebook.ipynb  # The main project notebook with all steps
```

## 📜 License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## 🙏 Acknowledgements
*   The dataset was created by Kotzias et. al. for their paper "From Group to Individual Labels using Deep Features".
*   This project was completed as part of the **Basic Text Processing** course offered by **Bisa AI**.

---
