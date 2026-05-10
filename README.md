# Alcohol QCM Sensor Dataset - Classification Analysis

## Overview
Machine learning classification project analyzing the Alcohol QCM (Quartz Crystal Microbalance) Sensor Dataset. The goal is to classify different alcohol compounds based on sensor measurements using multiple supervised learning algorithms.

## Dataset
- **Source**: [UCI Machine Learning Repository - Alcohol QCM Sensor](https://archive.ics.uci.edu/dataset/496/alcohol+qcm+sensor+dataset)
- **Target Variable**: 5 alcohol compounds classification
  - 1-Octanol
  - 1-Propanol
  - 2-Butanol
  - 2-Propanol
  - 1-Isobutanol
- **Features**: Multi-sensor QCM measurements
- **Data Split**: 70% training, 30% testing

## Technologies
- **Python** - Programming language
- **Pandas** - Data manipulation and loading
- **Scikit-learn** - Machine learning algorithms
- **Matplotlib/Seaborn** - Data visualization
- **Jupyter Notebook** - Interactive analysis

## Installation
```bash
# Clone repository
git clone <repository-url>
cd alcohol-qcm-analysis

# Install dependencies
pip install pandas scikit-learn matplotlib seaborn jupyter numpy
```

## Project Structure
├── QCM-Alcohol.ipynb              # Main analysis notebook
├── data/
│   └── QCM Sensor Alcohol Dataset/  # CSV files
├── README.md

## Usage
```bash
jupyter notebook QCM-Alcohol.ipynb
```

## Models Evaluated
The project compares the following classification algorithms:

1. **Decision Tree Classifier** - Single tree baseline
2. **Random Forest Classifier** - 100 trees ensemble
3. **K-Nearest Neighbors (KNN)** - k=3 neighbors
4. **AdaBoost Classifier** - Adaptive boosting (10 estimators)
5. **Logistic Regression** - Linear classifier
6. **Voting Classifier** - Ensemble of multiple models (KNN, Adaboost and Logistic Regression)

## Key Results
All models were trained on 70% of the data and evaluated on 30% test set:

| Model | Accuracy |
|-------|----------|
| Decision Tree | ~0.87 |
| Random Forest | ~1.00 |
| KNN (k=3) | ~0.92 |
| AdaBoost | ~0.74 |
| Logistic Regression | ~0.71 |
| Voting Classifier | ~0.74 |

## Workflow
1. **Data Loading** - Load and combine CSV files from UCI dataset
2. **Data Exploration** - Examine dataset structure and distributions
3. **Target Engineering** - Create target variable from one-hot encoded columns
4. **Feature Preparation** - Prepare features (X) and target (y)
5. **Train-Test Split** - Split data (70% train, 30% test)
6. **Model Training** - Train multiple classification models
7. **Model Evaluation** - Compare accuracy across models
8. **Visualization** - Bar plot comparing model performance
9. **Ensemble Methods** - Combine multiple classifiers using Voting

## Key Insights
- KNN (acc = 0.92) clearly outperformed the VotingClassifier (acc = 0.74) .
- The voting classifier needs tuning before it can outperform the single KNN model.

## Next Steps
- Hyperparameter tuning for best performing models
- Cross-validation for more robust evaluation
- Feature importance analysis
- Confusion matrix analysis
- Class imbalance handling if needed

## Author
Barbara Alfaro

## References
- [UCI ML Repository](https://archive.ics.uci.edu/)
- [Scikit-learn Documentation](https://scikit-learn.org/)
- [QCM Sensor Technology](https://en.wikipedia.org/wiki/Quartz_crystal_microbalance)

