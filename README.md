```markdown
# 🤖 Machine Learning & Data Science Portfolio (DS-ML-TASKS)

### Python • Scikit-Learn • Pandas • Matplotlib • Tkinter

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)
![Seaborn](https://img.shields.io/badge/Seaborn-444876?style=for-the-badge&logo=seaborn&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626.svg?style=for-the-badge&logo=Jupyter&logoColor=white)

Welcome to my **Data Science and Machine Learning** repository! This repository showcases my daily contributions, mini-projects, and comprehensive assignments covering end-to-end data science workflows — from data preprocessing and exploratory data analysis (EDA) to model training, evaluation, and interactive GUI applications.

🌐 **Check out my Portfolio:** [sabarishdev.netlify.app](https://sabarishdev.netlify.app/)

---

## 📖 Table of Contents

- [ML Pipeline Architecture](#-ml-pipeline-architecture)
- [Tech Stack](#-tech-stack)
- [Project Walkthrough](#-project-walkthrough)
  - [Unsupervised Learning & Clustering](#1-unsupervised-learning--clustering)
  - [Classification & NLP](#2-classification--nlp)
  - [Regression Models](#3-regression-models)
- [Getting Started](#-getting-started)
- [Repository Structure](#-repository-structure)
- [Roadmap](#-roadmap)
- [License](#-license)
- [Author](#-author)

---

## 🏗️ ML Pipeline Architecture

The projects in this repository follow a standard Data Science lifecycle. Interactive GUIs (built with Tkinter/PyQt) act as the client interface for users to input data and receive real-time predictions.

```mermaid
graph TD
    Data[🗄️ Raw Datasets] --> Preprocessing[⚙️ Data Preprocessing & Cleaning]
    
    subgraph Feature Engineering [🛠️ Feature Engineering]
        Scaling[Normalization / Standardization]
        Encoding[Label / One-Hot Encoding]
        PCA[PCA / Dimensionality Reduction]
    end
    
    Preprocessing --> Feature Engineering
    
    Feature Engineering --> ModelSelection[🤖 Model Selection]
    
    subgraph ML Models [🧠 Machine Learning Models]
        Clustering[Clustering: K-Medoids, DBSCAN, Hierarchical]
        Classification[Classification: Naive Bayes, Logistic Regression]
        Regression[Regression: Simple & Multiple Linear]
        NLP[NLP: Text Classification, Sentiment Analysis]
    end
    
    ModelSelection --> ML Models
    
    ML Models --> Evaluation[📊 Model Evaluation]
    Evaluation --> |Accuracy, R2 Score, Silhouette| Deployment[🚀 Deployment]
    
    Deployment --> GUI[💻 Interactive GUI / Visualization]

    classDef data fill:#f9d0c4,stroke:#333,stroke-width:2px;
    classDef process fill:#d4e157,stroke:#333,stroke-width:2px;
    classDef model fill:#81d4fa,stroke:#333,stroke-width:2px;
    classDef deploy fill:#ffcc80,stroke:#333,stroke-width:2px;
    
    class Data data;
    class Preprocessing,ModelSelection process;
    class Clustering,Classification,Regression,NLP model;
    class Evaluation,GUI deploy;
