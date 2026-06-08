# Movie Rating Prediction

A machine learning project that predicts IMDb movie ratings for Indian films using regression algorithms and comprehensive data analysis.

## Table of Contents

- [Overview](#overview)
- [Project Objective](#project-objective)
- [Dataset](#dataset)
- [Technologies & Libraries](#technologies--libraries)
- [Data Analysis](#data-analysis)
- [Features](#features)
- [Model Implementation](#model-implementation)
- [Results](#results)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Future Improvements](#future-improvements)
- [Author](#author)

## Overview

This project applies machine learning techniques to predict movie ratings on IMDb for Indian cinema. By analyzing various features such as genre, director, cast, duration, and historical votes, the models identify patterns that influence movie ratings. The project demonstrates end-to-end machine learning workflow including data exploration, preprocessing, feature engineering, model training, and evaluation.

## Project Objective

To develop a predictive model that accurately estimates movie ratings based on:
- Movie metadata (year, duration, genre)
- Cast and crew information (director, actors)
- Voting patterns and audience engagement

This helps stakeholders understand key factors affecting movie success and rating potential.

## Dataset

**Source:** [IMDb India Movies Dataset](https://www.kaggle.com/datasets/adrianmcmahon/imdb-india-movies)

### Dataset Characteristics:
- **Total Records:** 15,509 movies
- **Features:** 10 columns
- **Target Variable:** Rating (IMDb score 1-10)

### Columns:
| Column | Type | Description |
|--------|------|-------------|
| Name | String | Movie title |
| Year | String | Release year |
| Duration | String | Movie duration in minutes |
| Genre | String | Movie genre(s) |
| Rating | Float | IMDb rating (target variable) |
| Votes | Integer | Number of votes received |
| Director | String | Movie director |
| Actor 1 | String | Lead actor |
| Actor 2 | String | Supporting actor |
| Actor 3 | String | Supporting actor |

### Missing Values Summary:
- Duration: 8,269 missing values (53%)
- Rating: 7,590 missing values (49%)
- Votes: 7,589 missing values (49%)
- Genre: 1,877 missing values (12%)
- Year: 528 missing values (3%)
- Other features: Minimal missing values

## Technologies & Libraries

### Programming Language
- **Python 3.x**

### Core Libraries
- **Data Processing:** Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn
- **Machine Learning:** Scikit-learn
- **Preprocessing:** LabelEncoder (sklearn)

### Models Implemented
- Linear Regression
- Random Forest Regressor

### Evaluation Metrics
- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- R² Score

## Data Analysis

### Distribution Analysis
- **Rating Distribution:** Visualized using histogram with kernel density estimation
- Shows concentration of ratings and identifies distribution patterns

### Categorical Analysis
- **Top Genres:** Drama dominates, followed by Comedy and Thriller
- Genre analysis reveals which categories have higher average ratings

### Data Quality
- **Duplicate Removal:** Applied to ensure data integrity
- **Missing Value Handling:** 
  - Categorical features: Filled with 'Unknown'
  - Rating column: Dropped rows with missing ratings (primary target)

## Features

### Feature Engineering Approach
1. **Categorical Encoding:** LabelEncoder for director and actor names
2. **Genre Processing:** Categorical variable representing movie types
3. **Temporal Features:** Year information for trend analysis
4. **Audience Engagement:** Vote count as a proxy for popularity

### Feature Set
- Encoded Director
- Encoded Actor 1, Actor 2, Actor 3
- Genre information
- Movie Duration
- Release Year
- Vote Count

## Model Implementation

### Approach

#### 1. **Data Preprocessing**
```
- Load dataset with latin-1 encoding
- Handle missing values
- Remove duplicates
- Feature encoding
- Train-test split (typical 80-20)
```

#### 2. **Models Used**

**Linear Regression**
- Baseline model for comparison
- Assumes linear relationship between features and rating
- Fast training and interpretation

**Random Forest Regressor**
- Ensemble learning method
- Captures non-linear relationships
- Robust to outliers and missing patterns

#### 3. **Workflow**
1. Data loading and exploration
2. Data cleaning and preprocessing
3. Feature engineering and encoding
4. Train-test data splitting
5. Model training on training set
6. Performance evaluation on test set
7. Results comparison and analysis

## Results

### Model Evaluation Metrics

The models are evaluated using:
- **Mean Absolute Error (MAE):** Average absolute difference between predictions and actual ratings
- **Mean Squared Error (MSE):** Penalizes larger errors more heavily
- **R² Score:** Proportion of variance explained by the model

### Performance Comparison
Detailed results can be found by running the notebook. Random Forest typically outperforms Linear Regression due to its ability to capture complex non-linear patterns in movie ratings.

### Key Findings
- Director and cast composition significantly influence ratings
- Genre plays a crucial role in rating prediction
- Audience engagement (votes) correlates with rating accuracy

## Installation

### Prerequisites
- Python 3.7 or higher
- pip or conda package manager

### Setup Steps

1. **Clone the repository:**
```bash
git clone https://github.com/krishbhingradiya/CODSOFT.git
cd CODSOFT/Task-2-Movie-Rating-Prediction
```

2. **Create a virtual environment (optional but recommended):**
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install required packages:**
```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```

Or install from requirements file (if available):
```bash
pip install -r requirements.txt
```

## Usage

### Running the Project

1. **Using Jupyter Notebook:**
```bash
jupyter notebook Task_2.ipynb
```
Then run all cells sequentially or cell-by-cell for detailed analysis.

2. **Key Steps in the Notebook:**
   - Cell 1: Import all required libraries
   - Cell 2-3: Upload and load the dataset
   - Cell 4-6: Exploratory data analysis
   - Cell 7-8: Data cleaning and preprocessing
   - Cell 9+: Model training and evaluation

### Making Predictions

To make predictions on new data:

```python
# Example: Predict rating for a new movie
new_movie = [[encoded_director, encoded_actor1, encoded_actor2, 
              encoded_actor3, encoded_genre, duration, year, votes]]
predicted_rating = model.predict(new_movie)
print(f"Predicted Rating: {predicted_rating[0]:.2f}")
```

## Project Structure

```
Task-2-Movie-Rating-Prediction/
├── README.md                 # Project documentation
├── Task_2.ipynb             # Main Jupyter notebook
└── IMDb Movies India.csv    # Dataset (add locally)
```

## Future Improvements

### Enhancements for Future Versions
1. **Advanced Feature Engineering:**
   - Extract specific genres for multi-label classification
   - Create interaction features between cast and genre
   - Sentiment analysis on movie titles

2. **Model Enhancements:**
   - Hyperparameter tuning using GridSearchCV or RandomizedSearchCV
   - Gradient Boosting models (XGBoost, LightGBM)
   - Neural Networks for complex pattern recognition
   - Ensemble stacking of multiple models

3. **Data Improvements:**
   - Handle duration as numerical feature after parsing "min" suffix
   - Incorporate additional features (budget, release month, etc.)
   - Collect more recent data for temporal relevance

4. **Validation & Testing:**
   - Cross-validation for robust model evaluation
   - Feature importance analysis
   - Residual analysis and error distribution

5. **Deployment:**
   - Create REST API for model serving
   - Build web interface for predictions
   - Production-ready model packaging

## Author

**Krishnakumar Bhingradiya**

- GitHub: [@krishbhingradiya](https://github.com/krishbhingradiya)
- Project Repository: [CODSOFT](https://github.com/krishbhingradiya/CODSOFT)

## Acknowledgments

- Dataset sourced from [Kaggle - IMDb India Movies](https://www.kaggle.com/datasets/adrianmcmahon/imdb-india-movies)
- Project completed as part of CODSOFT Machine Learning internship
- Scikit-learn documentation and tutorials
- Python data science community

## License

This project is open source and available under the MIT License.

---

**Last Updated:** June 2026

For questions or suggestions, please feel free to open an issue on the GitHub repository.
