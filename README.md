Vaccine Prediction

This project predicts the likelihood that individuals will receive two types of vaccines: the XYZ flu vaccine and the seasonal flu vaccine. This is a multilabel classification problem where the goal is to predict two probabilities for each individual: one for receiving the XYZ vaccine and another for the seasonal vaccine.

Project Overview

This project uses machine learning techniques to predict vaccine uptake based on a variety of demographic, behavioral, and health-related features. The dataset includes information such as age group, education, race, income, marital status, and more.

Datasets

The project uses the following datasets:

- `training_set_features.csv`: Features for the training set.
- `training_set_labels.csv`: Labels for the training set.
- `test_set_features.csv`: Features for the test set.
- `submission_format.csv`: Format for the submission file.

Model and Approach

The project uses the following approach:

1. Data Preprocessing: Handle missing values, encode categorical features, and scale numerical features.
2. Model Training: Train a Random Forest classifier using the MultiOutputClassifier wrapper to handle multilabel classification.
3. Evaluation: Evaluate the model using ROC AUC scores on a validation set.
4. Prediction: Predict probabilities for the test set and generate a submission file.

The code is structured as follows:

- Preprocessing: Use `ColumnTransformer` to apply different preprocessing steps to numerical and categorical features.
- Pipeline: Combine preprocessing and model training in a `Pipeline` for cleaner code and easier management.

Evaluation

The model is evaluated using the area under the receiver operating characteristic curve (ROC AUC) for each of the two target variables. The overall score is the mean of the ROC AUC scores for `xyz_vaccine` and `seasonal_vaccine`.

Results

The model's performance on the validation set is measured by the mean ROC AUC score. The prediction script generates a `submission.csv` file with the predicted probabilities for the test set.

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.

