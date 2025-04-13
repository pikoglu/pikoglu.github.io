---
title: "🌍 Land Type Identification via Satellite Imagery"
excerpt: "<img src='/images/portfolio/satellite.png'>"
collection: portfolio
category: Research Projects
---

* __Project Type__: Group Research Project  
* __With__: Gabriel Mariadass and Vincent Gefflaut, supervised by Konstantin Kuznetsov & Pavel Litvinov (GRASP Earth)
* __Ressources__: **Read the report**: [Report](/files/portfolio/clustering_report.pdf)
* __When__: 2024
* __Associated to__: [ENPC](https://www.enpc.fr/en)

<image src='/images/portfolio/satellite.png' width="100%" />


### 🚀 Overview

This project explored **unsupervised land type classification** based on satellite-derived climatological data. Leveraging a global dataset provided by [GRASP Earth](https://www.grasp-earth.com), we applied **dimensionality reduction and clustering techniques** to segment the Earth's surface based on optical soil properties.

### 🛰️ Dataset

We used the **POLDER climatological dataset**, containing 131 optical variables over 64,800 geolocated points at 1.1° resolution. The focus was on land-only regions, with variables such as:
- **NDVI** (vegetation index)
- **DHR** (Bidirectional Reflectance Factors at multiple wavelengths)

### 🔍 Methodology

#### 1. Data Preprocessing
- Variable selection based on physical relevance (NDVI, DHRs)
- Normalization and correlation analysis to reduce redundancy

#### 2. Clustering on Raw Features
- Implemented **Hierarchical Agglomerative Clustering (HAC)** and **K-Means**
- Visualization over satellite maps
- Quantitative comparison using **Silhouette Score**

#### 3. Dimensionality Reduction
- Applied **PCA** to capture >95% variance with only 3 components
- Clustering in PCA space preserved spatial structure with minimal information loss

#### 4. Variational Autoencoder (VAE)
- Built a custom VAE for non-linear dimensionality reduction
- Trained on physical land parameters to learn a **structured latent space**
- Achieved superior clustering performance (Silhouette score: **0.40**, vs. PCA: **0.27**)
- Explored **1D VAE** for interpretable, segment-based clustering

### 🧠 Highlights

- Demonstrated effective **land segmentation** using unsupervised learning
- Built pipelines for data ingestion, preprocessing, clustering, and visualization
- Integrated both **classical ML** and **deep learning** (VAE) techniques
- Visualized clusters over satellite imagery for interpretability
- Latter, we developped a web application to let the users choose the variables and parameters, and explore the results, linking the segmentation with other classifications.

### 📊 Tools & Technologies

- Python (Pandas, Scikit-learn, PyTorch, Seaborn, Plotly)
- Satellite data processing (xarray, netCDF4)
- Custom interactive map generation (Mapbox)
- Web Application, via Plotly
