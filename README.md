## Global-Clustering-Development
A Streamlit-based web application for forecasting stock prices using historical market data. This project integrates both traditional and advanced time series forecasting models including LSTM and Facebook Prophet to provide users with insightful predictions and visualizations.

## 📑 Table of Contents

1. [Project Overview](#project-overview)  
2. [Data Collection](#data-collection)  
3. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)  
   - Country-wise Indicator Distribution  
   - Correlation Heatmaps  
   - PCA Visualization  
4. [Clustering Models](#clustering-models)  
   - K-Means Clustering  
   - Hierarchical (Agglomerative) Clustering  
   - DBSCAN  
5. [Deployment](#deployment)  
   - Streamlit App Features  
   - Cluster Interpretation & Visualization  
6. [Model Files Used for Deployment](#model-files-used-for-deployment)  
   - PCA Model: `pca_model.pkl`  
   - K-Means Model: `kmeans_model.pkl`  
   - Scaler File: `scaler.pkl`

---

## 📌 Project Overview

This repository contains a Streamlit web application that segments countries into development-based clusters using socio-economic indicators. The app applies unsupervised learning techniques like K-Means and Hierarchical Clustering and provides visual insights into how countries are grouped based on health, education, economy, and infrastructure.

The aim is to assist global organizations, NGOs, and governments in identifying country-level development patterns for better policy-making and resource planning.

---

## 📊 Data Collection

- **Sources:**  
  - [World Bank Open Data](https://data.worldbank.org)  
  - [United Nations Development Programme](https://hdr.undp.org)  
- Indicators considered:  
  - GDP per capita  
  - Literacy rate  
  - Life expectancy  
  - Internet usage  
  - Access to electricity  
  - Health expenditure  
  - And more...

---

## 📈 Exploratory Data Analysis (EDA)

- Explored indicator distributions using histograms and box plots  
- Generated **correlation matrices** to detect multicollinearity  
- Applied **Principal Component Analysis (PCA)** for dimensionality reduction and visualization

### Key Visuals:
- Country-wise Indicator Comparison  
- Correlation Heatmaps  
- PCA-based Scatter Plot of Country Clusters  

---

## 🔍 Clustering Models

### K-Means Clustering  
- Used Elbow Method and Silhouette Score to identify optimal number of clusters  
- Trained model on scaled PCA components

### Hierarchical (Agglomerative) Clustering  
- Built dendrograms to visualize hierarchical relationships  
- Useful for interpretable cluster merging decisions

### DBSCAN  
- Density-based model to identify noise points and non-linear clusters  
- Tested for robustness but not selected for final deployment

---

## 🚀 Deployment

The app is deployed using **Streamlit**, allowing users to:

- Select the number of clusters dynamically  
- Visualize countries colored by clusters on an interactive world map  
- View statistics and indicators for each cluster  
- Compare countries within a selected cluster

---

## 🧠 Model Files Used for Deployment

- **PCA Model:** `pca_model.pkl`  
- **K-Means Model:** `kmeans_model.pkl`  
- **Scaler File:** `scaler.pkl`  
- **Clustered Dataset:** `clustered_data.csv`
