# US-road-accident-severity-analysis


# Predicting Road Accident Severity in the United States (2016–2023)

## 📌 Project Overview
This project analyzes road traffic accidents across the United States using the **US Accidents dataset (2016–2023)**. The goal is to **predict accident severity** and identify the most influential environmental, temporal, and road-related factors contributing to severe crashes.

The study applies **Multiple Linear Regression**, **Logistic Regression**, and **Random Forest classification** to model accident severity and compare interpretability versus predictive performance.

---

## 🎯 Objectives
- Identify key predictors of road accident severity in the US  
- Understand how **weather**, **road features**, and **time-based factors** influence severity  
- Compare traditional regression models with machine learning approaches  
- Visualize spatial and temporal patterns in accident severity  

---

## 📊 Dataset
- **Source:** Kaggle – *U.S. Accidents (2016–2023)*
- **Coverage:** 49 U.S. states  
- **Original Size:** ~7.7 million records, 46 variables  
- **Sample Used:** 50,000 observations (for computational efficiency)  
- **Target Variable:**  
  - `Severity` (ordinal scale: 1 = least severe, 4 = most severe)

### Key Features
- **Weather:** Temperature, precipitation, visibility, pressure  
- **Road Features:** Traffic signals, junctions, bumps, crossings, stops  
- **Time Variables:** Hour of day, rush hour, weekend vs weekday  
- **Geography:** U.S. state  

---

## 🛠️ Methodology

### 1. Data Preprocessing
- Column selection and missing value removal  
- Feature engineering:
  - Rush hour indicator
  - Weekend indicator
  - Simplified weather categories
  - Composite road feature indicator  

### 2. Exploratory Data Analysis
- Severity trends by hour of day  
- Severity distribution across temperature ranges  
- State-wise average severity mapping  

### 3. Modeling Approaches
- **Multiple Linear Regression**
  - Full model with all predictors
  - Reduced model with significant predictors only
- **Logistic Regression**
- **Random Forest Classifier**
  - 500 trees
  - Variable importance analysis
  - Confusion matrix and accuracy evaluation  

---

## 📈 Key Results

### Multiple Linear Regression
- Full model adjusted R² ≈ **6%**
- Reduced model adjusted R² ≈ **7.8%**
- Significant predictors include:
  - Weather (rain, snow, freezing conditions)
  - Weekend indicator
  - Traffic signals (negative effect on severity)
  - Road features (generally reduce severity)

### Random Forest Model
- **Overall accuracy:** ~**85%**
- Top predictors:
  - Distance
  - State
  - Traffic signal presence
  - Atmospheric pressure
- Strong performance for majority severity class, weaker for rare classes (1 and 4)

---

## 🗺️ Visualizations
- Average accident severity by hour of day  
- Severity by temperature range  
- State-wise severity heat map  
- Random Forest variable importance plots  
- Confusion matrix heatmap  

---

## ⚠️ Limitations
- Severity is an **ordinal variable**, limiting linear model assumptions  
- Class imbalance affects prediction of rare severity levels  
- Sampling may omit some extreme cases  

---

## 📂 Repository Structure
