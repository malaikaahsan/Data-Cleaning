# 🧹 Data Cleaning & Preprocessing Portfolio

[![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)](https://www.python.org/)
[![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)](https://numpy.org/)
[![Kaggle](https://img.shields.io/badge/Kaggle-%2320BEFF.svg?style=for-the-badge&logo=kaggle&logoColor=white)](https://www.kaggle.com/)

A portfolio of **5 hands-on data cleaning projects** based on the Kaggle Data Cleaning course. Each project tackles a real-world messy dataset using Python and Pandas, covering the most critical preprocessing techniques needed before any data analysis or machine learning task.

---

## 📂 Projects Overview

| # | Project | Dataset | Technique |
|---|---|---|---|
| 1 | [Handling Missing Values](#1-handling-missing-values) | SF Building Permits | Imputation & Dropping |
| 2 | [Scaling & Normalization](#2-scaling-and-normalization) | Kickstarter Projects | Min-Max, Box-Cox |
| 3 | [Parsing Dates](#3-parsing-dates) | Earthquakes 1965–2016 | datetime64, pd.to_datetime |
| 4 | [Character Encodings](#4-character-encodings) | Fatal Police Shootings (US) | UTF-8, Windows-1252 |
| 5 | [Inconsistent Data Entry](#5-inconsistent-data-entry) | Pakistan Intellectual Capital | Fuzzy String Matching |

---

## 📁 Folder Structure

```
Data-Cleaning/
│
├── Handling-missing-values/
├── Scaling-and-Normalization/
├── Parsing-data/
├── Character-encoding/
└── Incosistent-data-entry/
```

---

## 🔍 Project Details

### 1. Handling Missing Values
**Dataset:** San Francisco Building Permits

**Problem:** Large portions of data were missing across multiple columns. Simply dropping everything would lose too much information.

**Solution:**
- Analyzed *why* data was missing — whether values were intentionally absent or just not recorded
- Applied both **row/column dropping** for heavily incomplete data
- Used **backfilling (imputation)** to automatically fill gaps where appropriate

**Key skill:** Understanding context before blindly removing or filling data

---

### 2. Scaling and Normalization
**Dataset:** Kickstarter Projects

**Problem:** `goal` and `pledged` columns had wildly different ranges and were heavily right-skewed — unsuitable for ML algorithms that are sensitive to feature scale.

**Solution:**
- Applied **Min-Max Scaling** (via `mlxtend`) to compress values into a [0, 1] range
- Used **Box-Cox Transformation** (via `scipy`) to normalize skewed distributions into a bell curve shape

**Key skill:** Preparing numerical features for machine learning models

---

### 3. Parsing Dates
**Dataset:** Significant Earthquakes, 1965–2016

**Problem:** Date columns were stored as plain strings with mixed formats — some in ISO 8601, others in MM/DD/YYYY — making time-based analysis impossible.

**Solution:**
- Used `pd.to_datetime()` with format inference
- Used `errors='coerce'` to handle unparseable values gracefully
- Unified all dates into a consistent `datetime64` dtype

**Key skill:** Converting messy date strings into proper time series data

---

### 4. Character Encodings
**Dataset:** Fatal Police Shootings in the US

**Problem:** Files were failing to load due to encoding mismatches (UTF-8 vs. Windows-1252), causing corrupted text known as **mojibake** (e.g., `Ã©` instead of `é`).

**Solution:**
- Detected the correct encoding using `chardet`
- Used Python's `.encode()` / `.decode()` methods to fix corrupted text
- Successfully loaded and cleaned the dataset with the right encoding

**Key skill:** Diagnosing and resolving character encoding issues in real-world data files

---

### 5. Inconsistent Data Entry
**Dataset:** Pakistan Intellectual Capital

**Problem:** University and country names were entered inconsistently (e.g., `"usa"`, `"usofa"`, `"U.S.A"` all meaning the same thing), making grouping and analysis unreliable.

**Solution:**
- Used **Fuzzy String Matching** via the `fuzzywuzzy` library
- Automatically identified similar strings above a similarity threshold
- Unified inconsistent entries into a clean, standardized format

**Key skill:** Detecting and fixing human data entry errors at scale

---

## 🛠️ Tech Stack

- **Language:** Python 3
- **Environment:** Jupyter Notebook / Kaggle Notebooks
- **Libraries:**
  - `pandas` — Core data manipulation
  - `numpy` — Numerical operations
  - `scipy` — Box-Cox transformation
  - `mlxtend` — Min-Max scaling
  - `fuzzywuzzy` — Fuzzy string matching
  - `chardet` — Encoding detection

---

## 🚀 How to Run

1. Clone the repository:
```bash
git clone https://github.com/malaikaahsan/Data-Cleaning.git
cd Data-Cleaning
```

2. Install dependencies:
```bash
pip install pandas numpy scipy mlxtend fuzzywuzzy python-levenshtein chardet
```

3. Open any notebook in Jupyter:
```bash
jupyter notebook
```

> **Note:** These projects were originally developed on Kaggle. Dataset paths may need updating if running locally. Datasets are available on [Kaggle's Data Cleaning course](https://www.kaggle.com/learn/data-cleaning).

---

## 💡 What I Learned

- Data is almost never clean in the real world — preprocessing is 80% of the work
- Different types of messiness require completely different solutions
- Understanding *why* data is missing matters as much as *how* to handle it
- Encoding issues and inconsistent text are among the most common problems in real datasets

---

## 👩‍💻 Author

**Malaika Ahsan**
BS Computer Science — PUCIT, Lahore
[GitHub](https://github.com/malaikaahsan)
