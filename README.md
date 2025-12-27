# 📚 Predicting Book Success: A Data-Driven Analysis

## 📖 Project Overview

**Project Duration:** 2 Weeks  
**Domain:** Literary & Linguistic Data Analysis

This capstone project aims to design and implement a data-driven analysis system that predicts book success (defined by high star ratings). By combining web-scraped data from a fictional bookstore with real-world dataset from Goodreads, this project explores literary patterns, analyzes features like price and description sentiment, and builds predictive machine learning models.

### 🎯 Core Objectives
* **Data Acquisition:** Scrape 200+ books from *books.toscrape.com* and integrate with Kaggle's Goodreads dataset.
* **EDA:** Identify factors contributing to a book’s popularity (Price, Category, Description Length).
* **Machine Learning:** Develop models to classify books as "High Rated" or "Low Rated."

---

## 📂 Repository Structure

| File Name | Description |
| :--- | :--- |
| `Capstone_Project.ipynb` | The main Jupyter Notebook containing all code for scraping, cleaning, EDA, and modeling. |
| `scraped_books.csv` | Raw data scraped from *books.toscrape.com* (Title, Price, Stock, Description, etc.). |
| `goodreads_books.csv` | External dataset from Kaggle (Real-world book ratings). |
| `combined_books_data.csv` | Merged dataset used for comparative analysis. |
| `cleaned_books_data.csv` | Final processed dataset used for EDA and visualization. |
| `README.md` | Project documentation (this file). |

---

## ⚙️ Methodology

### 1. Data Acquisition (Web Scraping)
* **Tool:** BeautifulSoup & Requests
* **Source:** [Books to Scrape](http://books.toscrape.com/)
* **Process:** Iterated through catalogue pages to extract Title, Price, Star Rating, Availability, and Product Description.
* **Output:** `scraped_books.csv` containing 200+ entries.

### 2. Data Integration & Cleaning
* Merged the scraped fictional data with the **Goodreads Books Dataset** from Kaggle.
* **Cleaning Steps:**
    * Handled missing values in `Title` and `Rating` fields.
    * Standardized text (lowercase, removed punctuation).
    * Converted `Price` and `Star Rating` to numeric types.
    * Removed outliers (e.g., negative prices).

### 3. Exploratory Data Analysis (EDA)
Key insights visualized using Matplotlib and Seaborn:
* **Rating Distribution:** Compared the spread of ratings between "Real" (Goodreads) and "Fictional" (Scraped) books.
* **Price vs. Rating:** Analyzed if expensive books receive better ratings (Correlation found to be low).
* **Text Analysis:** Examined the relationship between description length/sentiment and book success.

### 4. Machine Learning
* **Goal:** Predict if a book is "High Rated" (≥ 4 Stars) or "Low Rated" (< 4 Stars).
* **Feature Engineering:**
    * TF-IDF Vectorization for book descriptions.
    * One-Hot Encoding for book categories.
    * Sentiment Analysis using `TextBlob`.
* **Models Trained:**
    * Logistic Regression
    * Random Forest Classifier
    * Support Vector Machine (SVM)

---

## 📊 Key Findings

1.  **Price is not a predictor of quality:** There is no significant correlation between how much a book costs and its star rating in the scraped dataset.
2.  **Sentiment Matters:** Words used in the description (captured via TF-IDF) played a role in the model's ability to classify successful books.
3.  **Model Performance:** The **Random Forest Classifier** achieved the highest accuracy, suggesting that non-linear relationships between category and description features are important.

## 👤 Author

**Kasaba6330** *Data Science Enthusiast*
