# 🌍 Earthquake Prediction using Machine Learning  

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg?logo=python&logoColor=white)](https://www.python.org/)  
[![Tableau](https://img.shields.io/badge/Tableau-Visualization-orange.svg?logo=tableau&logoColor=white)](https://www.tableau.com/)  
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)  

✨ *A project for **CSE3505 - Essentials of Data Analytics** under **ELANGO N M***  

---

## 🎯 Abstract  
Earthquakes are **unpredictable natural disasters** that cause massive damage.  
In this project, we used **historic earthquake data** from California to build **Machine Learning models** that predict:  

- 📍 The probability of an earthquake in a region  
- 💥 Its possible magnitude  

> 🛑 Goal → Early warning systems, disaster planning & better risk assessment  

---

## 📂 Dataset  
We used the [SOCR Earthquake Dataset](http://socr.ucla.edu/docs/resources/SOCR_Data/SOCR_Data_Earthquakes_Over3.html) 📊  

📅 Period: **2017 → 2019**  
📈 Total Earthquakes: **37,706**  

Each record contains:  
- 🕒 Date & Time (UTC)  
- 🌎 Latitude & Longitude of epicenter  
- 📏 Depth (km)  
- 💥 Magnitude (Richter scale)  
- 📡 Number of stations recording  
- 📐 Gap, RMS, SRC  

---

## 📊 Data Visualization (Tableau)  

✨ Insights discovered:  
- Earthquakes vs number of stations recording it  
- Magnitude distribution  
- Depth vs Magnitude trends over the years  
- Heatmaps for density of earthquakes  

*(Graphs created in Tableau – Insert screenshots here 📷)*  

---

## 🛠️ Machine Learning Models  

We tested **4 different ML models**:  

### 🔹 Linear Regression  
- Predicts magnitude using latitude, longitude, depth & stations  
- Equation:  
Mag = -0.60Lat + 1.20Long - 0.0008Depth + 0.023Stations + 0.157

- 📉 MSE: `0.175` | R²: `0.035`  

---

### 🔹 Support Vector Machine (SVM)  
- Tries to fit a **hyperplane** for prediction  
- Works well on non-linear data (using kernels)  
- 📉 MSE: `0.532` | R²: `-1.92` ❌  

---

### 🔹 Naive Bayes  
- **Probabilistic model** based on Bayes’ theorem  
- Very scalable and fast  
- ✅ Accuracy: **98.5%**  
- Confusion Matrix heatmap shows high classification power  

---

### 🔹 Random Forest 🌲  
- Ensemble of decision trees → more stable & accurate  
- Handles overfitting much better  
- 📉 MSE: `0.156` | R²: `0.143` ✅ Best performance!  
- Feature Importance plot highlights most impactful features  

---

## 🏆 Conclusion  

📊 Model Comparison:  

| Model              | MSE     | R²      | Accuracy   |
|--------------------|---------|---------|------------|
| Linear Regression  | 0.175   | 0.035   | - |
| SVM                | 0.532   | -1.92   | - |
| Naive Bayes        | -       | -       | 98.5% ✅ |
| Random Forest 🌲   | 0.156   | 0.143   | - ✅ Best |

👉 **Random Forest outperformed all models for magnitude prediction**.  
👉 **Naive Bayes worked great for classification** tasks.  

---

## 🚀 Tech Stack  
- 🐍 Python (Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn)  
- 📊 Tableau (for visualization)  
- 🌲 ML Models: Linear Regression, SVM, Naive Bayes, Random Forest  

---

## 👨‍💻 How to Run  

# Clone the repository
git clone https://github.com/your-username/Earthquake-Prediction-ML.git

# Navigate into the folder
cd Earthquake-Prediction-ML

# Install dependencies
pip install -r requirements.txt

# Run the notebook
jupyter notebook earthquake_prediction.ipynb


📌 Future Work

🔮 Improve prediction with Deep Learning models (RNN, LSTM)

🌐 Expand dataset to global earthquakes

📡 Real-time data integration for early warning systems
