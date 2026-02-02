# 🏛️ Brazilian Empire Senate Discourses Analysis (1826-1888)

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![NLP](https://img.shields.io/badge/NLP-Spacy%2FPolars-green)
![Status](https://img.shields.io/badge/Status-Research%20in%20Progress-orange)

## 1. Overview
This repository hosts the source code and datasets for an **Undergraduate Research Project** focused on the quantitative analysis of political discourse in the Brazilian Empire.

By applying **Natural Language Processing (NLP)** techniques to over **80,000 parliamentary speeches**, this project aims to measure political polarization, identify thematic shifts, and structure unstructured historical text into a machine-learning-ready format.

## 2. The Dataset
The core of this repository is the curated dataset located in the `data/` folder. Due to the high volume of text, the data is stored in **Parquet format** to ensure efficiency and type preservation.

### 3. File: `discursos_senado_imperio_1826_1888.parquet` (~67MB)
This unified dataset contains cleaned and processed speeches from 1826 to 1888.

| Column | Description |
| :--- | :--- |
| `Ano` | Year of the speech session. |
| `Discurso_Bruto` | Raw text extracted via OCR/Scraping from the Senate Annals. |
| `Discurso` | **Processed text**: Lowercased, stopwords removed, and lemmatized for NLP tasks. |
| `Orador` | Normalized name of the Senator. |
| `Partido` | Political Affiliation (e.g., *Conservador*, *Liberal*). |
| `Província` | The province represented by the Senator. |
| `Legislatura` | The specific legislative period. |

> **Note:** The `Discurso` column is optimized for vectorization techniques like TF-IDF, Word2Vec, or BERT.

## 4. How to Load the Data
To maximize performance and avoid memory issues, the data is compressed using GZIP. You can load it directly with Pandas:

```python
import pandas as pd

# Efficiently load the compressed parquet file
df = pd.read_parquet('data/discursos_senado_imperio_1826_1888.parquet')

# Check the first rows
print(df.head())
