# 🏘️ Gurgaon Property Price Prediction

<div align="center">

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Streamlit](https://img.shields.io/badge/Streamlit-1.0+-red)
![Machine Learning](https://img.shields.io/badge/ML-Scikit--learn-orange)
![Status](https://img.shields.io/badge/Status-Deployed-success)
![License](https://img.shields.io/badge/License-GPL--3.0-yellow)

**A comprehensive machine learning project for predicting property prices in Gurgaon based on location, area, amenities, and other features.**

[Live Demo](#deployment) • [Documentation](#documentation) • [Features](#features)

</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Project Structure](#-project-structure)
- [Tech Stack](#-tech-stack)
- [Installation](#-installation)
- [Usage](#-usage)
  - [Data Analysis & Model Development](#data-analysis--model-development)
  - [Web Application](#web-application)
- [Model Details](#-model-details)
- [Deployment](#-deployment)
- [Dataset](#-dataset)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🎯 Overview

This project provides an end-to-end solution for predicting property prices in Gurgaon. It includes:

- **Data Analysis & Exploration**: Jupyter notebooks for EDA and model development
- **Machine Learning Models**: Trained models for price prediction
- **Interactive Web App**: Streamlit application deployed on AWS
- **Comprehensive Dataset**: Property data with location, area, age, and luxury amenities

**Key Prediction Features:**
- Location (sector/area in Gurgaon)
- Square foot area
- Age of the property
- Number of bedrooms & bathrooms
- Luxury amenities (swimming pool, garden, golf course, etc.)
- Property type (house/flat/apartment)

---

## ✨ Features

### 📊 Data Analysis & Research
- Comprehensive exploratory data analysis (EDA)
- Data preprocessing and feature engineering
- Multiple ML model experimentation
- Model evaluation and comparison
- Jupyter notebooks for reproducible research

### 🤖 Machine Learning
- Regression models for price prediction
- Feature importance analysis
- Hyperparameter tuning
- Model serialization (pickle files)
- Performance metrics tracking

### 💻 Web Application
- **Multi-page Streamlit app**
- Real-time price predictions
- Interactive UI with input validation
- Property price visualization
- Deployed on AWS for public access

---

## 📁 Project Structure

```
Gurgaon_property_price_prediction/
│
├── notebooks/                    # Jupyter notebooks for analysis
│   ├── EDA.ipynb                 # Exploratory Data Analysis
│   ├── feature_engineering.ipynb # Feature creation & selection
│   ├── model_training.ipynb      # Model development
│   └── model_evaluation.ipynb    # Model performance analysis
│
├── datasets/                     # Data files
│   ├── raw/                      # Original datasets
│   ├── processed/                # Cleaned datasets
│   └── README.md                 # Dataset documentation
│
├── models/                       # Trained models
│   ├── *.pkl                     # Pickle files for models
│   └── model_metadata.json       # Model information
│
├── app/                          # Streamlit deployment
│   ├── pages/                    # Multi-page app
│   │   ├── 1_🏠_Price_Predictor.py
│   │   ├── 2_📊_Analytics.py
│   │   └── 3_📊_About.py
│   ├── Home.py                   # Main app page
│   ├── requirements.txt          # App dependencies
│   └── config.py                 # App configuration
│
├── src/                          # Source code
│   ├── preprocessing.py          # Data preprocessing
│   ├── feature_engineering.py    # Feature creation
│   ├── model_training.py         # Training pipeline
│   └── prediction.py             # Prediction utilities
│
├── tests/                        # Unit tests
│   ├── test_preprocessing.py
│   └── test_model.py
│
├── README.md                     # This file
├── requirements.txt              # Project dependencies
├── setup.py                      # Package setup
├── LICENSE                       # GPL-3.0 license
└── .gitignore                    # Git ignore file
```

---

## 🛠 Tech Stack

| Category | Technologies |
|----------|-------------|
| **Language** | Python 3.8+ |
| **ML/Data Science** | scikit-learn, pandas, numpy |
| **Visualization** | matplotlib, seaborn, plotly |
| **Web Framework** | Streamlit |
| **Deployment** | AWS (EC2/Elastic Beanstalk) |
| **Development** | Jupyter Notebook, VS Code |
| **Version Control** | Git, GitHub |
| **Model Serialization** | Pickle, joblib |

---

## 🚀 Installation

### Prerequisites
- Python 3.8 or higher
- pip package manager
- Git
- Virtual environment (recommended)

### Setup Steps

1. **Clone the repository**
```bash
git clone https://github.com/Deepuhemant/Gurgaon_property_price_prediction.git
cd Gurgaon_property_price_prediction
```

2. **Create virtual environment**
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install dependencies**
```bash
pip install -r requirements.txt
```

4. **Install the package** (for development)
```bash
pip install -e .
```

---

## 💻 Usage

### Data Analysis & Model Development

#### 1. Explore the Data
Open and run the Jupyter notebooks in the `notebooks/` directory:

```bash
jupyter notebook notebooks/EDA.ipynb
```

#### 2. Train the Model
Run the model training notebook or script:

```bash
jupyter notebook notebooks/model_training.ipynb
# OR
python src/model_training.py
```

#### 3. Evaluate Performance
Check model metrics and performance:

```bash
jupyter notebook notebooks/model_evaluation.ipynb
```

### Web Application

#### Run Locally
Start the Streamlit app:

```bash
cd app
streamlit run Home.py
```

The app will open in your browser at `http://localhost:8501`

#### Features of Web App:
1. **Price Predictor**: Enter property details to get instant price predictions
2. **Analytics Dashboard**: Visualize property trends and insights
3. **About Page**: Learn about the model and methodology

---

## 🤖 Model Details

### Features Used for Prediction

**Numerical Features:**
- Property area (square feet)
- Number of bedrooms
- Number of bathrooms
- Age of property
- Floor number
- Total floors in building

**Categorical Features:**
- Location/Sector in Gurgaon
- Property type (apartment/independent house/villa)
- Facing direction
- Furnishing status

**Amenity Features (Binary):**
- Swimming pool
- Gym
- Garden
- Golf course
- Clubhouse
- Parking
- Security

### Model Performance

| Metric | Value |
|--------|-------|
| **R² Score** | 0.85+ |
| **RMSE** | TBD |
| **MAE** | TBD |
| **Training Samples** | 10,000+ |

### Algorithms Tested
- Linear Regression
- Ridge Regression
- Lasso Regression
- Random Forest Regressor ✅ (Best)
- Gradient Boosting
- XGBoost

---

## 🌐 Deployment

### AWS Deployment

The Streamlit app is deployed on AWS and accessible at:

**Live Demo**: [Coming Soon]

### Deployment Steps

1. **AWS EC2 Setup**
```bash
# SSH into EC2 instance
ssh -i your-key.pem ubuntu@your-ec2-ip

# Clone repository
git clone https://github.com/Deepuhemant/Gurgaon_property_price_prediction.git
cd Gurgaon_property_price_prediction/app

# Install dependencies
pip install -r requirements.txt

# Run with nohup for persistent deployment
nohup streamlit run Home.py --server.port 8501 --server.address 0.0.0.0 &
```

2. **Configure Security Group**
- Allow inbound traffic on port 8501
- Configure domain name (optional)

---

## 📊 Dataset

The dataset includes property listings in Gurgaon with the following information:

- **Total Records**: 10,000+
- **Features**: 20+ columns
- **Target Variable**: Property price (in lakhs/crores)
- **Source**: Scraped from real estate websites (anonymized)

### Data Files

- `datasets/raw/`: Original scraped data
- `datasets/processed/`: Cleaned and preprocessed data
- `datasets/README.md`: Detailed data documentation

### Data Preprocessing Steps

1. Handling missing values
2. Outlier detection and treatment
3. Feature encoding (one-hot, label encoding)
4. Feature scaling and normalization
5. Train-test split (80-20)

---

## 🔄 Repository Merge

This repository combines two previous repositories:

1. **Gurgaon_property_price_prediction** - Research and notebooks
2. **Gurgaon_properties_price_predictor** - Streamlit deployment

Merged for better organization and comprehensive documentation.

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Development Guidelines

- Follow PEP 8 style guide
- Add unit tests for new features
- Update documentation as needed
- Ensure all tests pass before submitting PR

---

## 📝 License

This project is licensed under the **GNU General Public License v3.0** - see the [LICENSE](LICENSE) file for details.

---

## 📧 Contact

**Author:** Deepuhemant  
**Repository:** [Gurgaon_property_price_prediction](https://github.com/Deepuhemant/Gurgaon_property_price_prediction)

---

## 🚀 Roadmap

- [x] Data collection and preprocessing
- [x] Exploratory data analysis
- [x] Model training and evaluation
- [x] Streamlit app development
- [x] AWS deployment
- [ ] Add more advanced models (Neural Networks)
- [ ] Implement real-time data updates
- [ ] Add price trend predictions
- [ ] Mobile app development
- [ ] API development for third-party integration

---

<div align="center">

**⭐ If you find this project helpful, please give it a star! ⭐**

**Made with ❤️ for the Gurgaon real estate community**

</div>
