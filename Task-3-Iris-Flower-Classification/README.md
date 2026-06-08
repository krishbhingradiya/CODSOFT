# Iris Flower Classification

## 📋 Project Overview

This project implements a **machine learning-based classification system** to predict iris flower species based on their physical characteristics. Using the classic Iris dataset, we develop and evaluate a Decision Tree Classifier to accurately categorize flowers into three species: *Setosa*, *Versicolor*, and *Virginica*.

**Project Objective:** Build an end-to-end ML pipeline that demonstrates data analysis, preprocessing, model training, and evaluation best practices.

---

## 🎯 Problem Statement

The Iris dataset contains measurements of four key botanical features (sepal length, sepal width, petal length, petal width) for 150 iris flower samples. The goal is to train a predictive model that can accurately classify iris flowers into their correct species category based on these measurements.

---

## 📊 Dataset Information

| Property | Details |
|----------|---------|
| **Dataset** | Iris Flower Dataset |
| **Total Samples** | 150 records |
| **Features** | 4 continuous features |
| **Target Classes** | 3 iris species |
| **Missing Values** | None |

### Features:
- **Sepal Length** (cm): Range 4.3 - 7.9
- **Sepal Width** (cm): Range 2.0 - 4.4
- **Petal Length** (cm): Range 1.0 - 6.9
- **Petal Width** (cm): Range 0.1 - 2.5

### Target Variable:
- **Species** (Categorical):
  - Iris-setosa
  - Iris-versicolor
  - Iris-virginica

---

## 🛠️ Technology Stack

| Component | Technology |
|-----------|-----------|
| **Language** | Python 3.x |
| **Data Processing** | Pandas, NumPy |
| **Machine Learning** | Scikit-learn |
| **Visualization** | Matplotlib, Seaborn |
| **Environment** | Google Colab / Jupyter Notebook |

---

## 📁 Project Structure

```
Task-3-Iris-Flower-Classification/
├── Task_3.ipynb                    # Main Jupyter Notebook
├── README.md                        # Project Documentation
└── IRIS.csv                         # Dataset File
```

---

## 🔄 Project Workflow

### 1. **Data Loading & Exploration**
   - Load the Iris dataset from CSV file
   - Display first few records and dataset structure
   - Verify data integrity and completeness

### 2. **Exploratory Data Analysis (EDA)**
   - Check dataset shape and column names
   - Analyze basic statistics (mean, std, min, max)
   - Identify and handle missing values (None found)
   - Visualize feature distributions and relationships

### 3. **Data Preprocessing**
   - Remove unnecessary columns (if applicable)
   - Encode categorical target variable using LabelEncoder
   - Split data into training and testing sets (80-20 split)

### 4. **Model Development**
   - Implement Decision Tree Classifier
   - Train the model on the training dataset
   - Fine-tune hyperparameters as needed

### 5. **Model Evaluation**
   - Generate predictions on test set
   - Calculate accuracy score
   - Create confusion matrix visualization
   - Generate detailed classification report

### 6. **Results & Insights**
   - Analyze model performance metrics
   - Identify classification patterns
   - Document key findings

---

## 🔧 Installation & Setup

### Prerequisites
```bash
Python 3.6 or higher
pip (Python package manager)
```

### Required Libraries
```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
```

### Quick Start
```bash
# 1. Clone the repository
git clone https://github.com/krishbhingradiya/CODSOFT.git

# 2. Navigate to project directory
cd CODSOFT/Task-3-Iris-Flower-Classification

# 3. Launch Jupyter Notebook
jupyter notebook Task_3.ipynb
```

---

## 📈 Model Performance

The Decision Tree Classifier achieves the following performance metrics:

| Metric | Value |
|--------|-------|
| **Accuracy** | High (depends on test split) |
| **Precision** | Weighted average across classes |
| **Recall** | Balanced across species |
| **F1-Score** | Harmonic mean of precision & recall |

### Classification Report
The model generates detailed per-class metrics:
- True Positive (TP): Correctly predicted species
- False Positive (FP): Incorrect species predictions
- False Negative (FN): Missed predictions

