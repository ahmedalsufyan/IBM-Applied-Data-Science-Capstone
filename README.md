# 🚀 IBM Applied Data Science Capstone Project

**Author:** Ahmed Al-Sufyan  
**Project:** SpaceX Falcon 9 First Stage Landing Prediction  
**Repository:** [IBM-Applied-Data-Science-Capstone](https://github.com/AhmedAlsufyan/IBM-Applied-Data-Science-Capstone)  

---

## 📌 Executive Summary
Commercial space launch services have transformed global aerospace logistics. Space Y—a hypothetical competitor to SpaceX—aims to offer lower bidding prices by determining whether first-stage rocket cores can be safely recovered and reused. 

This project delivers an end-to-end data science and machine learning pipeline to predict the successful landing outcome of Falcon 9 first-stage boosters using API metrics, web-scraped data, SQL queries, exploratory data analysis (EDA), and machine learning classification algorithms.

---

## 🛠️ Data Science Pipeline & Architecture

1. **Data Collection:**
   * Fetched historical SpaceX launch records via REST API endpoints.
   * Scraped Falcon 9 launch records and payloads directly from Wikipedia tables using `BeautifulSoup`.
2. **Data Wrangling & Cleaning:**
   * Handled missing values (mean payload imputation).
   * Feature engineering to generate a binary target variable (`Class`: `1` for Success, `0` for Failure).
3. **Exploratory Data Analysis (EDA):**
   * Relational SQL queries via `sqlite3` to evaluate orbit types, payload statistics, and launch site performance.
   * Visualized relationships between flight numbers, payload mass, and landing success using `Seaborn` and `Matplotlib`.
4. **Machine Learning Classification:**
   * Standardized features using `StandardScaler` and applied `One-Hot Encoding`.
   * Evaluated and hyperparameter-tuned multiple classification models using `GridSearchCV` with 10-fold Cross-Validation.

---

## 📊 Machine Learning Model Results

| Machine Learning Model | Best CV Score | Test Accuracy Score |
| :--- | :---: | :---: |
| **Logistic Regression** | **0.7911** | **94.44%** |
| **Support Vector Machine (SVM)** | **0.8339** | **94.44%** |
| **Decision Tree Classifier** | 0.7518 | 88.89% |
| **K-Nearest Neighbors (KNN)** | 0.7589 | 77.78% |

> **Key Insight:** **Logistic Regression** and **Support Vector Machine (SVM)** yielded the highest accuracy on unseen test data (**94.44%**).

---

## 💡 Key Business Takeaways
* **Payload Mass & Flight Experience:** Heavy payload capacities and higher flight counts strongly correlate with successful landings.
* **Launch Site Success:** Launch sites such as `KSC LC 39A` and `VAFB SLC 4E` exhibit higher success rates compared to early launch pads.
* **Commercial Value:** Accurately predicting booster recovery enables Space Y to estimate reusable launch costs dynamically and optimize commercial pricing strategies.

---

## 📁 Repository Structure
