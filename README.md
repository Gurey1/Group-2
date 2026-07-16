# SMART Survey Processing Pipeline and Machine Learning-Based Mortality Prediction

## Project Overview

This project was developed as part of the Data Science Final Year Project at SIMAD University. The objective of the project is to process raw SMART survey (.as) files through a complete data processing pipeline and develop machine learning models to predict mortality using anthropometric and household survey data.

The project follows the four-stage SMART Survey Processing Pipeline and applies machine learning techniques to classify mortality outcomes using a clean, analysis-ready dataset.

---

## Objectives

The main objectives of this project are:

- Process raw SMART survey (.as) files into structured datasets.
- Organize and classify SMART surveys based on survey type and administrative level.
- Extract mortality and anthropometry information.
- Clean and integrate multiple survey datasets into one final dataset.
- Develop machine learning models for mortality prediction.
- Compare the performance of different machine learning algorithms.
- Identify the best-performing model for mortality prediction.

---

## Dataset Description

The project uses SMART Survey datasets collected from multiple districts in Somalia.

The datasets include:

- Household information
- Anthropometric measurements
- Mortality records
- Survey metadata

Final datasets created during the project include:

- SMART_Clean_Dataset.csv
- mortality_household.csv
- mortality_legacy.csv
- survey_metadata.csv
- ML_Dataset_Final.csv

---

## Pipeline Stages

### Stage 1: Organize and Classify Surveys

- Read all SMART (.as) files.
- Identify survey type (Individual or Aggregate).
- Identify survey level (Admin2/LHZ).
- Organize surveys into folders.

### Stage 2: Convert to CSV

- Extract anthropometry data.
- Extract mortality data.
- Convert SMART survey files into CSV format.

### Stage 3: Household Processing

- Convert person-level mortality records into household-level records.
- Create household mortality datasets.
- Generate mortality indicators.

### Stage 4: Final Dataset Preparation

- Clean survey information.
- Standardize merge keys.
- Merge anthropometry and mortality datasets.
- Create the final machine learning dataset.

---

## Machine Learning Models Used

Three machine learning algorithms were implemented:

- K-Nearest Neighbors (KNN)
- Support Vector Machine (SVM)
- Decision Tree

Before training:

- Missing values were handled.
- Categorical variables were encoded.
- Features were standardized using StandardScaler.
- Class imbalance was handled using SMOTE.

---

## Results Summary

Three machine learning models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC
- Confusion Matrix

Model comparison:

| Model | Accuracy | Recall | AUC |
|--------|----------|---------|------|
| KNN | 87.46% | 15% | 0.520 |
| SVM | 72.01% | 31% | 0.535 |
| Decision Tree | 55.01% | **54%** | **0.564** |

The Decision Tree model achieved the highest Recall and ROC-AUC score, making it the most suitable model for identifying mortality cases in this dataset.

---

## Team Members

Group 2

- Abdinasir Xasan
- Harun
- (Add remaining group members if applicable)

---

## How to Run the Project

1. Clone the repository.

```bash
git clone https://github.com/yourusername/SMART_Mortality_Project.git
```

2. Open the project folder.

3. Install the required Python libraries.

```bash
pip install -r requirements.txt
```

4. Open the Jupyter notebooks.

5. Run the notebooks in the following order:

- Part I – SMART Survey Processing Pipeline
- Part II – Machine Learning Development

6. The final machine learning dataset will be generated in:

```
data/ml/ML_Dataset_Final.csv
```

---

## Project Structure

```
SMART_Mortality_Project/
│
├── data/
│   ├── final/
│   ├── ml/
│   └── mortality/
│
├── notebooks/
│   ├── Part1_Pipeline.ipynb
│   └── Part2_MachineLearning.ipynb
│
├── models/
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Imbalanced-learn (SMOTE)
- Matplotlib
- Jupyter Notebook

---

## License

This project was developed for academic purposes as part of the Data Science Final Year Project at SIMAD University.