# 🔀 Repository Merge Guide

## Overview

This guide will help you complete the merge of two Gurgaon Property Price Prediction repositories:

1. **Gurgaon_property_price_prediction** - Research notebooks and data
2. **Gurgaon_properties_price_predictor** - Streamlit deployment app

**Goal**: Combine both into a single, well-organized repository.

---

## ✅ Completed Steps

- [x] Created comprehensive README.md
- [x] Documented project structure
- [x] Defined merge strategy

---

## 🛠️ Steps to Complete the Merge

### Prerequisites

Before starting, ensure you have:
- Git installed on your machine
- GitHub account access
- Basic knowledge of git commands
- Terminal/Command Prompt access

### Step 1: Clone Both Repositories

```bash
# Create a working directory
mkdir gurgaon_merge
cd gurgaon_merge

# Clone the first repository (this one - with the new README)
git clone https://github.com/Deepuhemant/Gurgaon_property_price_prediction.git

# Clone the second repository
git clone https://github.com/Deepuhemant/Gurgaon_properties_price_predictor.git
```

### Step 2: Create New Folder Structure

```bash
# Navigate to the first repository
cd Gurgaon_property_price_prediction

# Create the new folder structure
mkdir -p notebooks
mkdir -p models
mkdir -p app/pages
mkdir -p src
mkdir -p tests
```

### Step 3: Organize Existing Files

```bash
# Move Jupyter notebook files to notebooks folder
mv Jupyter_python_file/* notebooks/ 2>/dev/null || true

# Rename folders for clarity
mv Pickle_files models/

# Organize datasets
# Keep the Datasets folder as is, or rename to datasets (lowercase)
mv Datasets datasets || true
mv Preprocessed_datasets_csv datasets/processed_csv || true
mv Preprocessed_datasets_excel datasets/processed_excel || true
```

### Step 4: Copy Streamlit App Files

```bash
# Go back to parent directory
cd ..

# Copy Streamlit app files from second repository
cp -r Gurgaon_properties_price_predictor/pages Gurgaon_property_price_prediction/app/
cp Gurgaon_properties_price_predictor/Home.py Gurgaon_property_price_prediction/app/
cp Gurgaon_properties_price_predictor/requirements.txt Gurgaon_property_price_prediction/app/

# Copy LICENSE if not already present
cp Gurgaon_properties_price_predictor/LICENSE Gurgaon_property_price_prediction/ 2>/dev/null || true
```

### Step 5: Handle Duplicate Files

```bash
cd Gurgaon_property_price_prediction

# Check for duplicate datasets
# Compare files in both Datasets folders and keep the most recent/complete version
# You may need to manually verify which files to keep

# Merge Pickle_files if there are models in both repositories
# Keep the best-performing model
```

### Step 6: Create requirements.txt (Root Level)

Create a comprehensive `requirements.txt` at the root level:

```bash
# Create/edit requirements.txt
nano requirements.txt
```

Add these dependencies:

```txt
# Data Science Libraries
pandas>=1.3.0
numpy>=1.21.0
scikit-learn>=1.0.0
matplotlib>=3.4.0
seaborn>=0.11.0
plotly>=5.0.0

# Web Framework
streamlit>=1.10.0

# Utilities
joblib>=1.0.0
pickle5>=0.0.11
python-box>=6.0.0
pyYAML>=6.0

# Jupyter
jupyter>=1.0.0
ipykernel>=6.0.0

# Development
pytest>=7.0.0
black>=22.0.0
flake8>=4.0.0
```

### Step 7: Create .gitignore

```bash
# Create .gitignore file
nano .gitignore
```

Add:

```
# Python
__pycache__/
*.py[cod]
*$py.class
*.so
.Python
env/
venv/
ENV/

# Jupyter Notebook
.ipynb_checkpoints

# Distribution / packaging
build/
dist/
*.egg-info/

# IDEs
.vscode/
.idea/
*.swp
*.swo
*~

# OS
.DS_Store
Thumbs.db

# Data files (optional - uncomment if datasets are too large)
# *.csv
# *.xlsx
# *.zip

# Models (optional - uncomment if models are too large)
# *.pkl
# *.h5
# *.model
```

### Step 8: Create setup.py

```bash
# Create setup.py for package installation
nano setup.py
```

Add:

```python
from setuptools import setup, find_packages

setup(
    name="gurgaon-property-price-prediction",
    version="1.0.0",
    author="Deepuhemant",
    description="Gurgaon Property Price Prediction ML Project",
    packages=find_packages(),
    install_requires=[
        "pandas>=1.3.0",
        "numpy>=1.21.0",
        "scikit-learn>=1.0.0",
        "streamlit>=1.10.0",
    ],
    python_requires=">=3.8",
)
```

### Step 9: Commit and Push Changes

```bash
# Stage all changes
git add .

# Commit with descriptive message
git commit -m "refactor: Reorganize repository structure and merge Streamlit app

- Moved Jupyter notebooks to notebooks/ folder
- Organized models in models/ folder
- Added Streamlit app in app/ folder
- Created comprehensive folder structure
- Merged files from Gurgaon_properties_price_predictor
- Added setup.py and updated requirements.txt"

# Push to GitHub
git push origin main
```

### Step 10: Verify and Test

```bash
# Test Streamlit app
cd app
streamlit run Home.py

# Test Jupyter notebooks
cd ../notebooks
jupyter notebook

# Install package in development mode
cd ..
pip install -e .
```

---

## 📋 Final Folder Structure

After completing all steps, your repository should look like:

```
Gurgaon_property_price_prediction/
├── notebooks/
│   ├── EDA.ipynb
│   ├── feature_engineering.ipynb
│   ├── model_training.ipynb
│   └── model_evaluation.ipynb
├── datasets/
│   ├── raw/
│   └── processed/
├── models/
│   └── *.pkl
├── app/
│   ├── pages/
│   ├── Home.py
│   └── requirements.txt
├── src/
│   ├── preprocessing.py
│   ├── model_training.py
│   └── prediction.py
├── tests/
├── README.md
├── MERGE_GUIDE.md (this file)
├── requirements.txt
├── setup.py
├── .gitignore
└── LICENSE
```

---

## 🛡️ Troubleshooting

### Issue: Git conflicts during merge
**Solution**: Use `git status` to see conflicts, resolve manually, then `git add` and `git commit`

### Issue: File path too long (Windows)
**Solution**: Enable long paths: `git config --system core.longpaths true`

### Issue: Permission denied when copying files
**Solution**: Use `sudo` on Linux/Mac, or run terminal as Administrator on Windows

### Issue: Streamlit app won't run
**Solution**: Check if all pickle files are in the correct location and requirements are installed

---

## ♻️ Cleaning Up

After successful merge, you can:

1. **Archive the second repository** (Gurgaon_properties_price_predictor)
   - Go to repository Settings
   - Scroll to "Danger Zone"
   - Click "Archive this repository"

2. **Or delete it** if no longer needed
   - Go to repository Settings
   - Scroll to "Danger Zone"
   - Click "Delete this repository"
   - Type the repository name to confirm

3. **Update repository description**
   - Update the "About" section to reflect the merged nature

---

## ❓ Need Help?

If you encounter issues:
1. Check the [README.md](README.md) for more information
2. Review git documentation
3. Create an issue in this repository

---

**Good luck with the merge! 🚀**

*Last updated: November 26, 2025*
