# RBF Support Vector Classifier to predict rain


## 📌 Project Overview  
This project builds a **Support Vector Classifier (SVC)** using a **Radial Basis Function (RBF) kernel** to predict whether it will rain based on quantitative weather features. The classifier is optimized using **GridSearchCV** to tune hyperparameters (`C` and `gamma`).

## 📊 Dataset  
- **Source**: [Weather Forecast Dataset on Kaggle](https://www.kaggle.com/datasets/zeeshier/weather-forecast-dataset?select=weather_forecast_data.csv)  
- **File**: `weather_forecast_data.csv`  
- **Target Variable**: `Rain` (Categorical: "Yes" or "No")  
- **Features**:
  - Temperature  
  - Humidity  
  - Wind Speed  
  - Cloud Coverage  
  - Pressure  

The dataset contains under **10,000 rows**, making it suitable for efficient model training and evaluation.

## ⚙️ Methodology  
1. **Initial Model**  
   - Built an SVC using the RBF kernel with default hyperparameters  
   - Achieved a **baseline test accuracy of 87.7%**

2. **Model Optimization**  
   - Performed **Grid Search** on `C` and `gamma`  
   - Achieved an **optimized test accuracy of 97.1%** (accuracy = 0.9707)  
   - Generated a **confusion matrix** to evaluate model performance

## 🔍 Evaluation Metric Consideration  
The default scoring metric in GridSearchCV is **accuracy**, which may not always be ideal — particularly for **imbalanced datasets** where high accuracy can obscure poor performance on the minority class.

In this case:
- The dataset appears to be **relatively balanced**
- The **consequences of false positives or false negatives are minimal**
- Thus, using **accuracy as the evaluation metric is acceptable**

However, for **high-stakes applications** (e.g., flash flood or disaster prediction), it would be more appropriate to **maximize Recall**. In such cases, false negatives (i.e., failing to predict actual rain) could have **severe real-world consequences**, so a model that minimizes them is preferred.

## 📁 Files Included  
- `weather_forecast_data.csv` (linked from Kaggle)  
- `assignment_notebook.ipynb` (model training, grid search, and evaluation)  
- Confusion matrix output included in notebook

## ✅ Results Summary  
- **Baseline SVC Accuracy**: 87.7%  
- **Optimized SVC Accuracy (Grid Search)**: 97.1%  
- **Best Parameters Found**: via GridSearchCV  
- **Confusion Matrix**:
![Assign4_CM](https://github.com/user-attachments/assets/a5a09a80-e5a7-49ec-9ef7-f1e703cbe124) 