```

---

## 🛠️ Tech Stack

| Layer | Technology |
| --- | --- |
| **Language** | Python 3.x |
| **Data Manipulation** | Pandas, NumPy |
| **Machine Learning** | Scikit-Learn (Sklearn) |
| **Data Visualization** | Matplotlib, Seaborn |
| **Natural Language Processing** | NLTK, WordCloud, Regex |
| **GUI Frameworks** | Tkinter, Jupyter Notebook (Colab UI) |
| **Environment** | Jupyter Notebook, VS Code |

---

## ✨ Project Walkthrough

Here is a showcase of the core Machine Learning paradigms covered in this repository.

### 1. Unsupervised Learning & Clustering

Projects focused on discovering hidden patterns in unlabeled data.

#### 🔍 Hierarchical Clustering (Malware Analysis)
Dendrograms showing both agglomerative (bottom-up) and divisive (top-down) clustering to group malware families based on their behavioral features.
| Agglomerative Clustering | Divisive Clustering |
| :---: | :---: |
| ![Agglomerative Dendrogram](./images/agg_dendrogram.png) | ![Divisive Dendrogram](./images/div_dendrogram.png) |

#### 📍 DBSCAN Clustering (Donation Data)
A density-based spatial clustering map analyzing donor behavior based on Recency (V1) and Frequency (V2). The model successfully identifies noise/outliers (red 'X') vs core clusters.
![DBSCAN Clustering](./images/dbscan.png)

#### 📦 Amazon Product Segmentation (K-Medoids)
A GUI application and scatter plot that segments Amazon products into categories (Budget, Mid-Range, Premium) based on discounted price and ratings using K-Medoids clustering.
| Clustering Map | Predictor Interface |
| :---: | :---: |
| ![Amazon Clusters](./images/amazon_clusters.png) | ![K-Medoids GUI](./images/kmedoids_gui.png) |

#### 🧬 PCA - Breast Cancer Wisconsin Dataset
Principal Component Analysis (PCA) applied to reduce high-dimensional medical data into 2 principal components, clearly visualizing the separation between malignant and benign tumors.
![PCA Breast Cancer](./images/pca_breast_cancer.png)

---

### 2. Classification & NLP

Supervised learning models predicting discrete categories, including text analysis.

#### 🏥 Gaussian Naive Bayes - Heart Disease Predictor
A medical prediction GUI application that predicts heart disease based on clinical parameters. It features an interactive form and is accompanied by a Pearson correlation heatmap for feature analysis.
| Correlation Heatmap | Predictor GUI |
| :---: | :---: |
| ![Heart Disease Heatmap](./images/heart_heatmap.png) | ![Heart Disease GUI](./images/heart_gui.png) |

#### 📝 Text Classification (NLP)
A GUI application classifying text as *Poetic* or *Normal*, displaying confidence scores and recognized vocabulary. Also included are word clouds representing three distinct text categories (Space, Baseball, Graphics) after text cleaning.
| Poetic vs Normal Classifier | Text Category Word Clouds |
| :---: | :---: |
| ![Text Classifier](./images/text_classifier.png) | ![Word Clouds](./images/wordclouds.png) |

#### 🎬 Sentiment Analysis - Movie Reviews
A session tracker application that predicts whether a user-inputted movie review is positive or negative. It visualizes the distribution of predictions across a user session.
![Sentiment Analysis](./images/sentiment_analysis.png)

#### 🛒 Logistic Regression - Sales Classifier
A model predicting the probability of a product achieving High vs Low/Med sales. The GUI outputs the predicted class alongside a probability bar chart.
![Logistic Regression](./images/logistic_regression.png)

---

### 3. Regression Models

Supervised learning models predicting continuous numerical values.

#### 📈 Multiple Linear Regression - Sales Predictor
A robust prediction model utilizing multiple features (Price, Quantity, Discount) to forecast Total Sales. Includes an Actual vs. Predicted scatter plot showing the line of best fit.
![Multiple Linear Regression](./images/multiple_regression.png)

#### 💸 Simple Linear Regression - Flipkart Sales Predictor
A foundational model predicting Total Sales based solely on Price. The visualization demonstrates the linear relationship between price and total sales with a plotted regression line.
![Simple Linear Regression](./images/simple_regression.png)

---

## 🚀 Getting Started

### Prerequisites

- **Python 3.8+**
- **Jupyter Notebook** (to run the `.ipynb` files)
- **Pip** package manager

### Installation & Usage

**1. Clone the repository**

```bash
git clone https://github.com/SabarishMS123/DS-ML-TASKS.git
cd DS-ML-TASKS
```

**2. Install Dependencies**

Install the required libraries used across the notebooks:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn nltk wordcloud
```

**3. Run the Notebooks**

Launch Jupyter Notebook or upload the `.ipynb` files to Google Colab to explore the tasks and models:

```bash
jupyter notebook
```

---

## 📁 Repository Structure

Here is an overview of the tasks and projects present in this repository:

```
DS-ML-TASKS/
├── MINI PROJECT WEEK 1/         # Initial data exploration tasks
├── MINI PROJECT WEEK2/          
├── MINI PROJECT 3/              # Core ML algorithms
├── MINI PROJECT 4/              # Gaussian Naive Bayes
├── MINI PROJECT 5/              
├── MINI PROJECT 6/              # KNN Algorithm implementation
├── mini project 7/              # Decision Tree Regressor & Classifier
├── ML WEEKLY PROJECT 8/         
├── MINI project 9/              
├── Mini project 10/             
├── MINI PROJECT 11/             
├── ML PROJECT 12/               # Random Forest Regressor & Classifier
├── ML MINI PROJECT 13 WEBSCRAPPING/  # Web Scraping with DS/ML
├── ml project 14/               
├── Data Preprocessing Tasks/
│   ├── DISTRIBUITION_TASKS.ipynb
│   ├── MATPLOTLIB TASKS.ipynb
│   ├── NUMPY TASKS.ipynb
│   ├── PANDAS TASK.ipynb
│   ├── REGEX TASKS.ipynb
│   ├── SKEWNESS AND KURTOSIS TASKS.ipynb
│   └── kurtosis EXPLORATION.ipynb
├── AGRI DATASET.csv             # Sample dataset used in projects
└── README.md
```

---

## 🗺️ Roadmap

- [ ] Add Deep Learning models (TensorFlow/PyTorch) for image classification.
- [ ] Containerize the GUI applications using Streamlit for web deployment.
- [ ] Implement cross-validation and hyperparameter tuning (GridSearchCV) for all models.
- [ ] Deploy the models as REST APIs using FastAPI.

---

## 📄 License

**© All Rights Reserved.**

This project and its source code are the intellectual property of the author. Unauthorized copying, modification, or distribution of this project, via any medium, is strictly prohibited without prior written permission.

---

## 👨‍💻 Author

**Sabarish M S**

📍 Salem, Tamil Nadu, India

- GitHub: [@SabarishMS123](https://github.com/SabarishMS123)
- Portfolio: [sabarishdev.netlify.app](https://sabarishdev.netlify.app/)
- LinkedIn: [sabarish-m-s](https://linkedin.com/in/sabarish-m-s/)

---

## 🙏 Acknowledgements

- [Scikit-Learn Documentation](https://scikit-learn.org/stable/)
- [Matplotlib Gallery](https://matplotlib.org/stable/gallery/index.html)
- [Seaborn Tutorial](https://seaborn.pydata.org/tutorial.html)
- [NLTK Book](https://www.nltk.org/book/)

---

⭐ If you found these projects helpful, consider giving this repository a star!
```
