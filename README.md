# 🛒 InsightCart: Machine Learning from Customer Data

## 📋 Table of Contents
- [About the Project](#about-the-project)
- [Problem Statement](#problem-statement)
- [Dataset Description](#dataset-description)
- [Business Objectives](#business-objectives)
- [Technologies Used](#technologies-used)
- [Project Workflow](#project-workflow)
- [Clustering Algorithms](#clustering-algorithms)
- [Key Features](#key-features)
- [Results & Insights](#results--insights)
- [Installation & Usage](#installation--usage)
- [Project Structure](#project-structure)
- [Lessons Learned](#lessons-learned)
- [Future Improvements](#future-improvements)
- [Contributing](#contributing)
- [License](#license)

---

## 🎯 About the Project

**InsightCart** is an unsupervised machine learning project focused on customer segmentation for SmartCart, a growing e-commerce platform. The project uses clustering algorithms to analyze customer transaction data and identify meaningful customer segments for personalized marketing and improved customer retention.

### The Challenge

SmartCart serves customers across multiple countries but currently uses **generic marketing strategies** for all customers, leading to:
- ❌ Inefficient marketing spend
- ❌ Missed opportunities to retain high-value customers
- ❌ Delayed identification of at-risk customers
- ❌ Poor understanding of distinct customer behavior patterns

### The Solution

Build an **intelligent customer segmentation system** using unsupervised machine learning to:
- ✅ Discover hidden patterns in customer behavior
- ✅ Group customers into meaningful clusters
- ✅ Enable personalized marketing and engagement strategies
- ✅ Support data-driven decision-making for customer retention

---

## 📝 Problem Statement

**SmartCart** is a growing e-commerce platform serving customers across multiple countries. The company has collected extensive customer data consisting of **2240 customer records** with **22 comprehensive attributes** including:
- Demographics
- Purchase behavior
- Website activity
- Customer feedback

### Current Situation
SmartCart uses **generic marketing and engagement strategies** for all customers, without clearly understanding different customer patterns. This results in:
- Inefficient marketing
- Missed opportunities to retain high-value customers
- Delayed identification of at-risk, low-engagement customers

### Goal
Build an **intelligent customer segmentation system** using **unsupervised machine learning** that will:
1. Analyze historical customer transaction data
2. Group customers into meaningful clusters based on:
   - Purchasing behavior
   - Engagement levels
   - Loyalty indicators
3. Enable personalized marketing and customer retention strategies

### Your Role
As an **AI/ML Engineer**, develop this system using **clustering algorithms** to:
- Discover hidden patterns in customer behavior
- Support **data-driven decision-making** for personalized marketing and customer retention

---

## 📊 Dataset Description

The dataset contains **2240 customer records** with **22 attributes** describing customer spending and activity on the platform.

### 1. Customer Demographics

| Feature | Description |
|---------|-------------|
| `ID` | Unique customer identifier |
| `Year_Birth` | Year of birth of the customer |
| `Education` | Highest education level achieved |
| `Marital_Status` | Marital status of the customer |
| `Income` | Yearly household income |
| `Kidhome` | Number of small children in household |
| `Teenhome` | Number of teenagers in household |
| `Dt_Customer` | Date when customer enrolled with SmartCart |

### 2. Purchase Behavior (Amount Spent)

| Feature | Description |
|---------|-------------|
| `MntWines` | Amount spent on wine products |
| `MntFruits` | Amount spent on fruits |
| `MntMeatProducts` | Amount spent on meat products |
| `MntFishProducts` | Amount spent on fish products |
| `MntSweetProducts` | Amount spent on sweet products |
| `MntGoldProds` | Amount spent on gold products |

### 3. Purchase Behavior (Frequency)

| Feature | Description |
|---------|-------------|
| `NumDealsPurchases` | Purchases made using discounts |
| `NumWebPurchases` | Purchases made through website |
| `NumCatalogPurchases` | Purchases made through catalog |
| `NumStorePurchases` | Purchases made in physical stores |
| `NumWebVisitsMonth` | Number of visits to website per month |

### 4. Customer Feedback & Constants

| Feature | Description |
|---------|-------------|
| `Recency` | Number of days since last purchase |
| `Complain` | Customer complained in last 2 years (1 = Yes, 0 = No) |

---

## 🎯 Business Objectives

### Primary Goals
1. **Customer Segmentation**: Identify distinct customer groups with similar behaviors
2. **Behavioral Analysis**: Understand what drives different customer segments
3. **Marketing Optimization**: Enable targeted marketing campaigns
4. **Retention Strategy**: Identify and retain high-value customers
5. **Risk Mitigation**: Detect at-risk or low-engagement customers early

### Expected Outcomes
- Clear customer personas for marketing teams
- Data-driven insights for product recommendations
- Improved customer lifetime value (CLV)
- Reduced customer acquisition costs
- Enhanced customer satisfaction and loyalty

---

## 🛠️ Technologies Used

```python
# Core Libraries
- Python 3.8+
- NumPy
- Pandas

# Data Visualization
- Matplotlib
- Seaborn
- Plotly (interactive visualizations)

# Machine Learning (Clustering)
- Scikit-learn
  - KMeans
  - DBSCAN
  - Hierarchical Clustering
  - Gaussian Mixture Models

# Dimensionality Reduction
- PCA (Principal Component Analysis)
- t-SNE
- UMAP (optional)

# Model Evaluation
- Silhouette Score
- Davies-Bouldin Index
- Calinski-Harabasz Index
- Elbow Method

# Jupyter
- Jupyter Notebook / JupyterLab
```

---

## 🔄 Project Workflow

```
1. Data Collection & Understanding
   ↓
2. Exploratory Data Analysis (EDA)
   - Customer demographics analysis
   - Purchase behavior patterns
   - Correlation analysis
   ↓
3. Data Preprocessing
   - Handle missing values
   - Outlier detection and treatment
   - Feature scaling/normalization
   ↓
4. Feature Engineering
   - Create derived features (customer age, total spending, etc.)
   - Calculate customer lifetime metrics
   - Engineer engagement scores
   ↓
5. Dimensionality Reduction (Optional)
   - PCA for visualization
   - Feature selection
   ↓
6. Clustering Analysis
   - Determine optimal number of clusters
   - Apply multiple clustering algorithms
   - Compare algorithm performance
   ↓
7. Cluster Validation & Interpretation
   - Evaluate cluster quality
   - Analyze cluster characteristics
   - Create customer personas
   ↓
8. Business Insights & Recommendations
   - Actionable marketing strategies
   - Customer retention tactics
```

---

## 🤖 Clustering Algorithms

### 1. K-Means Clustering
**Purpose:** Partition customers into K distinct clusters
- **Pros:** Fast, scalable, easy to interpret
- **Cons:** Requires pre-specifying K, sensitive to outliers
- **Use Case:** General customer segmentation

### 2. Hierarchical Clustering
**Purpose:** Build a tree of clusters (dendrogram)
- **Pros:** No need to specify K upfront, visualizable hierarchy
- **Cons:** Computationally expensive for large datasets
- **Use Case:** Understanding customer hierarchy and relationships

### 3. DBSCAN (Density-Based Clustering)
**Purpose:** Find clusters based on density
- **Pros:** Finds arbitrary-shaped clusters, handles outliers
- **Cons:** Sensitive to parameter tuning
- **Use Case:** Identifying niche customer groups

### 4. Gaussian Mixture Models (GMM)
**Purpose:** Probabilistic clustering approach
- **Pros:** Soft clustering, handles overlapping clusters
- **Cons:** Assumes Gaussian distribution
- **Use Case:** Customers belonging to multiple segments

---

## ✨ Key Features

### Data Analysis
- **Comprehensive EDA** with distribution analysis
- **Customer lifetime value** calculation
- **RFM Analysis** (Recency, Frequency, Monetary)
- **Correlation heatmaps** for feature relationships
- **Outlier detection** using IQR and Z-score methods

### Feature Engineering
- Customer Age calculation from `Year_Birth`
- Total Spending = Sum of all product categories
- Total Purchases = Sum of all purchase channels
- Customer Tenure (days since enrollment)
- Purchase Frequency metrics
- Engagement scores based on web visits

### Clustering Techniques
- **Elbow Method** for optimal K selection
- **Silhouette Analysis** for cluster quality
- **Multiple algorithms comparison**
- **3D visualization** of clusters using PCA
- **Cluster profiling** with statistical summaries

### Business Insights
- Customer persona creation for each cluster
- Marketing recommendations per segment
- High-value customer identification
- At-risk customer detection
- Channel preference analysis

---

## 📈 Results & Insights

### Optimal Number of Clusters
> **Finding:** [Your optimal K value, e.g., "4 clusters identified using Elbow Method and Silhouette Score"]

### Cluster Performance Metrics

| Algorithm | Silhouette Score | Davies-Bouldin Index | Calinski-Harabasz Score |
|-----------|------------------|----------------------|-------------------------|
| K-Means | TBD | TBD | TBD |
| Hierarchical | TBD | TBD | TBD |
| DBSCAN | TBD | TBD | TBD |
| GMM | TBD | TBD | TBD |

> **Note:** Update these values after running your complete analysis

### Customer Segments Discovered

#### 🌟 Segment 1: [Name, e.g., "High-Value Loyalists"]
- **Size:** [X% of customers]
- **Characteristics:**
  - High spending across all categories
  - Frequent purchases
  - Low recency (recent buyers)
  - Prefer [channel preference]
- **Marketing Strategy:**
  - VIP rewards program
  - Exclusive early access to products
  - Premium customer service

#### 💼 Segment 2: [Name, e.g., "Budget-Conscious Shoppers"]
- **Size:** [X% of customers]
- **Characteristics:**
  - Moderate spending
  - High deal/discount usage
  - Price-sensitive
- **Marketing Strategy:**
  - Targeted discount campaigns
  - Bundle offers
  - Loyalty points program

#### 🔄 Segment 3: [Name, e.g., "Occasional Buyers"]
- **Size:** [X% of customers]
- **Characteristics:**
  - Low purchase frequency
  - High recency (haven't bought recently)
  - Lower engagement
- **Marketing Strategy:**
  - Re-engagement campaigns
  - Personalized product recommendations
  - Win-back offers

#### 🆕 Segment 4: [Name, e.g., "New/Exploratory Customers"]
- **Size:** [X% of customers]
- **Characteristics:**
  - Recent enrollments
  - Exploring product categories
  - Moderate spending
- **Marketing Strategy:**
  - Onboarding campaigns
  - Product education
  - First-purchase incentives

### Key Business Insights

1. **Revenue Concentration**
   - [X%] of revenue comes from [Y%] of customers (80/20 rule?)
   - High-value segment generates [Z] times more revenue per customer

2. **Channel Preferences**
   - Segment [X] prefers online shopping
   - Segment [Y] prefers in-store purchases
   - Catalog purchases dominated by [Z] segment

3. **Product Category Insights**
   - Wine purchases highest in [segment]
   - Meat products popular across [segments]
   - Sweet products correlate with [demographic feature]

4. **Risk Indicators**
   - [X%] of customers haven't purchased in 90+ days
   - Customers with complaints concentrated in [segment]
   - Website visits declining in [segment]

---

## 🚀 Installation & Usage

### Prerequisites
```bash
Python 3.8 or higher
pip package manager
```

### Clone the Repository
```bash
git clone https://github.com/AkshataJv/InsightCart.git
cd InsightCart
```

### Install Dependencies
```bash
pip install numpy pandas matplotlib seaborn scikit-learn plotly jupyter
```

### Run the Notebook
```bash
jupyter notebook InsightCart.ipynb
```

### Quick Start
```python
# Import required libraries
import pandas as pd
import numpy as np
from sklearn.cluster import KMeans
import matplotlib.pyplot as plt
import seaborn as sns

# Load the dataset
data = pd.read_csv('customer_data.csv')

# Follow the notebook for step-by-step analysis
# Each section includes detailed explanations and visualizations
```

---

## 📁 Project Structure

```
InsightCart/
│
├── InsightCart.ipynb         # Main Jupyter notebook with complete analysis
├── README.md                 # Project documentation (you are here!)
├── LICENSE                   # MIT License
│
├── data/                     # Dataset folder
│   └── customer_data.csv     # SmartCart customer data (2240 records)
│
├── models/                   # Saved model files (optional)
│   ├── kmeans_model.pkl
│   └── scaler.pkl
│
├── visualizations/           # Generated plots and charts
│   ├── elbow_curve.png
│   ├── silhouette_plots.png
│   ├── cluster_distribution.png
│   ├── pca_clusters_3d.png
│   └── dendrogram.png
│
├── reports/                  # Business insights reports
│   ├── customer_personas.pdf
│   └── segment_recommendations.pdf
│
└── requirements.txt          # Python dependencies
```

---

## 💡 Lessons Learned

### What Worked
- ✅ Feature engineering significantly improved cluster quality
- ✅ Combining multiple clustering algorithms provided robust validation
- ✅ RFM analysis aligned well with business understanding
- ✅ Dimensionality reduction (PCA) made visualization intuitive
- ✅ Silhouette analysis helped identify optimal cluster count

### Challenges Faced
- ❌ High-dimensional data required careful feature selection
- ❌ Outliers in income and spending skewed initial clusters
- ❌ Balancing cluster granularity vs. actionability
- ❌ Interpreting clusters in business terms required domain knowledge
- ❌ DBSCAN was sensitive to parameter tuning

### Key Takeaways
- **Data preprocessing is critical**: Scaling and outlier handling significantly impact results
- **No single "right" answer**: Clustering is exploratory; business context matters
- **Domain knowledge essential**: Technical clusters must translate to actionable segments
- **Validation is multifaceted**: Use multiple metrics to evaluate cluster quality
- **Visualization helps**: PCA/t-SNE makes high-dimensional clusters understandable
- **Iterate and refine**: First attempt rarely yields best segmentation

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://github.com/AkshataJv/InsightCart/issues).

### How to Contribute
1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add customer churn analysis'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- **SmartCart** (hypothetical e-commerce platform) for the business case
- **Scikit-learn community** for excellent clustering implementations
- **Kaggle** for inspiration and learning resources
- **Customer segmentation research papers** that guided this analysis
- Open-source data science community for tools and knowledge

---

## 📬 Contact

I'm actively learning data science and documenting the journey. Let's connect and learn together!

**Professional:**
- 💼 **LinkedIn:** [linkedin.com/in/akshata-jadhav-5b5611344](https://linkedin.com/in/akshata-jadhav-5b5611344)
- 💻 **GitHub:** [@AkshataJv](https://github.com/AkshataJv)
- 📧 **Email:** akshata.mjv@gmail.com

**Writing:**
- 📝 **Medium:** [medium.com/@akshata.mjv](https://medium.com/@akshata.mjv)

---

### 👩‍💻 About Me:

🎓 **BTech in AI & Data Science** at K.K. Wagh Institute, Nashik  
📚 **Currently Learning:** Python, Machine Learning, Data Analysis, Deep Learning  
🔭 **Working On:** Real-world data science projects, documenting the learning process  
💬 **Ask Me About:** My learning journey, fraud detection challenges, ML struggles  
⚡ **Fun Fact:** I debug models more than I write code, and that's okay!

---

### ✍️ What I Write About:

- The honest (messy) process of learning data science
- Dealing with imbalanced datasets (the struggle is real!)
- Mistakes I've made and how I fixed them
- Real project challenges and solutions

**Follow along if you're on a similar journey!**

---

## 📚 References & Resources

### Clustering & Segmentation
1. [Scikit-learn Clustering Documentation](https://scikit-learn.org/stable/modules/clustering.html)
2. [Customer Segmentation with Machine Learning](https://towardsdatascience.com/customer-segmentation)
3. [Evaluating Clustering Quality](https://scikit-learn.org/stable/modules/clustering.html#clustering-performance-evaluation)

### Business & Marketing
4. [RFM Analysis Guide](https://www.optimove.com/resources/learning-center/rfm-analysis)
5. [Customer Lifetime Value (CLV)](https://www.retentionscience.com/customer-lifetime-value/)
6. [Market Segmentation Strategies](https://www.marketingmag.com.au/hubs-c/market-segmentation/)

### Visualization
7. [Plotly for Python](https://plotly.com/python/)
8. [Seaborn Documentation](https://seaborn.pydata.org/)

---

<div align="center">

### 🎯 Project Status: Active Development

**Current Focus:** Optimizing cluster quality and developing actionable business insights

---

### ⭐ If you found this project helpful, please consider giving it a star!

**Made with lots of ☕ by Akshata**

</div>
