version https://git-lfs.github.com/spec/v1
oid sha256:746964cc7abdde0bc542065d8bb61198e64c1f00eca9d8b598e42f54ea52ad0a
size 2463

# GST Analytics Hackathon

This repository contains the solution for the GST Analytics Hackathon organized by the Government of India. The project focuses on analyzing GST data using machine learning techniques to predict and identify patterns in tax filing behavior.

## Project Overview

The solution implements a machine learning pipeline to analyze GST-related data with the following key components:

### Methodology

1. **Data Loading and Preprocessing**
   - Loading training and test datasets
   - Handling missing values using median imputation
   - Encoding categorical variables
   - Dataset alignment and consistency checks

2. **Model Architecture**
   - Implementation using scikit-learn Pipeline
   - Components:
     - Imputer for missing values
     - StandardScaler for feature normalization
     - Feature selection using RandomForest
     - RandomForestClassifier as the main predictive model

3. **Feature Engineering**
   - Automated feature selection using RandomForest importance
   - Standardization of numerical features
   - Label encoding for categorical variables

4. **Model Performance**
   - Training Metrics:
     - Accuracy: 97.10%
     - Precision: 97.50%
     - Recall: 97.10%
     - F1-score: 97.22%
     - AUC-ROC: 99.28%
   
   - Test Metrics:
     - Accuracy: 97.04%
     - Precision: 97.46%
     - Recall: 97.04%
     - F1-score: 97.16%
     - AUC-ROC: 99.25%

## Repository Structure

- `gov-dataanalytics-hackathon.ipynb`: Main notebook containing the analysis and model implementation
- `checksum.py`: Utility script for file integrity verification
- `push_lfs_files.py`: Script for handling large files using Git LFS
- `label_encoders.joblib`: Saved label encoders for categorical variables
- Various model artifacts and data files tracked with Git LFS

## Setup and Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/[username]/GST-Hackathon.git
   ```

2. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the notebook:
   ```bash
   jupyter notebook gov-dataanalytics-hackathon.ipynb
   ```

## File Verification

Use the checksum utility to verify file integrity:
```bash
python checksum.py [file_path] -a sha256
```

## Large File Storage

This repository uses Git LFS for managing large files. After cloning, run:
```bash
git lfs pull
```
