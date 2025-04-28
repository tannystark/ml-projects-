# Credit Card Fraud Detection

## Problem Statement
Develop a machine learning model to detect fraudulent credit card transactions based on structured financial data.

## Approach
- **Data Preprocessing**:
  - Handle missing values and outliers.
  - Address severe class imbalance using **undersampling** techniques.
  
- **Modeling**:
  - Built multiple supervised learning models:
    - Logistic Regression
    - Random Forest
    - Gradient Boosting
    - Support Vector Machine
    - Shallow Neural Networks
  
- **Model Evaluation**:
  - Used **Precision**, **Recall**, and **F1 Score** to evaluate the performance of each model.
  - The **Shallow Neural Network** performed the best with:
    - Precision: **0.92**
    - Recall: **0.92**
    - F1 Score: **0.92**

## Technologies Used
- **Programming Language**: Python
- **Libraries**: Scikit-learn, Keras, TensorFlow, Pandas, NumPy, Matplotlib, Seaborn
- **Data Handling**: Pandas, NumPy
- **Modeling**: Scikit-learn, Keras
- **Data Visualization**: Matplotlib, Seaborn

## Results
- The **Shallow Neural Network** outperformed other models with the best balance between precision and recall.
- Achieved a precision of **0.92**, recall of **0.92**, and F1 score of **0.92**.

## Key Learnings
- Techniques for handling **class imbalance** in highly skewed datasets.
- Comparison of multiple supervised learning models and understanding their strengths/weaknesses.
- Full model lifecycle from **data preprocessing** to **model evaluation**.

## Future Improvements
- Explore more advanced neural networks or ensemble techniques to further improve model performance.
- Investigate methods for **handling imbalanced datasets** more effectively, such as SMOTE.

