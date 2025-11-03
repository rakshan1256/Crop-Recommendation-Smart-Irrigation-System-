# Crop-Recommendation-Smart-Irrigation-System-
Built a high-accuracy ML model to classify crop types based on real-time soil and climate conditions. This system automates crop selection and provides smart irrigation decisions by integrating with a live weather API.
# AI-Driven Crop Recommendation & Smart Irrigation System

This project uses machine learning to recommend the best crop to grow based on soil and live weather data. It also includes the logic for a smart irrigation system to conserve water.

---

## Part 1: Crop Recommendation Model (99.55% Accuracy)

* Trained and compared 4 different classification models (Random Forest, Stacking, KNN, Logistic Regression) to predict one of 22 different crop types.
* The final **Random Forest** model achieved **99.55% accuracy** on the test set.
* Performed Exploratory Data Analysis (EDA) to visualize soil (N, P, K) and climate (temperature, rainfall) requirements for different crops.
* Saved the final model, scaler, and encoder as `.pkl` files for use in a live application.

**Model Comparison:**
![Model Accuracy Graph](visualisations/model_comparison.png)

---

## Part 2: Smart Irrigation App

* Loads the trained `.pkl` model to make live predictions.
* Fetches real-time weather data from the Open-Meteo API (no API key required).
* Applies a logic engine to provide a final decision ("IRRIGATE" or "DO NOT IRRIGATE") based on the crop's needs, current humidity, and recent rainfall.

---

## How to Run

1.  **Part 1 (Training):** Run the `1_Model_Training_EDA.ipynb` notebook to train the model and generate the `.pkl` files.
2.  **Part 2 (Application):** Run the `2_Smart_Irrigation_App.ipynb` notebook. This will load the saved models, fetch live weather, and print a final irrigation decision.

## Technologies Used
* Python
* Scikit-learn
* Pandas
* Matplotlib / Seaborn
* Joblib
* Jupyter Notebook
