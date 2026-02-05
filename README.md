# Customer Segmentation Using Clustering Algorithms

A comprehensive exploration of unsupervised learning techniques for pattern discovery and customer segmentation, featuring K-Means, Hierarchical Clustering, and DBSCAN implementations.

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.0%2B-orange.svg)](https://scikit-learn.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

## 📋 Table of Contents
- [Overview](#overview)
- [Algorithms Implemented](#algorithms-implemented)
- [Dataset](#dataset)
- [Key Features](#key-features)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Results & Insights](#results--insights)
- [Technologies Used](#technologies-used)
- [Learning Outcomes](#learning-outcomes)
- [Article](#article)
- [Contact](#contact)

## 🎯 Overview

This project demonstrates practical implementation of three major clustering algorithms to uncover hidden patterns in unlabeled data. Using a real-world City Lifestyle dataset, I explore how different clustering approaches reveal distinct customer segments and behavioral patterns.

**Business Context:** Customer segmentation is crucial for targeted marketing, personalized services, and strategic decision-making. This project showcases how unsupervised learning can transform raw data into actionable business insights.

## 🧮 Algorithms Implemented

### 1. **K-Means Clustering**
- Centroid-based partitioning algorithm
- Optimal cluster selection using Elbow Method and Silhouette Score
- Feature scaling and PCA visualization
- Detailed cluster interpretation and profiling

### 2. **Hierarchical Clustering**
- Agglomerative (bottom-up) approach
- Dendrogram visualization for cluster hierarchy
- Multiple linkage methods comparison (Ward, Complete, Average)
- Nested cluster structure analysis

### 3. **DBSCAN (Density-Based Spatial Clustering)**
- Density-based clustering for arbitrary shapes
- Automatic outlier detection
- No need to specify number of clusters
- Parameter optimization (eps and min_samples)

## 📊 Dataset

**Source:** [City Lifestyle Dataset - Kaggle](https://www.kaggle.com/)

**Features:**
- Population Density
- Average Income
- Air Pollution Index
- Happiness Score
- Green Space Ratio
- Internet Penetration
- Public Transport Score
- Rental Costs


The dataset contains socioeconomic and environmental indicators for various cities, making it ideal for discovering lifestyle-based segments.

## Key Features

- ✅ **Complete preprocessing pipeline** (handling missing values, feature scaling, outlier detection)
- ✅ **Multiple evaluation metrics** (Inertia, Silhouette Score, Davies-Bouldin Index)
- ✅ **Rich visualizations** (2D/3D scatter plots, dendrograms, heatmaps, elbow curves)
- ✅ **Cluster interpretation** with business insights
- ✅ **Comparative analysis** of all three algorithms
- ✅ **Well-documented code** with detailed comments
- ✅ **Reproducible results** (random seeds set)

## Installation

### Prerequisites
- Python 3.8 or higher
- pip package manager

### Setup

1. **Clone the repository**
```bash
git clone https://github.com/your-username/customer-segmentation-clustering.git
cd customer-segmentation-clustering
```

2. **Create a virtual environment (recommended)**
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install required packages**
```bash
pip install -r requirements.txt
```

### Required Libraries
```txt
numpy>=1.21.0
pandas>=1.3.0
scikit-learn>=1.0.0
matplotlib>=3.4.0
seaborn>=0.11.0
scipy>=1.7.0
jupyter>=1.0.0
```

## 💻 Usage

### Quick Start

Run the Jupyter notebooks in order:
```bash
jupyter notebook
```

1. **`01_data_exploration.ipynb`** - Data loading, EDA, and preprocessing
2. **`02_kmeans_clustering.ipynb`** - K-Means implementation and analysis
3. **`03_hierarchical_clustering.ipynb`** - Hierarchical clustering with dendrograms
4. **`04_dbscan_clustering.ipynb`** - DBSCAN implementation
5. **`05_comparison_analysis.ipynb`** - Comparative evaluation of all methods

### Running Python Scripts
```bash
# Run K-Means clustering
python scripts/kmeans_analysis.py

# Run all clustering algorithms
python scripts/run_all_clustering.py

# Generate visualizations
python scripts/generate_visualizations.py
```

## 📁 Project Structure
```
customer-segmentation-clustering/
│
├── data/
│   ├── raw/
│   │   └── city_lifestyle_dataset.csv
│   └── processed/
│       └── scaled_data.csv
│
├── notebooks/
│   ├── 01_data_exploration.ipynb
│   ├── 02_kmeans_clustering.ipynb
│   ├── 03_hierarchical_clustering.ipynb
│   ├── 04_dbscan_clustering.ipynb
│   └── 05_comparison_analysis.ipynb
│
├── scripts/
│   ├── kmeans_analysis.py
│   ├── hierarchical_analysis.py
│   ├── dbscan_analysis.py
│   └── utils.py
│
├── visualizations/
│   ├── kmeans/
│   ├── hierarchical/
│   └── dbscan/
│
├── results/
│   ├── cluster_profiles.csv
│   ├── evaluation_metrics.csv
│   └── insights.md
│
├── requirements.txt
├── README.md
├── LICENSE
└── .gitignore
```

## 📈 Results & Insights

### K-Means Clustering (K=3)

**Cluster 0: High-Density Urban Stress Zones**
- High population density and air pollution
- Lower income and happiness scores
- Limited green spaces

**Cluster 1: Low-Income Underserved Regions**
- Low income and internet penetration
- Poor public transport infrastructure
- Lower overall quality of life indicators

**Cluster 2: Affluent High-Quality Living Areas**
- Above-average income and happiness
- Better air quality and green spaces
- Strong public infrastructure

### Key Visualizations

![K-Means Clusters](visualizations/kmeans/clusters_pca.png)
*PCA visualization of K-Means clusters*

![Elbow Method](visualizations/kmeans/elbow_curve.png)
*Elbow method for optimal K selection*

![Dendrogram](visualizations/hierarchical/dendrogram.png)
*Hierarchical clustering dendrogram*

### Performance Metrics

| Algorithm | Silhouette Score | Davies-Bouldin Index | Execution Time |
|-----------|------------------|---------------------|----------------|
| K-Means (k=3) | 0.XX | X.XX | X.XX s |
| Hierarchical | 0.XX | X.XX | X.XX s |
| DBSCAN | 0.XX | X.XX | X.XX s |

## 🛠 Technologies Used

- **Python 3.8+** - Core programming language
- **NumPy** - Numerical computations
- **Pandas** - Data manipulation and analysis
- **Scikit-learn** - Machine learning algorithms
- **Matplotlib & Seaborn** - Data visualization
- **SciPy** - Scientific computing (dendrograms)
- **Jupyter Notebook** - Interactive development

## 🎓 Learning Outcomes

Through this project, I developed expertise in:

1. **Unsupervised Learning Fundamentals**
   - Understanding when and why to use clustering
   - Choosing appropriate algorithms for different data characteristics

2. **Data Preprocessing**
   - Feature scaling and standardization
   - Handling missing values and outliers
   - Dimensionality reduction with PCA

3. **Model Evaluation**
   - Silhouette analysis
   - Elbow method
   - Davies-Bouldin Index
   - Domain-specific validation

4. **Business Intelligence**
   - Translating clusters into actionable insights
   - Customer segmentation strategies
   - Data-driven decision making

5. **Technical Communication**
   - Clear code documentation
   - Effective data visualization
   - Writing technical articles

## 📝 Article

I wrote a comprehensive Medium article explaining K-Means clustering in detail:

**[Understanding K-Means Clustering: A Practical Guide for Unsupervised Learning](your-medium-article-link)**

The article covers:
- Theoretical foundations of K-Means
- Step-by-step implementation in Python
- Importance of feature scaling
- Cluster interpretation techniques
- Common pitfalls and best practices

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://github.com/your-username/customer-segmentation-clustering/issues).

### How to Contribute

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👤 Contact

**Suparna Chowdhury**

[![Portfolio](https://img.shields.io/badge/Website-000000?logo=About.me&logoColor=white)](https://suparnachowdhury.github.io/home/index.html) 
[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/suparna-chowdhury) 
[![Medium](https://img.shields.io/badge/Medium-12100E?logo=medium&logoColor=white)](https://suparnachowdhury.medium.com/)
[![Twitter](https://img.shields.io/badge/Twitter-%231DA1F2.svg?logo=X&logoColor=white)](https://x.com/DataSapient) 

---

⭐ If you found this project helpful, please consider giving it a star!

**Project Link:** [https://github.com/suparnachowdhury/advanced-clustering-analysis](https://github.com/suparnachowdhury/advanced-clustering-analysis)

---

*This project was created as part of my data science portfolio to demonstrate practical machine learning skills and analytical thinking.*
