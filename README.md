# IBM Data Science Capstone Project - SpaceX Falcon 9 Landing Prediction

## Executive Summary
This project aims to predict the success of SpaceX Falcon 9 first-stage landings to evaluate reusability and estimate launch costs. Using various data science techniques—including API data collection, web scraping, data wrangling, exploratory data analysis (EDA) via SQL and visualization tools, interactive mapping, dynamic dashboards, and machine learning algorithms—we developed models capable of predicting landing outcomes with high accuracy.

---

## Project Architecture & Methodology
1. **Data Collection**: 
   - Retreived flight data via SpaceX REST API.
   - Web scraped historical launch records from Wikipedia using `BeautifulSoup`.
2. **Data Wrangling**: 
   - Handled missing values, encoded categorical variables using One-Hot Encoding, and formatted binary target variables (`Class`).
3. **Exploratory Data Analysis (EDA)**:
   - Visualized payload mass, flight numbers, and launch site outcomes using `Matplotlib` & `Seaborn`.
   - Executed SQL queries in `SQLite` to analyze payload totals, success rates, and launch site rankings.
4. **Interactive Visual Analytics**:
   - Built interactive Folium maps with marker clusters and distance proximity analysis.
   - Developed an interactive dashboard using `Streamlit` / `Plotly` to filter launch metrics.
5. **Predictive Analytics (Machine Learning)**:
   - Trained and evaluated Logistic Regression, SVM, Decision Tree, and KNN classifiers using `GridSearchCV`.

---

## Repository Structure
