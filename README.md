# \ud83c\udfnf Gurgaon Property Price Prediction

[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Streamlit](https://img.shields.io/badge/framework-Streamlit-FF4B4B.svg)](https://streamlit.io/)
[![Scikit-learn](https://img.shields.io/badge/ML-scikit--learn-F7931E.svg)](https://scikit-learn.org/)
[![AWS](https://img.shields.io/badge/deployment-AWS-FF9900.svg)](https://aws.amazon.com/)
[![License: GPL-3.0](https://img.shields.io/badge/License-GPL--3.0-yellow.svg)](https://opensource.org/licenses/GPL-3.0)
[![Status](https://img.shields.io/badge/status-deployed-brightgreen.svg)]()

A comprehensive ML project for predicting property prices in Gurgaon. Features data analysis, trained ML models, and a production Streamlit web app deployed on AWS.

## \ud83c\udf3f Overview

End-to-end solution combining:
- Comprehensive data analysis with Jupyter notebooks
- Multiple ML models for price prediction
- Interactive multi-page Streamlit web application
- Production deployment on AWS EC2

**Key Highlights:**
- \u2705 Data preprocessing pipeline
- \u2705 ML model experimentation (Linear, Ridge, Lasso, Random Forest, XGBoost)
- \u2705 Multi-page Streamlit web app
- \u2705 AWS deployment
- \u2705 Model serialization with pickle
- \u2705 R\u00b2 Score 0.85+

## \u2728 Features

**Data Analysis:**
- Comprehensive EDA
- Feature engineering
- Model experimentation
- Performance tracking

**Machine Learning:**
- Regression models
- Feature importance
- Hyperparameter tuning
- Model serialization

**Web Application:**
- Multi-page Streamlit app
- Real-time predictions
- Interactive UI
- Analytics dashboard
- AWS deployment

## \ud83d\udd27 Tech Stack

| Category | Technologies |
|----------|---------------|
| Language | Python 3.8+ |
| ML/Data | scikit-learn, pandas, numpy |
| Visualization | matplotlib, seaborn, plotly |
| Web | Streamlit |
| Deployment | AWS EC2 |
| Serialization | Pickle, joblib |

## \ud83d\ude80 Quick Start

**Clone & Setup:**
```bash
git clone https://github.com/Deepuhemant/Gurgaon_property_price_prediction.git
cd Gurgaon_property_price_prediction
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

**Run Web App:**
```bash
cd app
streamlit run Home.py
```

Access at: `http://localhost:8501`

## \ud83e\udd16 Model Details

**Algorithms:**
- Linear Regression
- Ridge Regression
- Lasso Regression  
- Random Forest \u2705 (Best)
- Gradient Boosting
- XGBoost

**Performance:**
- R\u00b2 Score: 0.85+
- Training Samples: 10,000+
- Features: 20+

## \ud83c\udf10 AWS Deployment

```bash
ssh -i key.pem ubuntu@ec2-ip
git clone <repo>
cd app
pip install -r requirements.txt
nohup streamlit run Home.py --server.port 8501 &
```

## \ud83d\udccc Dataset

- Records: 10,000+
- Features: 20+
- Source: Real estate websites
- Preprocessed & ready for ML

## \ud83d\udc4b Contributing

1. Fork repository
2. Create feature branch
3. Commit changes
4. Push & open PR

## \ud83d\udcc4 License

GNU General Public License v3.0

## \ud83d\udce7 Contact

**Author:** Deepuhemant

**Repo:** [Gurgaon_property_price_prediction](https://github.com/Deepuhemant/Gurgaon_property_price_prediction)

---

**\u2b50 Star this project if it helps! \u2b50**

**Made with \u2764\ufe0f for Gurgaon real estate**
