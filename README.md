# House Price Prediction: A CRISP-DM Approach with Random Forests

## 📖 Blog Post  
Check out the full write-up on Medium:  
🔗 [House Price Prediction: A CRISP-DM Approach with Random Forests](https://medium.com/@tshepisomokoena20/house-price-prediction-a-crisp-dm-approach-with-random-forests-518f4615ce1b)  

---

## 🎯 Project Objective  

This project follows the **CRISP-DM (Cross-Industry Standard Process for Data Mining)** framework to **analyze, model, and predict house prices** using **Random Forest Regression**. The goal is to **identify key price-driving factors** and create an accurate predictive model that can help **homeowners, investors, and real estate professionals** make **data-driven pricing decisions**.  

---

## 📌 CRISP-DM Process  

### **1️⃣ Business Understanding**  
**Key Business Questions:**  
1. **Which factors most influence house prices?**  
2. **How do amenities (e.g., air conditioning, basement, parking) impact house prices?**  
3. **Does furnishing status (furnished, semi-furnished, unfurnished) significantly affect house prices?**  
4. **Can we build an accurate predictive model for house prices?**  

### **2️⃣ Data Understanding**  
- The dataset contains **545 housing records** with **13 features**, including:  
  - **Numerical Features**: `price`, `area`, `bedrooms`, `bathrooms`, `stories`, `parking`  
  - **Categorical Features**: `mainroad`, `guestroom`, `basement`, `hotwaterheating`, `airconditioning`, `prefarea`, `furnishingstatus`  

### **3️⃣ Data Preparation**  
- **Encoded categorical variables** (`yes/no` → `1/0`)  
- **Scaled numerical variables** using **StandardScaler**  
- **Split the dataset** into **80% training** and **20% testing**  

### **4️⃣ Modeling**  
- Built a **Random Forest Regressor** for house price prediction  
- Used **GridSearchCV** to **fine-tune hyperparameters**  
- Evaluated model using **Mean Absolute Error (MAE), Mean Squared Error (MSE), RMSE, and R² Score**  

### **5️⃣ Evaluation**  
- **Identified the most influential factors** in house pricing  
- **Assessed model performance** to ensure generalization  
- **Validated findings with feature importance analysis**  

### **6️⃣ Deployment (Optional)**  
- The model can be **converted into a Flask API** for real-time price predictions  

---

## 📁 File Structure  

📄 README.md # Project documentation │── 📄 Housing.csv # Housing dataset │── 📄 House Pricing Model.ipynb # Jupyter Notebook (EDA, Modeling, and Evaluation)


---

## ⚙️ Installation  

To set up the project, clone the repository and install dependencies:  

```sh
git clone https://github.com/your-username/house-price-prediction.git
cd house-price-prediction
pip install -r requirements.txt



### 🛠 Required Libraries  

```sh
pip install pandas numpy matplotlib seaborn scikit-learn
```

If using Jupyter Notebook, install:  

```sh
pip install notebook
```

---

## 🏆 Results  

### ✅ **Model Performance:**  
| Metric | Score |
|--------|------:|
| **Best Hyperparameters** | `{ 'max_depth': 10, 'min_samples_leaf': 2, 'min_samples_split': 2, 'n_estimators': 100 }` |
| **Mean Absolute Error (MAE)** | **1,055,753.94** |
| **Mean Squared Error (MSE)** | **2.05 × 10¹²** |
| **Root Mean Squared Error (RMSE)** | **1,431,492.91** |
| **R² Score** | **0.5946** |

### 📊 **Feature Importance:**  
- **Area** is the most significant factor, contributing nearly **50%** to price determination.  
- **Bathrooms and air conditioning** are strong predictors, influencing valuation.  
- **Location factors (mainroad, preferred area) are less impactful**, contrary to common belief.  

---

## ✅ Answers to Business Questions  

- **Which factors most influence house prices?**  
  - **Area, bathrooms, air conditioning, and number of stories are key drivers.**  

- **How do amenities impact house prices?**  
  - **Features like air conditioning and furnished status significantly raise home values.**  

- **Does furnishing status affect pricing?**  
  - **Yes, furnished homes command the highest prices, followed by semi-furnished and unfurnished.**  

- **Can we build an accurate predictive model for house prices?**  
  - **Yes, with an R² score of 0.59, the model performs well but could be improved with additional location and market data.**  

---

## 🚀 Next Steps  

- **Enhance predictions by incorporating location-based data** (neighborhood, crime rates, school ratings).  
- **Use external market trends** (real estate demand, inflation) for better accuracy.  
- **Experiment with advanced models** like **XGBoost or Gradient Boosting**.  






