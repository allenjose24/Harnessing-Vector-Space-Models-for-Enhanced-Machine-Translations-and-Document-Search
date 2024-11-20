
# Harnessing Vector Space Models for Enhanced Machine Translations and Document Search.

This project focuses on integrating **Vector Space Models** (VSM) with **Machine Translation** (MT) models for enhancing document search and translation quality. It involves the use of **MarianMT** for translation, **GloVe** for word embeddings, and **cosine similarity** for document ranking.

## Introduction

This project aims to analyze and evaluate translation results from **MarianMT** and **Google Translate**. It calculates back-translation similarity scores using **cosine similarity** between the original and back-translated sentences, and compares the performance of the two translation models.

The project also uses GloVe word embeddings to calculate the similarity between translated sentences and documents from the Reuters dataset.

## Installation

To get started, you need to install the required libraries:

```bash
pip install googletrans==4.0.0-rc1
pip install plotly autocorrect
pip install gensim nltk
```

These commands will install the required libraries like Google Translate API, Plotly, Gensim (for pre-trained GloVe embeddings), and Hugging Face Transformers for MarianMT.

### Requirements
This project relies on the following libraries: 
* googletrans: For translating text using Google Translate.
* Plotly: For visualizing translation similarity scores.
* gensim: For downloading and using pre-trained word embeddings (GloVe).
* NLTK: For tokenization and text processing, and access to the Reuters dataset.
* transformers: For using MarianMT for translation.
* torch: For running the MarianMT model.
* autocorrect: For correcting spelling mistakes in the input sentences.

### Key Features
* Multi-Language Support: Translation between various languages supported by MarianMT and Google Translate.
* Back-Translation: Translates a sentence to a target language and then back to the source language for evaluation.
* Cosine Similarity Calculation: Compares the original and back-translated sentences using cosine similarity based on GloVe embeddings.
* Visualization: Bar charts for comparing the similarity scores of MarianMT and Google Translate, as well as document similarity scores using Plotly.
* Document Evaluation: Similarity evaluation with English documents from the Reuters dataset.
* Spell Checking: Automatically detects and corrects spelling mistakes in user input using the autocorrect library.
* Data Export: Saves the similarity scores to an Excel file for further analysis.

### Usage
#### 1. Language Translation and Evaluation:

The user is prompted to input a source language, target language, and a query sentence.
The sentence is translated using both MarianMT and Google Translate.
The back-translated sentence is compared to the original, and a cosine similarity score is calculated.

#### 2. Back-Translation and Similarity Scores:

The cosine similarity between the original sentence and the back-translated sentence is computed for both MarianMT and Google Translate.
The back-translation similarity scores are visualized using Plotly.
#### 3. Document Evaluation:

The similarity between the translated query and a set of English documents from the Reuters dataset is evaluated using cosine similarity.
#### 4. Visualization:

Similarity scores are plotted for easy comparison of MarianMT and Google Translate performance.
#### 5. Export to Excel:

The cosine similarity scores between the translated query and English documents are saved to an Excel file for further analysis.

### Example Flow

```bash
Enter the source language code (e.g., 'en' for English): en
Enter the target language code (e.g., 'es' for Spanish): es
Enter the sentence to translate: "Machine Translation is revolutionizing the way we communicate."
```

#### The program will output:

The translated sentence using MarianMT and Google Translate.
The back-translated sentence from both systems.
Cosine similarity scores between the original and back-translated sentences.
A comparison plot of the similarity scores.
A file **(cosine_similarity_scores.xlsx)** with all similarity scores.

## Results
#### The program will output:

* Translated sentences using both MarianMT and Google Translate.
* Back-translated sentences (from target language to source language).
* Similarity scores (cosine similarity) of the original and  back-translated sentences.
* A bar chart comparing the back-translation similarity scores for MarianMT and Google Translate.
* Document similarity scores for the translated queries compared to English documents from the Reuters dataset.
* A saved Excel file (cosine_similarity_scores.xlsx) containing the similarity scores.

## Exporting Data
The cosine similarity results for the translated queries against the Reuters dataset documents are saved in an Excel file:

```bash
cosine_similarity_scores.xlsx
```
This file contains the similarity scores for both MarianMT and Google Translate for all evaluated documents.

## Acknowledgments
1. Google Translate API: For providing a robust translation system.
2. MarianMT: A high-quality, pre-trained neural machine translation model from the Hugging Face Transformers library.
3. NLTK: For providing the Reuters dataset and text processing utilities.
4. Gensim: For pre-trained GloVe word embeddings.
5. Plotly: For visualizing similarity scores.
Autocorrect: For correcting spelling mistakes in the input queries.
