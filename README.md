# Sentiment Analysis with Basic Text Processing

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python: 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)
[![Framework: Pandas](https://img.shields.io/badge/pandas-2.0-blue)](https://pandas.pydata.org/)
[![Framework: NLTK](https://img.shields.io/badge/nltk-3.8-blue)](https://www.nltk.org/)

A comprehensive project focused on the fundamentals of Natural Language Processing (NLP). This repository contains the final project for the **Basic Text Processing** course from Bisa AI, where raw text data from multiple sources is cleaned, processed, and prepared for sentiment analysis.

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Repository Structure](#repository-structure)
- [Methodology](#methodology)
- [Installation and Setup](#installation-and-setup)
- [Results](#results)
- [License](#license)
- [Acknowledgements](#acknowledgements)

## Project Overview

This project demonstrates a fundamental NLP pipeline using a sentiment-labelled dataset. The primary goal is to apply various text processing techniques to transform raw, unstructured text into a clean, structured format suitable for machine learning tasks. The project covers data loading, exploration, cleaning, and several core preprocessing steps.

The key text processing techniques applied are:
*   **Case Folding:** Converting all text to a uniform case (lowercase) to ensure consistency.
*   **Punctuation & Number Removal:** Eliminating characters that do not carry sentiment information.
*   **Filtering (Stopword Removal):** Removing common words (e.g., "the", "a", "is") that provide little value in sentiment prediction.
*   **Tokenizing:** Breaking down sentences into individual words or tokens.
*   **Stemming:** Reducing words to their root form to consolidate variations of a word.

## Dataset
The project utilizes the "Sentiment Labelled Sentences Data Set" from Kaggle. This dataset contains sentences sourced from three different domains:
*   **IMDb:** Movie reviews
*   **Amazon:** Product reviews
*   **Yelp:** Restaurant reviews

Each sentence is labelled with a binary sentiment score: `1` for positive and `0` for negative. The data can be found and downloaded from the following link:
[**Kaggle Dataset: Sentiment Labelled Sentences**](https://www.kaggle.com/datasets/marklvl/sentiment-labelled-sentences-data-set/data)

## Repository Structure
```
sentiment-analysis-text-processing/
├── .gitignore
├── LICENSE
├── README.md
├── requirements.txt
├── data/
│   ├── raw/
│   └── processed/
├── notebooks/
│   └── 1.0-data-preprocessing-and-eda.ipynb
└── src/
    └── utils/
```

## Methodology

1.  **Data Loading:** The three raw data files (`imdb`, `amazon`, `yelp`) are loaded into Pandas DataFrames.
2.  **Exploratory Data Analysis (EDA):** Initial analysis is performed to understand the structure, class distribution, and characteristics of the data.
3.  **Data Merging:** The three individual datasets are combined into a single, master DataFrame for unified processing.
4.  **Text Preprocessing Pipeline:** A series of sequential cleaning steps are applied to the text data as outlined in the [Project Overview](#project-overview).
5.  **Final Data Export:** The fully cleaned and processed data is saved to the `data/processed/` directory for future use.

## Installation and Setup

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

## Results
*(This section will be updated with key findings from the notebook, such as before-and-after examples of text, data distributions, and final dataset statistics.)*

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements
*   The dataset was created by Kotzias et. al. for their paper "From Group to Individual Labels using Deep Features".
*   This project was completed as part of the **Basic Text Processing** course offered by **Bisa AI**.
