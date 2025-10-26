# End-to-End Deep Learning Project using ANN

## Project Overview
This repository demonstrates an **end-to-end deep learning pipeline** for predicting **customer churn** and performing **salary regression** using an Artificial Neural Network (ANN). The project includes data preprocessing, model building, training, evaluation, and deployment via a Streamlit web application.

The deployed app is available [here](https://end-to-end-dl-project-using-ann-4vujetnwsbypdwaatvscdn.streamlit.app/).

---

## Dataset
The dataset used is **Churn_Modelling.csv**, containing 10,000 customer records with the following features:

- `CreditScore`: Customer's credit score  
- `Geography`: Customer's country (France, Germany, Spain)  
- `Gender`: Customer's gender  
- `Age`: Customer's age  
- `Tenure`: Number of years with the bank  
- `Balance`: Account balance  
- `NumOfProducts`: Number of products the customer has  
- `HasCrCard`: Whether the customer has a credit card (0 or 1)  
- `IsActiveMember`: Active membership status (0 or 1)  
- `EstimatedSalary`: Customer's salary  
- `Exited`: Whether the customer churned (0 or 1)

---

## Features

### 1. Customer Churn Prediction
- **Goal:** Predict whether a customer is likely to churn.  
- **Model:** ANN with 2 hidden layers (64 and 32 neurons) and an output layer with sigmoid activation.  
- **Data Preprocessing:**
  - Drop irrelevant columns: `RowNumber`, `CustomerId`, `Surname`
  - Label Encoding for `Gender`
  - One-Hot Encoding for `Geography`
  - Feature scaling using `StandardScaler`
- **Training:**
  - Optimizer: Adam  
  - Loss: Binary Crossentropy  
  - Metrics: Accuracy  
  - Early Stopping and TensorBoard callbacks included
- **Evaluation:** Validation accuracy around 86%.

### 2. Salary Regression
- **Goal:** Predict customer salary.  
- **Model:** ANN with 2 hidden layers (64 and 32 neurons) and a linear output layer.  
- **Data Preprocessing:**
  - Same as churn prediction
  - Target variable: `EstimatedSalary`
- **Training:**
  - Optimizer: Adam  
  - Loss: Mean Absolute Error (MAE)  
  - Metrics: MAE  
  - Early Stopping and TensorBoard callbacks included

---

## File Structure

├── app.py # Streamlit web app for churn prediction               
├── Churn_Modelling.csv # Dataset                    
├── ann.ipynb # Notebook for churn prediction                       
├── salaryregression.ipynb # Notebook for salary regression                     
├── model.h5 # Saved ANN model for churn prediction                    
├── scaler.pkl # Scaler for features                    
├── label_encoder_gender.pkl                      
├── one_hot_encoder.pkl                       
├── scaler1.pkl # Scaler for regression features                       
├── label_encoder_gender1.pkl                     
├── one_hot_encoder1.pkl                          
└── README.md                            



---

## Streamlit Web App

The **Streamlit app** allows users to input customer data and predict the probability of churn. Features include:

- Selectable Geography and Gender  
- Slider for Age, Tenure, and Number of Products  
- Input fields for Balance, Credit Score, and Estimated Salary  
- Output: Probability of churn and classification result  

---

## Installation

1. Clone the repository:
```bash
git clone https://github.com/ManelHjaoujia/End-to-End-DL-Project-using-ANN.git
cd End-to-End-DL-Project-using-ANN
```
## Install dependencies

```bash
pip install -r requirements.txt
```
## Run the Streamlit app

```bash
streamlit run app.py
```

## Technologies Used

- Python 3.x
- Pandas, NumPy, Scikit-learn
- TensorFlow / Keras
- Streamlit
- Pickle (for saving encoders and scalers)

---

## Conclusion

This project showcases a **complete ML workflow**:

- Data preprocessing
- ANN model building for classification and regression
- Model evaluation and visualization
- Deployment using Streamlit

It demonstrates practical skills for an **end-to-end deep learning pipeline**.

---

## Author

**Hjaoujia Manel**  
Master's Student in Information Systems Engineering & Data Science






