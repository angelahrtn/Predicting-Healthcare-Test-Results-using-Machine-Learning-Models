# Predicting-Healthcare-Test-Results
# Project Overview
This project, conducted as part of a Machine Learning course in the third semester, focuses on predicting healthcare test results based on patient data using multiple machine learning models. The dataset includes various patient information and healthcare details, which are analyzed to classify test results into three categories: Normal, Inconclusive, and Abnormal. Several machine learning models, including Random Forest, Bagging, Boosting, and Stacking, were implemented to determine the best-performing model for accurate classification. The project emphasizes improving the models through tuning to enhance prediction accuracy.

# Case Description
The primary goal of this project is to classify healthcare test results based on patient data, which includes variables such as:
- Days Gap (calculated from Date of Admission and Discharge Date)
- Medical history
- Test-related variables
Healthcare test result prediction is crucial for optimizing medical diagnoses and resource management. By using machine learning models, we aim to predict whether a test result is Normal, Inconclusive, or Abnormal, which could assist healthcare professionals in better managing patient care.

# Objectives
- Build predictive models to classify healthcare test results into three categories.
- Compare different machine learning models to identify the best-performing one.
- Tune the models to enhance performance, especially in terms of recall and precision for each test result class.
- Evaluate models using various metrics such as accuracy, precision, recall, and F1-score.
- Provide recommendations for improving healthcare test result predictions.

# Project Steps and Features
1. Data Collection and Preparation
- The dataset was sourced from a healthcare database and loaded into Google Colab for analysis. Key steps in data preparation include:
  - Feature extraction: Creating the new feature 'Days Gap' (difference between admission and discharge dates).
  - Encoding: Using label encoding and one-hot encoding for categorical features.
  - Scaling: Applying StandardScaler to normalize numerical data.

2. Model Construction
- Four machine learning models were implemented:
  - Random Forest: A bagging method used to reduce variance.
  - Bagging: Another ensemble method focused on stability and accuracy.
  - Boosting: A model that focuses on improving misclassified instances.
  - Stacking: A combination of multiple models to improve overall predictions.

3. Model Tuning
- Each model was tuned using hyperparameter optimization techniques to improve its performance.
- Tuning involved adjusting parameters such as the number of estimators, learning rates, and max depths to balance model accuracy and recall.

4. Model Evaluation
- The models were evaluated using metrics like:
  - Accuracy: The overall correctness of the model.
  - Precision and Recall: Important for measuring the model’s performance on individual test result categories (Normal, Inconclusive, Abnormal).
  - F1-Score: A balance between precision and recall.

5. Results and Interpretation
- Boosting was identified as the best-performing model, achieving the highest accuracy of 0.35 after tuning.
- Other models like Random Forest and Bagging showed improvements, but faced challenges in predicting less frequent classes (Inconclusive and Normal).

# Tools Used
- Programming Language: Python
- Libraries:
  - Pandas: For data manipulation.
  - NumPy: For numerical computations.
  - Scikit-learn: For implementing machine learning models.
  - Google Colab: For executing the analysis in Jupyter Notebook environment.
  - Matplotlib & Seaborn: For data visualization.
  - StandardScaler: For normalizing numerical data.

# Challenges
- Class Imbalance: Predicting rare classes (Inconclusive and Normal) was a challenge due to the imbalance in the dataset.
- Model Tuning: Hyperparameter tuning was necessary to improve the performance of the models, but it was computationally expensive and required careful fine-tuning.
- Feature Engineering: Creating the 'Days Gap' feature significantly impacted model performance, but more feature extraction could further improve predictions.

# Conclusion
This project successfully applied several machine learning models to predict healthcare test results. After evaluating different models, Boosting emerged as the most accurate, with an accuracy improvement from 0.34 to 0.35 after tuning. Other models like Random Forest and Stacking also performed well but faced challenges in accurately predicting the less frequent categories.

Further improvements could include advanced feature engineering, better handling of class imbalance, and testing additional machine learning models. This project demonstrates the effectiveness of machine learning techniques in healthcare prediction and highlights the importance of model tuning and feature extraction for better performance.
