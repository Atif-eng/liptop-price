# 💻 Laptop Market 2026: Pricing Logic & Spec Mining

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Library](https://img.shields.io/badge/Library-XGBoost-red)
![Library](https://img.shields.io/badge/Library-Plotly-green)
![Status](https://img.shields.io/badge/Status-Completed-success)

## 📌 Project Overview
**"Why does this laptop cost $2000?"**

This project aims to reverse-engineer the pricing logic of the laptop market. By mining specifications directly from raw text and applying Machine Learning, we identify the **"Premium Brand Tax"** (e.g., Apple vs. Dell) and predict the fair market value of devices. 

The goal is to help consumers find the **"Best Value"** segments—laptops that offer high performance without the flagship markup.

**Author:** Muhammad Atif

## 📂 Dataset
The dataset (**PriceOye Laptops Version 2**) contains raw listings of laptops including their titles, prices, and unstructured specification strings.

- **Target Variable:** `Price` (Numerical).
- **Key Features (Mined):**
  - **Processor:** Core i5 vs. i7 vs. M3.
  - **RAM & Storage:** Extracted from text (e.g., "8GB/256GB").
  - **Brand:** Apple, HP, Lenovo, Dell, etc.

## 🛠 Tech Stack
- **Language:** Python
- **Data Manipulation:** `pandas`, `numpy`
- **Visualization:** - `matplotlib` & `seaborn` (Static Plots)
  - `plotly` (Interactive Charts)
- **Machine Learning:** - `scikit-learn` (Random Forest, Gradient Boosting)
  - `xgboost` (XGBRegressor)

## 📊 Project Workflow

### 1. Feature Engineering (Spec Mining)
Raw text data was parsed to create structured features:
- **Text Parsing:** Extracted RAM size, SSD capacity, and Processor generation from messy product titles.
- **Brand Hierarchy:** Categorized brands to analyze premium vs. budget positioning.

### 2. Exploratory Data Analysis (EDA)
- **The "Apple Tax":** Visualized the price gap between Apple MacBooks and Windows counterparts with similar specs.
- **Market Segmentation:** Grouped laptops into "Budget," "Mid-Range," and "Flagship" tiers.

### 3. Model Building
Several regression models were trained to predict price:
- **Linear Regression:** Baseline model.
- **Random Forest Regressor:** To capture non-linear price jumps.
- **Gradient Boosting & XGBoost:** The best performers for high-accuracy predictions.

### 4. Results & Insights
- **Feature Importance:** Found that **RAM** and **Processor Generation** were the biggest drivers of price, followed closely by **Brand Name**.
- **Value Gems:** Identified specific models where the predicted price was *higher* than the actual price (Good Deals).

## 🚀 How to Run

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/your-username/laptop-pricing-2026.git](https://github.com/your-username/laptop-pricing-2026.git)
