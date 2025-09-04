
# 🚴 San Francisco Bikeshare ML Project

This project explores the **San Francisco Bikeshare dataset** from Google BigQuery and applies machine learning models to predict trip-related outcomes.  
The focus is on building regression models (Random Forest Regressor, Logistic Regression, etc.) to analyze factors such as trip duration, station usage, and bike demand.

---

## 📊 Dataset
- **Source:** [BigQuery Public Dataset: San Francisco Bikeshare](https://console.cloud.google.com/marketplace/product/cityofsandiego/san_francisco_bikeshare)  
- **Dataset ID:** `bigquery-public-data.san_francisco_bikeshare`  
- Contains information about trips, stations, subscribers, and bike usage.  

---

## 🎯 Objectives
1. **Predicting Trip Duration**  
   Based on features like start/end station, subscriber type, birth year, and trip date.  

2. **Predicting Station Usage**  
   Forecast usage levels at different stations using location, capacity, weather, and nearby attractions.  

3. **Predicting Bike Demand**  
   Forecast overall demand considering weather, events, and time of day.  

---

## 🛠️ Technologies & Libraries
- **Google BigQuery** (data extraction)  
- **Python (Colab / Jupyter)**  
- **Pandas & NumPy** (data handling)  
- **Scikit-learn** (ML models & preprocessing)  
- **Matplotlib & Seaborn** (visualizations)  

---

## 🔬 Model Used
- **Random Forest Regressor**  
   - Features: `subscriber_type`, `member_birth_year`  
   - Target: `duration_sec` (trip duration in seconds)  
   - Preprocessing:  
     - One-Hot Encoding for categorical features  
     - Standard Scaling for numerical features  
     - Missing value imputation with `SimpleImputer`  

---

## 📈 Results
- **R² Score (Random Forest):** ~0.50  
- Scatter plot shows predicted vs true trip duration.  

Example Visualization:  

![Sample Plot](https://matplotlib.org/stable/_images/sphx_glr_scatter_001.png)  
*(Replace with actual plot image if saved in repo)*

---

## 📂 Project Structure
```

📁 SanFrancisco-Bikeshare-ML
│── bikeshare\_model.ipynb   # Jupyter/Colab Notebook
│── README.md               # Project documentation
│── requirements.txt        # Dependencies (optional)

````

---

## 👨‍💻 Collaborators
- Hasan Zarook (2021-CE-58)  
- Abraham Oreem (2021-CE-32)  

---

## 🚀 How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/SanFrancisco-Bikeshare-ML.git
   cd SanFrancisco-Bikeshare-ML
````

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Open the notebook in **Google Colab** or **Jupyter Notebook**.
   Make sure to authenticate with your Google account for BigQuery access:

   ```python
   from google.colab import auth
   auth.authenticate_user()
   ```
---

## 📌 Future Work

* Try Logistic Regression for classification tasks (e.g., predicting user type).
* Incorporate weather/event datasets for improved predictions.
* Deploy model using **Flask / FastAPI** or **Google Cloud AI Platform**.

```

---
