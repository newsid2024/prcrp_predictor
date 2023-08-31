# Weather Prediction Project

This project involves predicting precipitation (PRCP) using machine learning techniques. The dataset used for this project contains various weather-related features such as temperature, wind speed, and weather type codes. The main goal is to build and evaluate a classification model to predict whether there will be precipitation on a given day.

## Project Structure

The project is organized into several main steps:

1. **Data Preprocessing**: The initial step involves loading and cleaning the dataset (`dataset.csv`). The dataset is read using the Pandas library, and missing values are handled by filling them with the mode of each column. Additionally, non-essential columns such as 'WT02', 'TAVG', 'PGTM', and several others are dropped.

2. **Feature Engineering**: The target feature 'PRCP' is transformed into a binary classification problem by setting any value greater than 0 to 1, indicating precipitation. The data is then normalized using Min-Max scaling to ensure features are on similar scales.

3. **Feature Selection**: The Chi-Square test is used to evaluate the statistical significance of each feature's relationship with the target variable. Features with high p-values are considered less relevant and are dropped from the dataset.

4. **Model Building**: Two classification models are used for predicting precipitation:
   - **Logistic Regression**: A logistic regression model is trained on the preprocessed dataset and evaluated for accuracy and other metrics.
   - **K-Nearest Neighbors (KNN)**: A KNN classifier is trained and tested for comparison.

5. **Model Evaluation**: The performance of both models is evaluated using metrics such as accuracy, precision, recall, F1-score, ROC curve, and AUC score. Different threshold values are explored to optimize model performance.

## Dependencies

The following libraries are used in this project:

- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

## How to Run

1. Make sure you have Python installed on your system.
2. Install the required libraries using `pip install pandas matplotlib seaborn scikit-learn`.
3. Download the `dataset.csv` file and place it in the same directory as the project files.
4. Run the project by executing the provided code snippets in your preferred Python environment (e.g., Jupyter Notebook).

## Results

The project's outcome includes:
- Data preprocessing and transformation
- Feature engineering and selection
- Model building and evaluation
- Visualizations of feature relationships and model performance

The final models achieved an accuracy of around 93.4% for the logistic regression model and a ROC AUC score of around 0.91.
