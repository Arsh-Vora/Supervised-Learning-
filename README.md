# Heart Disease Prediction using K-Nearest Neighbors (KNN)

This project demonstrates how to build and evaluate a K-Nearest Neighbors (KNN) classifier to predict the presence of heart disease in patients. The model is trained on the "Heart Disease UCI" dataset, and the entire workflow is implemented in a Jupyter Notebook.

## Project Overview

The primary goal of this project is to develop a reliable machine learning model that can classify patients into two categories: those with heart disease and those without. The project covers all the key stages of a machine learning workflow, from data preparation and cleaning to model training, evaluation, and visualization.

The key steps in this project are:
1.  **Data Preparation**: Loading the dataset and performing an initial exploratory analysis.
2.  **Data Cleaning and Preprocessing**: Handling missing values, encoding categorical features, and creating a binary target variable.
3.  **Model Training**: Splitting the data and training a KNN classifier with an optimal `k` value.
4.  **Model Evaluation**: Assessing the model's performance using various metrics, including accuracy, a classification report, a confusion matrix, and an ROC curve.

## Getting Started

To run this project on your local machine, follow these steps:

### Prerequisites

Make sure you have Python installed. The required libraries are listed in the [`requirements.txt`](requirements.txt:1) file.

### Installation

1.  Clone the repository to your local machine:
    ```bash
    git clone https://github.com/your-username/Supervised-Learning-.git
    ```
2.  Navigate to the project directory:
    ```bash
    cd Supervised-Learning-
    ```
3.  Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

### Dataset

This project uses the "Heart Disease UCI" dataset, which can be downloaded from Kaggle.

1.  **Download the dataset**:
    *   Go to the [Heart Disease Data](https://www.kaggle.com/datasets/redwankarimsony/heart-disease-data?resource=download) page on Kaggle.
    *   Click the "Download" button to get the `heart_disease_uci.csv` file.

2.  **Add the dataset to the project**:
    *   Create a `data` directory in the root of the project folder.
    *   Place the downloaded `heart_disease_uci.csv` file inside the `data` directory.

### Running the Notebook

Once the setup is complete, you can run the Jupyter Notebook:

```bash
jupyter notebook notebooks/knn.ipynb
```

## Workflow

The project is structured in the following sequence:

1.  **Introduction and Setup**: Imports all necessary libraries, including `pandas`, `numpy`, `matplotlib`, `seaborn`, and `scikit-learn`.
2.  **Data Preparation**:
    *   Loads the "Heart Disease UCI" dataset from `data/heart_disease_uci.csv`.
    *   Displays the first few rows, general information, and descriptive statistics of the dataset.
3.  **Data Cleaning and Preprocessing**:
    *   Drops irrelevant columns (`id`, `dataset`).
    *   Engineers the `target` variable from the `num` column, where `0` indicates no heart disease and `1` indicates the presence of heart disease.
    *   Handles missing values using median imputation for numerical columns.
    *   Applies one-hot encoding to convert categorical features into a numerical format.
4.  **Data Splitting and Scaling**:
    *   Splits the data into training and testing sets (80/20 split).
    *   Standardizes the features using `StandardScaler` to ensure all variables contribute equally to the model.
5.  **Finding the Optimal K**:
    *   Determines the best `k` value for the KNN model by plotting the error rate for a range of `k` values (1 to 29). The optimal `k` is found to be `6`.
6.  **Model Training and Evaluation**:
    *   Trains the KNN classifier using the optimal `k` value.
    *   Evaluates the model's performance on the test set, generating:
        *   **Accuracy Score**: Measures the overall correctness of the model.
        *   **Classification Report**: Provides precision, recall, and F1-score for each class.
        *   **Confusion Matrix**: Visualizes the model's performance in classifying true positives, true negatives, false positives, and false negatives.
        *   **ROC Curve and AUC Score**: Shows the model's ability to distinguish between classes.

## Results

*   **Model Accuracy**: The KNN classifier achieves an accuracy of **86.96%** on the test data.
*   **ROC AUC Score**: The model has an AUC score of **0.91**, indicating excellent performance in distinguishing between patients with and without heart disease.

The confusion matrix and classification report provide further details on the model's performance for each class.