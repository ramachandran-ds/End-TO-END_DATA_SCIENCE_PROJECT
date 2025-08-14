# END-TO-END_DATA_SCIENCE_PROJECT
COMPANY        :   CODTECH IT SOLUTIONS

NAME           :   RAMACHANDRAN K

INTERN ID      :   CT04DH2787

DOMAIN         :   DATA SCIENCE

DURATION       :   4 WEEEKS

MENTOR         :   NEELA SANTOSH

# Iris Flower Species Prediction API — Google Colab Deployment

## 📌 Overview
This project demonstrates a **complete machine learning pipeline** developed and deployed entirely within a Google Colab environment. Using the famous **Iris dataset**, the model predicts the species of an Iris flower given four measured features: sepal length, sepal width, petal length, and petal width.

It covers the entire ML workflow:
1. Data loading & exploration
2. Preprocessing (scaling, splitting)
3. Model training & evaluation
4. Saving the model and scaler
5. Building an API with Flask
6. Temporary cloud deployment using **ngrok**

This step-by-step tutorial is designed for beginners learning data science, as well as developers prototyping quick APIs.

---

## 📂 Dataset
We use the well-known **Iris dataset** from `scikit-learn`:
- **Samples:** 150 flowers
- **Classes:**
  - 0 → Iris setosa
  - 1 → Iris versicolor
  - 2 → Iris virginica
- **Features:**
  1. Sepal length (cm)
  2. Sepal width (cm)
  3. Petal length (cm)
  4. Petal width (cm)

---

## ⚙ Technologies Used
- **Python** for the entire workflow
- **Pandas** for dataset handling
- **Scikit-learn** for data preprocessing, modeling, and evaluation
- **Logistic Regression** for classification
- **Pickle** to save and reload trained models
- **Flask** to create the API
- **Ngrok** for public exposure of Colab-hosted APIs

---

## 🚀 How to Run
### **1. Open in Google Colab**
Copy the `.ipynb` file into your Google Drive or upload it to Colab.

### **2. Install Required Packages**
The first cell installs:
!pip install flask-ngrok scikit-learn pandas numpy



### **3. Run the Notebook**
Execute each cell in order. The final cell will print out a **public ngrok link** like:
Running on: https://<random_id>.ngrok.io



### **4. Testing the API**
#### **Check API health**
Open the given URL in a browser:  
`https://<random_id>.ngrok.io/`

#### **Prediction endpoint**
Send a POST request to:
https://<random_id>.ngrok.io/predict


**Body:**
{
"features": [5.1, 3.5, 1.4, 0.2]
}


**Example using curl:**
curl -X POST -H "Content-Type: application/json"
-d '{"features":[5.1, 3.5, 1.4, 0.2]}'
https://<random_id>.ngrok.io/predict


**Response:**
{
"prediction_index": 0,
"prediction_label": "setosa"
}



---

## ⚠ Notes About Deployment
- **Session-based**: The API will stop working when you close your Colab session.
- For a permanent API, deploy onto **Render**, **Vercel**, **Heroku**, or **AWS**.

---

## 📊 Model Performance
The trained Logistic Regression model achieves **~95% accuracy** on the Iris dataset test split. While this dataset is simple, it’s perfect for demonstrating concepts.

---

## 🧩 Why This Project is Useful
This project is a **hands-on reference** for:
- Understanding the **end-to-end ML lifecycle**
- Learning to expose a model as a **REST API**
- Using **Google Colab + ngrok** as a fast deployment solution

---

## 📌 Future Improvements
- Add **FastAPI** alternative for better performance
- Integrate **model retraining** via API
- Deploy to persistent cloud hosting
  
---

## ✨ Credits
- Dataset: scikit-learn Iris dataset
- Author: Adapted for Google Colab + Flask + Ngrok pipeline
