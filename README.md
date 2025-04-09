# Worker Welfare in Indonesia - Machine Learning Project

## Overview

This project analyzes worker welfare in Indonesia using machine learning techniques, focusing on economic indicators from multiple datasets. The analysis combines clustering to identify patterns and classification to predict welfare groups based on key economic factors.

The project examines relationships between minimum wage policies, poverty lines, average wages, and spending patterns across different provinces and regions in Indonesia.

## Table of Contents

- Project Structure
- Datasets
- Features
- Methodology
- Key Findings
- Model Performance
- Technical Implementation
- Installation
- Usage
- Contribution

## Project Structure

This project consists of two main components:

1. **Clustering Analysis** (Clustering_Submission_BMLP.ipynb)
   - Explores underlying patterns in worker welfare data
   - Identifies distinct economic groupings across Indonesian provinces
   - Creates labeled clusters for classification

2. **Classification Analysis** (Klasifikasi_Submission_BMLP.ipynb)
   - Predicts cluster membership using various ML algorithms
   - Compares performance of multiple classification techniques
   - Identifies key features that determine economic groupings

## Datasets

The project utilizes four primary datasets:

- **rataRataUpah.csv**: Average hourly wages across different provinces and years
- **minUpah.csv**: Provincial minimum wage data
- **garisKemiskinan.csv**: Poverty line thresholds by province, period, and area type
- **pengeluaran.csv**: Per-capita expenditure by province and area type

## Features

Key features analyzed in this project include:

- **upah**: Average hourly wage
- **ump**: Provincial minimum wage
- **gk**: Poverty line threshold
- **peng**: Per-capita expenditure
- **daerah**: Area type (urban/rural)
- **jenis**: Expenditure type (food/non-food)
- **provinsi**: Province in Indonesia
- **tahun**: Year of data collection

## Methodology

### Clustering Approach

1. **Data Preprocessing**
   - Missing value imputation using KNN
   - Feature encoding for categorical variables
   - Normalization using MinMax scaling

2. **Clustering Algorithms Comparison**
   - KMeans
   - Hierarchical (Agglomerative)
   - DBSCAN

3. **Optimal Cluster Selection**
   - Using silhouette scores and elbow method
   - Identified 9 distinct economic clusters

### Classification Approach

1. **Model Selection**
   - Random Forest Classifier
   - Support Vector Machine
   - Gradient Boosting Classifier

2. **Hyperparameter Tuning**
   - Grid search for Random Forest and SVM
   - Randomized search for Gradient Boosting

3. **Model Evaluation**
   - Accuracy, F1-Score, Precision, Recall
   - Confusion matrices
   - Feature importance analysis

## Key Findings

1. **High minimum wages don't always increase purchasing power**
   - Some clusters show high UMP but low expenditure levels
   - Other factors like job availability and prices have stronger influence

2. **Higher poverty lines correlate with higher purchasing power**
   - Areas with higher GK generally have higher expenditure
   - Reflects regional cost of living differences

3. **Urban-rural divide is significant**
   - Urban areas show distinct spending patterns compared to rural areas
   - Expenditure to poverty line ratios differ significantly by region type

4. **Economic policy implications**
   - Simply increasing minimum wages may not improve welfare
   - Need integrated approaches addressing inflation and economic access

## Model Performance

### Clustering Results

- **Best Model**: KMeans with 9 clusters
- **Silhouette Score**: 0.719
- **Distinctiveness**: Clear separation between economic groups

### Classification Results

| Model | Accuracy | F1-Score | Precision | Recall |
|-------|----------|----------|-----------|--------|
| Random Forest | 1.0 | 1.0 | 1.0 | 1.0 |
| SVM | 1.0 | 1.0 | 1.0 | 1.0 |
| Gradient Boosting | 1.0 | 1.0 | 1.0 | 1.0 |
| RF (Tuned) | 1.0 | 1.0 | 1.0 | 1.0 |
| SVM (Tuned) | 1.0 | 1.0 | 1.0 | 1.0 |
| GB (Tuned) | 1.0 | 1.0 | 1.0 | 1.0 |

**Note**: The perfect classification performance suggests the clusters are highly distinguishable based on the selected features.

## Technical Implementation

### Libraries Used

- **Data Manipulation**: Pandas, NumPy
- **Visualization**: Matplotlib, Seaborn
- **Machine Learning**: Scikit-learn
- **Clustering**: KMeans, AgglomerativeClustering, DBSCAN
- **Classification**: RandomForestClassifier, SVC, GradientBoostingClassifier
- **Evaluation**: Silhouette score, confusion matrices, classification reports

### Visualization Techniques

- PCA for dimension reduction and cluster visualization
- Feature importance plots
- Silhouette analysis
- Confusion matrices
- Comparative metric bar charts

## Installation

```bash
# Clone the repository
git clone https://github.com/maybeitsai/social-welfare-pattern-analysis
cd social-welfare-pattern-analysis

# Create and activate virtual environment (recommended)
python -m venv venv
# On Windows
venv\Scripts\activate
# On macOS/Linux
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt
```

## Usage

1. **Data Preparation**
   - Place datasets in the data directory
   - Ensure all CSV files are present

2. **Run Clustering Analysis**
   ```bash
   jupyter notebook "[Clustering]_Submission_Akhir_BMLP_Harry Mardika.ipynb"
   ```

3. **Run Classification Analysis**
   ```bash
   jupyter notebook "[Klasifikasi]_Submission_Akhir_BMLP_HarryMardika.ipynb"
   ```

4. **Generated Outputs**
   - Trained models
   - Clustering results in hasil_clustering_final.csv
   - Classification dataset in train.csv

## Contribution

This project was developed as part of a Machine Learning Beginner Project. Contributions and improvements are welcome:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/improvement`)
3. Commit your changes (`git commit -m 'Add some improvement'`)
4. Push to the branch (`git push origin feature/improvement`)
5. Open a Pull Request

---

## Author

**Harry Mardika** - [GitHub Profile](https://github.com/hkacode)