# CORD-19 Sample Data Explorer

[![Python](https://img.shields.io/badge/Python-3.10-blue)](https://www.python.org/)
[![Streamlit](https://img.shields.io/badge/Streamlit-App-green)](https://streamlit.io/)
[![GitHub](https://img.shields.io/badge/GitHub-Repo-black)](https://github.com/Robibiruk/CORD19_Sample)

[Live Demo on Streamlit](https://cord19-sample-analysis.streamlit.app/)

---

## Table of Contents
1. [Overview](#overview)
2. [Features](#features)
3. [Skills Demonstrated](#skills-demonstrated)
4. [Dataset](#dataset)
5. [Requirements](#requirements)
6. [How to Run Locally](#how-to-run-locally)
7. [Live Deployment](#live-deployment)
8. [Project Workflow](#project-workflow)
9. [Learning Outcomes](#learning-outcomes)
10. [Screenshots](#screenshots)
11. [Author](#author)
12. [License](#license)

---

## Overview

This project is a **comprehensive analysis of COVID-19 research papers** using the CORD-19 dataset. The goal was to explore and visualize patterns in the dataset and build an interactive **Streamlit web application** to make the insights accessible in a dynamic and user-friendly way.  

It demonstrates **data cleaning, feature engineering, visualization, and machine learning classification** skills in Python.

---

## Features

### 🔳 Data Loading & Inspection
- Load the sample CORD-19 metadata CSV file using `pandas`.
- Explore the dataset shape, column types, and missing values.
- Preview the first few rows of data directly in the web app.

### 🔳 Feature Engineering
- Handle missing data in numeric and categorical columns.
- Convert publication dates to datetime and extract `publish_year`.
- Create new features:
  - `abstract_word_count`
  - `title_word_count`
  - `num_authors`
- Reduce journal categories to top publishers for better analysis.

### 🔳 Visualizations
- **Publications Over Time:** Interactive bar chart showing number of papers per year since 1990.
- **Top Journals:** Horizontal bar chart of the 10 most prolific journals publishing COVID-19 papers.
- **Word Cloud of Titles:** Most frequent words in paper titles to highlight research trends.
- **Distribution by Source:** Cleaned bar chart showing top sources of papers plus an 'Other' category.

### 🔳 Abstract Length Classification
- Classify abstracts as **short vs long** based on word count using a **Random Forest Classifier**.
- Features include:
  - `publish_year`
  - `title_word_count`
  - `num_authors`
  - One-hot encoded top journals
- Outputs in the app:
  - Cross-validated accuracy
  - Classification report
  - Confusion matrix
  - Feature importance plot
  - Predicted probabilities scatter and histogram
  - Correlation heatmap of numeric features

### 🔳 Interactive Streamlit Application
- Built a **fully interactive dashboard** using Streamlit.
- Displayed tables, plots, and word clouds dynamically.
- Users can explore the dataset visually without running code locally.
- Clean, intuitive layout suitable for presentations or reports.

---

## Skills Demonstrated

- **Python Programming:** Data loading, cleaning, and feature engineering.
- **Data Analysis:** Handling missing values, descriptive statistics, numerical and categorical processing.
- **Data Visualization:** Matplotlib, Seaborn, WordCloud for clear, interpretable plots.
- **Machine Learning:** Random Forest for classification, model evaluation (cross-validation, confusion matrix, feature importance).
- **Web App Development:** Streamlit dashboard for interactive exploration.
- **Data Communication:** Translating data insights into interactive visuals and concise reports.

---

## Dataset

- **Source:** [CORD-19 Research Challenge - Kaggle](https://www.kaggle.com/allen-institute-for-ai/CORD-19-research-challenge)
- **File Used:** `metadata.csv` (or a sampled version for performance)
- Contains:
  - Paper titles and abstracts
  - Publication dates
  - Authors and journals
  - Source information

> Note: The full CORD-19 dataset is very large. This project uses a sampled dataset for fast exploration and deployment.

---

## Requirements

- Python 3.7+
- Libraries:
  - pandas
  - numpy
  - matplotlib
  - seaborn
  - wordcloud
  - scikit-learn
  - streamlit

Install with:

```bash
pip install -r requirements.txt
````

---

## How to Run Locally

1. Clone the repository:

```bash
git clone https://github.com/Robibiruk/CORD19_Sample.git
cd CORD19_Sample
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Run the Streamlit app:

```bash
streamlit run main.py
```

4. Open the provided URL in your browser to interact with the app.

---

## Live Deployment

Experience the app live on **Streamlit Cloud**:

[https://cord19-sample-analysis.streamlit.app/](https://cord19-sample-analysis.streamlit.app/)

---

## Project Workflow

1. **Data Exploration:** Understand the dataset structure and identify cleaning needs.
2. **Cleaning & Feature Engineering:** Handle missing values, create new columns, reduce categories.
3. **Visualization:** Build plots to communicate patterns and trends.
4. **Machine Learning:** Classify abstracts as short or long and analyze model performance.
5. **Streamlit App:** Combine all analyses into an interactive dashboard for easy access and presentation.

---

## Learning Outcomes

* Hands-on experience with **real-world scientific datasets**.
* Skills in **data cleaning, visualization, and basic ML classification**.
* Experience building **interactive data-driven web applications**.
* Ability to communicate insights visually and interactively.

---

## Screenshots

### 🔳 Dashboard Overview
![Dashboard Overview](https://icecream.me/uploads/14d6b74221dd63a19f517491537d6571.png)


### 🔳 Publications Over Time
![Publications Over Time](https://icecream.me/uploads/0f1daad05245cb447eb54656b477eea0.png)


### 🔳 Top Journals
![Top Journals](https://icecream.me/uploads/3bc75152aa2a97ddba85cb8b1cb4629b.png)


### 🔳 Word Cloud
![Word Cloud](https://icecream.me/uploads/b79791e0c630bc69cf8501d05bad8bfb.png)


### 🔳 Abstract Classification
![Abstract Classification](https://icecream.me/uploads/4277e1815ebd8cd688102038352a6b1a.png)


### 🔳 Source Distribution
![Source Distribution](https://icecream.me/uploads/69a46cf9bde5b231759a5f4c6c78bcf4.png)



## Author

**Robel Biruk**

* [GitHub Repository](https://github.com/Robibiruk/CORD19_Sample)
* [Streamlit App](https://cord19-sample-analysis.streamlit.app/)

---

## License

⚖️ This project is released under the MIT License.