### Confusion Matrix
Provides a detailed breakdown of prediction accuracy per species class, helping identify any class-specific misclassifications.

---

## 🎓 Key Learnings

This project demonstrates:

1. **End-to-End ML Pipeline Development**
   - From raw data to deployment-ready predictions

2. **Data Preprocessing Best Practices**
   - Data cleaning, encoding, and train-test splitting

3. **Model Selection & Training**
   - Understanding decision tree algorithms and hyperparameters

4. **Comprehensive Model Evaluation**
   - Multiple evaluation metrics beyond just accuracy

5. **Data Visualization Techniques**
   - Clear visual representation of data distributions and model performance

---

## 📊 Visualization Components

The notebook includes:
- **Feature distributions** using histograms and box plots
- **Correlation heatmaps** to identify feature relationships
- **Confusion matrix visualization** for classification analysis
- **Classification report summaries** for detailed metrics

---

## 🚀 Future Enhancements

Potential improvements for production deployment:

1. **Advanced Algorithms**
   - Random Forest, SVM, Neural Networks

2. **Hyperparameter Optimization**
   - GridSearchCV for automated parameter tuning
   - Cross-validation for robust evaluation

3. **Feature Engineering**
   - Create derived features from existing measurements
   - Feature scaling and normalization

4. **Model Deployment**
   - Save trained model using joblib/pickle
   - Create REST API for predictions
   - Build web interface for user interaction

5. **Performance Enhancement**
   - Ensemble methods (Voting, Bagging)
   - Class imbalance handling (if applicable)

---

## 💡 Usage Example

```python
# After loading and training the model:

# Make predictions on new data
new_flower = [[5.1, 3.5, 1.4, 0.2]]
prediction = model.predict(new_flower)

# Get prediction probability
probability = model.predict_proba(new_flower)
```

---

## 📝 Code Highlights

### Data Loading
```python
df = pd.read_csv('IRIS.csv')
```

### Model Training
```python
from sklearn.tree import DecisionTreeClassifier
model = DecisionTreeClassifier()
model.fit(X_train, y_train)
```

### Evaluation
```python
from sklearn.metrics import accuracy_score, classification_report
accuracy = accuracy_score(y_test, y_pred)
print(classification_report(y_test, y_pred))
```

---

## 📌 Key Statistics

- **Dataset Completeness**: 100% (no missing values)
- **Feature Correlation**: Strong separation between species
- **Training Data**: 120 samples
- **Testing Data**: 30 samples
- **Model Type**: Decision Tree Classifier

---

## 🔍 Troubleshooting

### Issue: Module not found error
**Solution:** Ensure all required libraries are installed using pip

### Issue: Dataset file not found
**Solution:** Verify IRIS.csv is in the same directory or upload via Google Colab file widget

### Issue: Poor model accuracy
**Solution:** Consider hyperparameter tuning or try alternative algorithms

---

## 📞 Contact & Support

**Project Author:** Krish Bhingradiya  
**Repository:** [CODSOFT GitHub](https://github.com/krishbhingradiya/CODSOFT)  
**Project Location:** Task-3-Iris-Flower-Classification

For questions or suggestions, please refer to the main repository documentation.

---

## 📄 License

This project is part of the CODSOFT Machine Learning internship program.

---

## 🙏 Acknowledgments

- **Dataset Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/iris)
- **Libraries:** Scikit-learn, Pandas, Matplotlib, Seaborn communities
- **CODSOFT:** For providing this learning opportunity

---

## 📚 References

1. Scikit-learn Documentation: [DecisionTreeClassifier](https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeClassifier.html)
2. Iris Dataset: [Fisher's Iris Flower Dataset](https://en.wikipedia.org/wiki/Iris_flower_data_set)
3. Pandas Documentation: [Data Analysis](https://pandas.pydata.org/)
4. Matplotlib/Seaborn: [Data Visualization](https://matplotlib.org/)

---

**Last Updated:** 2026  
**Status:** ✅ Complete & Tested
