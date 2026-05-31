# DG4NLP Natural Language Processing Coursework

## Overview

This project was developed for the DG4NLP Natural Language Processing coursework using the ArXiv scientific paper dataset.

The project implements a complete NLP pipeline covering:

* Text preprocessing and cleaning
* Feature representation
* Classical machine learning classification
* Extractive summarisation
* LLM-based classification and summarisation
* Retrieval-Augmented Generation (RAG)
* Interactive Gradio-based NLP assistant interface

---

## Dataset

This project uses the ArXiv Metadata Dataset.

Dataset source:
https://www.kaggle.com/datasets/Cornell-University/arxiv

After downloading:

1. Place `arxiv-metadata-oai-snapshot.json` inside the `data/` directory.
2. Run the preprocessing notebook to generate `arxiv_processed.csv`.

The dataset files are excluded from this repository due to their large size.


**Dataset Source:**
ArXiv Scientific Papers Dataset

**Main categories used:**

* cs
* math
* physics
* q-bio
* q-fin
* stat

---

## Project Structure

```text
DG4NLP_KamakshaShekhawat/
│
├── notebooks/
│   └── DG4NLP_NLP_Project.ipynb
│
├── data/
│   ├── arxiv_processed.csv
│   └── label_mapping.json
│
├── assets/
│
├── README.md
├── requirements.txt
└── DG4NLP_Report.pdf
```

---

## How to Run

### 1. Install Required Packages

```bash
pip install -r requirements.txt
```

### 2. Configure Hugging Face API Key

The LLM classification, summarisation, title generation, and RAG components require a Hugging Face API key.

#### How to Obtain an API Key

**Step 1:** Sign in or create a Hugging Face account.

**Step 2:** Click your profile icon in the top-right corner.

**Step 3:** Navigate to **Settings → Access Tokens**.

**Step 4:** Click **Create New Token**.

**Step 5:** Select an appropriate token type (Read access is sufficient).

**Step 6:** Generate the token.

**Step 7:** Copy the generated API key.

#### Add the API Key

Paste your API key into the notebook where indicated:

```python
GROQ_API_KEY = "YOUR_KEY"
```

or set it as an environment variable:

```bash
export HF_TOKEN="YOUR_HUGGINGFACE_API_KEY"
```

### 3. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
DG4NLP_NLP_Project.ipynb
```

Run all notebook cells sequentially to reproduce the experiments and results.

---

## Features

### Classical NLP Pipeline

* TF-IDF feature extraction
* Doc2Vec feature representation
* Logistic Regression
* Multinomial Naive Bayes
* Linear SVM
* Random Forest

### Summarisation

* Extractive summarisation using TextRank

### LLM-Based Methods

* LLM paper classification
* LLM abstractive summarisation
* LLM title generation

### Retrieval-Augmented Generation (RAG)

* Retrieval of similar papers
* Context-enhanced classification
* Context-enhanced title generation

### User Interface

* Interactive Gradio-based NLP Assistant
* Paper classification
* Summary generation
* Title generation

---

## Author

**Kamaksha Shekhawat**

MSc Artificial Intelligence
Aston University
