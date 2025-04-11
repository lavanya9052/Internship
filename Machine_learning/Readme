# Student Performance Analysis

## 1. Project Overview

This project aims to analyze the Student Performance Dataset and develop a predictive model for student pass/fail status. The analysis involves data cleaning, exploratory data analysis (EDA), and the application of machine learning classification techniques. The goal is to identify key factors influencing student performance and build a model that can accurately predict academic outcomes.

## 2. Dataset

- [click here](https://www.kaggle.com/datasets/spscientist/students-performance-in-exams)


### 2.1. Description

The primary dataset used is "StudentsPerformance.csv," which contains student scores in mathematics, reading, and writing, along with various demographic, family, and school-related features.


## 3. Files

### 3.1. Core Files

* `student_performance.ipynb`: This Jupyter Notebook contains the complete Python code for the data analysis, model training, and evaluation.
* `StudentsPerformance.csv`: The dataset file used in the analysis.
* `README.md`: This file, providing a comprehensive overview of the project, methodology, and results.

### 3.2. Supporting Files (If Applicable)

* \[Any other files, e.g., visualizations saved as images, preprocessed data files, etc.]

## 4. Libraries and Dependencies

The following Python libraries are essential for running the code in the `student_performance.ipynb` notebook:

* `pandas`: For data manipulation and analysis.
* `numpy`: For numerical computations.
* `matplotlib`: For creating static, interactive, and animated visualizations.
* `seaborn`: For making statistical graphics.
* `scikit-learn`: For machine learning algorithms (Logistic Regression, Random Forest) and model evaluation metrics.

## 5.Methodology

## 5.1. Data Loading
The dataset was loaded into a pandas DataFrame using the pd.read_csv() function.

## 5.2. Data Cleaning
The following data cleaning steps were performed to ensure data quality and suitability for analysis:

- **Duplicate Removal**: Duplicate rows were identified and removed using the drop_duplicates() method to avoid redundancy in the data.

- **Missing Values Handling**: The dataset was checked for missing values using the isnull().sum() method. Since no missing values were found, no imputation or deletion was necessary.

- **Data Type Conversion**: Categorical features were transformed into numerical representations using one-hot encoding with the pd.get_dummies() function. The drop_first=True parameter was used to avoid multicollinearity.

## 5.3. Exploratory Data Analysis (EDA)

EDA was conducted to gain insights into the data's characteristics and relationships between variables. Key visualizations and analyses include:

- **Average Score Calculation**: A new feature, average_score, was calculated by averaging the scores in math, reading, and writing. This provides an overall measure of student performance.
- **Score Distributions**: Histograms were used to visualize the distribution of scores in each subject (math, reading, writing) and the average_score.
- **Correlation Analysis**: A correlation matrix was generated to explore the linear relationships between numerical features.
- **Categorical Feature Analysis**: Box plots and other appropriate visualizations were used to examine the relationship between categorical features (e.g., gender, race/ethnicity, parental level of education) and student performance (e.g., average_score).

For detailed visualizations and their interpretations, please refer to the student_performance.ipynb notebook.

## 5.4. Pass/Fail Classification

Target Variable Definition: A binary target variable, pass, was created to represent student pass/fail status. Students with an average_score of 70 or higher were labeled as "1" (pass), while those below 70 were labeled as "0" (fail).

- **Feature Selection**: The following features were selected as predictor variables (X): [List the selected features here and justify their selection based on EDA or domain knowledge].
- **Data Splitting**: The data was divided into training (80%) and testing (20%) sets using the train_test_split() function from scikit-learn, with random_state=42 for reproducibility.
- **Model Training**: Two classification models were trained on the training data:
- **Logistic Regression**: A linear model that predicts the probability of a binary outcome.
- **Random Forest**: An ensemble learning method that combines multiple decision trees.
  
## 5.5. Model Evaluation

The performance of the trained models was evaluated on the testing data using the following metrics:

- **Accuracy**: The proportion of correctly classified instances.
- **Confusion Matrix**: A table showing the number of true positives, true negatives, false positives, and false negatives.
- **F1-score**: The harmonic mean of precision and recall, providing a balanced measure of a model's accuracy.

The evaluation metrics were calculated and presented for both the Logistic Regression and Random Forest models to compare their effectiveness.

## 6. Results

This section should provide a concise summary of the key findings. Include specific metrics and observations.

For example:

"The Exploratory Data Analysis revealed strong correlations between scores in different subjects, indicating that students who perform well in one subject tend to perform well in others."
"Both the Logistic Regression and Random Forest models achieved high accuracy in predicting student pass/fail status. The Random Forest model demonstrated slightly better performance, with an accuracy of [Accuracy Value] and an F1-score of [F1-score Value], compared to the Logistic Regression model's accuracy of [Accuracy Value] and F1-score of [F1-score Value]."
"The confusion matrices showed that both models had some difficulty in accurately predicting students who failed, as indicated by [specific numbers from the confusion matrices]."

## 7. Conclusion
This analysis demonstrates the feasibility of predicting student pass/fail status using machine learning techniques. The Random Forest model exhibited strong predictive capabilities. The insights gained from the EDA can be valuable for educators in identifying students who may need additional support.

