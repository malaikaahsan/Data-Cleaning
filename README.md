# Data-Cleaning
A comprehensive portfolio of 5 data cleaning projects using Python and Pandas. Covers missing value imputation, data scaling/normalization, date parsing, character encoding, and fuzzy string matching on real-world datasets..
Data Cleaning & Pre-processing Portfolio
This repository contains my completed work for the Kaggle Data Cleaning course. Each folder represents a unique challenge where raw, messy data was transformed into high-quality, analysis-ready datasets.

🛠️ Tech Stack
Language: Python 3

Libraries: Pandas, NumPy, Scipy (Box-Cox), mlxtend (Min-Max Scaling), FuzzyWuzzy (String Matching)

🚀 Projects Included
1. Handling Missing Values
Dataset: San Francisco Building Permits.

Problem: Large amounts of missing data across multiple columns.

Solution: Analyzed whether data was missing because it didn't exist or wasn't recorded. Implemented both row/column dropping and automated imputation (backfilling).

2. Scaling and Normalization
Dataset: Kickstarter Projects.

Problem: Goal and pledged amounts were on wildly different scales and heavily skewed.

Solution: Applied Min-Max Scaling to unify data ranges (0-1) and Box-Cox Transformations to achieve a normal distribution for machine learning readiness.

3. Parsing Dates
Dataset: Significant Earthquakes, 1965-2016.

Problem: Date columns were stored as objects (strings) with inconsistent formats (ISO 8601 vs. MM/DD/YYYY).

Solution: Used pd.to_datetime with format inference and error coercion to unify the timeline into a single datetime64 dtype.

4. Character Encodings
Dataset: Fatal Police Shootings in the US.

Problem: Files failing to load due to encoding errors (UTF-8 vs. Windows-1252).

Solution: Identified correct encoding keys and used .decode()/.encode() methods to fix "mojibake" (corrupted text).

5. Inconsistent Data Entry
Dataset: Pakistan Intellectual Capital.

Problem: Diverse naming conventions for universities and countries (e.g., "usa" vs. "usofa").

Solution: Leveraged Fuzzy String Matching with the fuzzywuzzy library to automatically identify and unify inconsistent text entries
