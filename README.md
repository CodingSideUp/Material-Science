# Material-Science

## Overview
This repository contains all project files, Jupyter notebooks, and reports developed for the **Material Science Machine Learning project**.  
The work focuses on **predicting material properties (bandgap in my case)** and **automating feature extraction**, and provides **a framework to compare the performance of a traditional ML regressor (XGBoost) vs. a graph neural network (CGCNN)**.  
Model performance is reported using **MSE, MAE, and R²**.

You will also find my **thesis report** submitted at **SRH Hochschule Heidelberg** (Department of Information, Medien und Design).

---

## Repository Structure
```
Material-Science/
├── Dataset/                # Raw and processed data files
├── notebooks/              # Jupyter notebooks for data processing & modeling
│   ├── Data_collection.ipynb
│   ├── atomic_data.ipynb
│   ├── EDA_XGB_latest.ipynb
│   └── CGCNN_final.ipynb
├── Thesis-report/          # Project thesis report and documentation
│   └── ADSA_Thesis_Gurudarshan_Nagaraju.pdf
├── best_model.pt           # Trained CGCNN model (excluded if using .gitignore)
├── requirements.txt        # List of required Python packages
├── .gitattributes          # Git LFS tracking info
└── README.md               # Project overview and instructions
```

## Dataset:
[Link to download the QMOF dataset](https://figshare.com/articles/dataset/QMOF_Database/13147324)

## Setup Instructions

### Step 1: Create Environment

conda create -n matsci python=3.10 -y
conda activate matsci


### Step 2: Install Dependencies

pip install -r requirements.txt


### Step 3: Install Torch + PyTorch Geometric (GPU)

pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121

pip install torch-geometric torch-scatter torch-sparse torch-cluster -f https://data.pyg.org/whl/torch-2.3.0+cu121.html


## Notebooks Overview
```
Notebooks and their Description:

Data_collection.ipynb: Collects and computes geometry and porosity features from the QMOF dataset.
atomic_data.ipynb: Aggregates atom-site DFT data and merges with geometric features.
EDA_XGB_latest.ipynb: Exploratory data analysis and XGBoost regression for bandgap prediction.
CGCNN_final.ipynb: Trains a Crystal Graph Convolutional Neural Network (CGCNN) for bandgap prediction.
```

## Results Summary
```
Achieved R² ≈ 0.71 with the CGCNN model.
Improved bandgap prediction using hybrid feature sets (geometry + atom-site DFT data).
Developed interpretable models using SHAP for feature importance.
```

## Tools & Libraries Used
```
Python, Jupyter Notebook
scikit-learn, XGBoost
PyTorch, PyTorch Geometric
pandas, numpy, matplotlib, seaborn
pymatgen, rdkit
```

## Author:

**Gurudarshan Nagaraju**
**MSc. in Applied Data Science and Analytics – SRH Hochschule, Heidelberg**
[LinkedIn](https://www.linkedin.com/in/gurudarshan-b-n-4b3b919b/)
