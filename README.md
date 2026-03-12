# Titanic Survival Prediction

This project analyzes the famous Titanic dataset from Kaggle to predict passenger survival using machine learning techniques. The analysis includes data exploration, visualization, feature engineering, and model training with various algorithms.

## Dataset

The dataset is sourced from the [Kaggle Titanic competition](https://www.kaggle.com/c/titanic). It consists of:
- `train.csv`: Training data with passenger information and survival labels.
- `test.csv`: Test data without survival labels for prediction.

## Data Dictionary

- **Survived**: 0 = No, 1 = Yes
- **Pclass**: Ticket class (1 = 1st, 2 = 2nd, 3 = 3rd)
- **SibSp**: Number of siblings/spouses aboard
- **Parch**: Number of parents/children aboard
- **Ticket**: Ticket number
- **Cabin**: Cabin number
- **Embarked**: Port of Embarkation (C = Cherbourg, Q = Queenstown, S = Southampton)

## Requirements

- Python 
- Libraries: pandas, numpy, matplotlib, seaborn, scikit-learn

Install dependencies using pip:

pip install pandas numpy matplotlib seaborn scikit-learn


## How to Run

1. Clone or download the repository.
2. Ensure `train.csv` and `test.csv` are in the same directory as the notebook.
3. Open `Titanic.ipynb` in Jupyter Notebook or JupyterLab.
4. Run the cells sequentially to perform data loading, exploration, visualization, feature engineering, modeling, and prediction.
5. The final predictions will be saved to `solution.csv`.

## Project Structure

- **Data Collection**: Load training and testing datasets.
- **Exploratory Data Analysis**: Examine data structure, check for null values, and understand distributions.
- **Data Visualization**: Visualize survival rates across categorical features like Sex, Pclass, SibSp, Parch, and Embarked.
- **Feature Engineering**:
  - Extract titles from names and map to categories.
  - Map Sex and Embarked to numerical values.
  - Fill missing Age values and bin into categories.
  - Bin Fare into quartiles.
  - Map Cabin letters to numerical values.
  - Create FamilySize feature from SibSp and Parch.
- **Modeling**: Train and evaluate models using K-Fold cross-validation:
  - K-Nearest Neighbors (KNN)
  - Decision Tree
  - Random Forest
  - Support Vector Machine (SVM)
  - Naive Bayes
- **Testing**: Use the best model (SVM) to predict on test data and generate solution file.

## Results

Model accuracies from cross-validation:
- KNN: ~81%
- Decision Tree: ~78%
- Random Forest: ~80%
- SVM: ~83%
- Naive Bayes: ~79%

The SVM model is used for final predictions.

## Files

- `Titanic.ipynb`: Main Jupyter notebook with analysis and code.
- `train.csv`: Training dataset.
- `test.csv`: Test dataset.
- `solution.csv`: Predicted survival outcomes for test data.

## License

This project is for educational purposes. Dataset is from Kaggle.