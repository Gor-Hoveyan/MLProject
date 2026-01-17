# 🚗 Auto.am Market Analysis & Price Prediction (AI & ML)

![Python](https://img.shields.io/badge/python-3.10+-blue.svg)
![Machine Learning](https://img.shields.io/badge/ML-Random%20Forest-green.svg)
![Selenium](https://img.shields.io/badge/Scraping-Selenium-orange.svg)
![Status](https://img.shields.io/badge/Status-Completed-success.svg)

An end-to-end Machine Learning project that scrapes, cleans, analyzes, and predicts used car prices in the Armenian market (**Auto.am**). This project was developed as a final submission for the **AI & Machine Learning Exam (2026)**.

---

## 🌟 Project Overview
This project solves the problem of price opacity in the used car market by creating a data-driven valuation model. It covers the entire AI lifecycle:
1. **Data Acquisition:** Real-time web scraping.
2. **Data Engineering:** ETL (Extract, Transform, Load) processes.
3. **EDA:** Exploratory Data Analysis to find market trends.
4. **Modeling:** Supervised learning using Regression.

---

## 🛠️ Technical Pipeline

### 1. Web Scraping 🌐
We used **Selenium WebDriver** to extract data from Auto.am.
- **Anti-Bot Bypass:** Implemented User-Agent rotation and CDP (Chrome DevTools Protocol) commands to hide automated footprints.
- **Data Extracted:** Brand, Model, Year, Price (AMD/USD), and Mileage.



### 2. Data Preprocessing & Cleaning 🧹
Raw web data is messy. We performed the following:
- **Currency Standardization:** Converted all prices to USD using a fixed exchange rate (1 USD = 400 AMD).
- **Regex Cleaning:** Stripped non-numeric characters from mileage and price strings.
- **Feature Engineering:** Created the `Vehicle_Age` feature ($2025 - Year$) to provide a linear correlation for the model.



### 3. Machine Learning Model 🧠
The core of this project is a **Random Forest Regressor**. 
- **Algorithm:** Random Forest was chosen for its ability to handle non-linear relationships and its robustness against outliers.
- **Training:** 80/20 Train-Test split.
- **Feature Importance:** Identified that **Vehicle Age** is the strongest predictor of price, followed by **Mileage**.



---

## 📊 Visual Insights (EDA)
The following insights were derived from the data:
- **Price Distribution:** Most cars in the market fall within the $5,000 - $15,000 range.
- **Depreciation:** A steep price drop is observed in the first 5-7 years of a vehicle's life.
- **Market Dominance:** High frequency of brands like Toyota, Mercedes-Benz, and BMW in the Armenian secondary market.



---

## 📈 Model Performance
| Metric | Value |
| :--- | :--- |
| **Algorithm** | Random Forest Regressor |
| **Mean Absolute Error (MAE)** | ~$9,510 USD |
| **R² Score** | 0.75 |

*Note: The R² score indicates that while age and mileage are strong indicators, other factors (condition, engine size, options) also play a significant role in pricing.*

---

## 📂 Repository Structure
- `auto_scraper.py`: Selenium-based data collection script.
- `data_cleaning.py`: Script for regex cleaning and feature engineering.
- `ml_model.ipynb`: Jupyter Notebook containing EDA and ML training.
- `plots/`: Folder containing all generated visualizations.
- `data/`: CSV files of the raw and cleaned datasets.

---

## 🎓 Author
**Gor Hoveyan** Artificial Intelligence & Machine Learning  
Academic Year: 2026

---
*This project is for educational purposes as part of an AI & ML examination.*
