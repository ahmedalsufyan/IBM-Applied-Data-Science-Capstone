# IBM Data Science Capstone Project: SpaceX Falcon 9 Landing Prediction

**Author:** Ahmed Alsufyan  
**Repository:** [IBM-Applied-Data-Science-Capstone](https://github.com/ahmedalsufyan/IBM-Applied-Data-Science-Capstone)  
**Live Interactive Dashboard:** [SpaceX Streamlit Web App](https://grinch-basics-unjustly.ngrok-free.dev/)

---

## 📌 Executive Summary
The primary objective of this capstone project is to predict the landing success of SpaceX Falcon 9 first-stage boosters. By accurately forecasting whether a booster will land successfully, we can estimate launch costs and evaluate commercial feasibility, as first-stage reusability significantly reduces spaceflight expenditure. 

This project encompasses the full data science workflow:
* **Data Collection** via SpaceX REST API and BeautifulSoup Web Scraping.
* **Data Cleaning & Wrangling** using Pandas to handle missing values and feature encoding.
* **Exploratory Data Analysis (EDA)** using SQL queries and visualizations (Seaborn/Matplotlib).
* **Interactive Data Visualization** using Folium spatial mapping and Streamlit interactive web applications.
* **Machine Learning Prediction** using Logistic Regression, Support Vector Machines (SVM), Decision Trees, and K-Nearest Neighbors (KNN), optimized via `GridSearchCV`.

---

## 🛠️ Project Structure & Notebooks

| Module / Notebook | Description | Source / Live Link |
| :--- | :--- | :--- |
| **1. Data Collection (API)** | Fetched flight launch metrics using SpaceX API endpoint. | [`1_Data_Collection_API.ipynb`](./1_Data_Collection_API.ipynb) |
| **2. Data Collection (Scraping)** | Scraped historical launch data from Wikipedia using `BeautifulSoup`. | [`2_Data_Collection_WebScraping.ipynb`](./2_Data_Collection_WebScraping.ipynb) |
| **3. Data Wrangling** | Performed data transformation, missing value imputation, and One-Hot Encoding. | [`3_Data_Wrangling.ipynb`](./3_Data_Wrangling.ipynb) |
| **4. EDA with Visualizations** | Evaluated relationships between flight number, payload mass, launch sites, and orbit types. | [`4_EDA_Visualization.ipynb`](./4_EDA_Visualization.ipynb) |
| **5. EDA with SQL** | Ran exploratory queries using SQLite to compute success rates and payload aggregates. | [`5_EDA_SQL.ipynb`](./5_EDA_SQL.ipynb) |
| **6. Interactive Maps (Folium)** | Mapped launch site locations, outcome markers, and calculated proximity to landmarks. | [`6_Interactive_Visual_Analytics_Folium.ipynb`](./6_Interactive_Visual_Analytics_Folium.ipynb) |
| **7. Machine Learning Models** | Built and evaluated classification algorithms with cross-validation. | [`7_Machine_Learning_Prediction.ipynb`](./7_Machine_Learning_Prediction.ipynb) |
| **8. Interactive Dashboard** | Dynamic Streamlit dashboard deployed via ngrok. | 🚀 [Live App Link](https://grinch-basics-unjustly.ngrok-free.dev/) \| [`app.py`](./app.py) |

---

## 📊 Key Insights & Results

* **Launch Site Success:** Specific launch sites like `KSC LC-39A` demonstrated significantly higher landing success rates compared to earlier flight test sites.
* **Payload Impact:** Heavier payloads typically exhibit higher landing success rates, correlating with improved hardware reliability in later Falcon 9 block iterations.
* **Model Performance:** 
  * Classification models (Logistic Regression, Decision Tree, SVM, and KNN) were evaluated using `GridSearchCV`.
  * **Decision Tree** and **Logistic Regression** achieved top-tier predictive performance with strong accuracy scores on the evaluation test set.

---

## 🚀 Interactive Web Dashboard

The project includes an interactive web interface powered by **Streamlit** to visualize landing outcomes dynamically.

* **Live URL:** [https://grinch-basics-unjustly.ngrok-free.dev/](https://grinch-basics-unjustly.ngrok-free.dev/)

### How to Run Locally:
```bash
# Clone the repository
git clone [https://github.com/ahmedalsufyan/IBM-Applied-Data-Science-Capstone.git](https://github.com/ahmedalsufyan/IBM-Applied-Data-Science-Capstone.git)

# Navigate to the repository
cd IBM-Applied-Data-Science-Capstone

# Run the Streamlit application
streamlit run app.py
