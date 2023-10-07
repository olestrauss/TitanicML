# Titanic Survival Prediction using Random Forest Classifier

This Python script demonstrates how to predict passenger survival on the Titanic using a Random Forest Classifier. It leverages the popular machine learning library, Scikit-Learn, for data preprocessing and model training. 
It scored .75 in the Kaggle competition.

## Prerequisites

Make sure you have the following libraries installed in your Python environment:

- pandas
- scikit-learn (sklearn)

You can install them using pip: `pip install pandas scikit-learn`

## Getting Started

### Loading Datasets

The code begins by loading the training and testing datasets (`train.csv` and `test.csv`) using the Pandas library. These datasets contain passenger information such as age, gender, class, and ticket fare.

### Data Preprocessing

Irrelevant columns (`PassengerId`, `Name`, `Ticket`, and `Cabin`) are dropped from both the training and testing datasets. The target variable `Survived` is separated from the features in the training data.

The training data is then split into training and validation sets using `train_test_split` to evaluate the model's performance locally.

### Data Transformation

#### One-Hot Encoding and Missing Value Handling

The code defines preprocessing steps for categorical and numerical columns. Categorical columns (`Sex` and `Embarked`) are transformed using one-hot encoding, and missing values are filled with the most frequent value. Numerical columns (`Pclass`, `Age`, `SibSp`, `Parch`, and `Fare`) are imputed with the mean for missing values.

### Model Training

A Random Forest Classifier is chosen as the model for this prediction task. The entire data preprocessing pipeline, including imputation and one-hot encoding, is created using Scikit-Learn's `Pipeline` and `ColumnTransformer`. The model is fitted to the training data.

### Model Evaluation

The model's accuracy is evaluated locally using the validation set, and a classification report is generated. The `accuracy_score` and `classification_report` functions from Scikit-Learn are used for this purpose.

### Making Predictions

The trained model is then used to make predictions on the testing dataset (`test.csv`). The resulting predictions are stored in a DataFrame.

### Saving Predictions

The predicted results, including `PassengerId` and `Survived` values, are saved to a CSV file named `predictions.csv`. This file can be used for further analysis or submission to competitions like Kaggle.

## Usage

1. Ensure you have the required libraries installed.
2. Download the Titanic dataset files (`train.csv` and `test.csv`) and place them in the same directory as this script.
3. Run the script. It will preprocess the data, train the Random Forest Classifier, evaluate the model locally, and generate predictions for the testing dataset.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- This script was created as a learning exercise in machine learning and data preprocessing.
- Dataset source: [Kaggle Titanic: Machine Learning from Disaster](https://www.kaggle.com/c/titanic)

Feel free to modify and enhance this code to experiment with different machine learning models and techniques for better predictive accuracy.


