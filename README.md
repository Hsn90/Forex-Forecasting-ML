# 📌 Forex Forecasting Using Machine Learning

## 📖 Project Overview

This project explores the application of **traditional time series models (ARIMA, Naïve)** and **advanced machine learning techniques (LightGBM, LSTM)** to predict the EUR/USD exchange rate. The dataset consists of **OHLCV (Open, High, Low, Close, Volume) Forex data** collected over a **10-year period**.

The key goal is to evaluate whether modern machine learning models can outperform traditional statistical methods in Forex forecasting.

---

## 📂 Repository Structure

```
/Forex-Forecasting-ML
│── README.md                    # Project Overview & Instructions  
│── data/                         # Dataset Folder
│   ├── forex_data.csv            # Raw OHLCV Forex Data
│   ├── Forex_data_feature_added (Garch).csv  # Feature-engineered Dataset
│── notebooks/                     # Jupyter Notebooks for Analysis & Modeling
│   ├── EDA_and_Naive_Model.ipynb   # Exploratory Data Analysis & Naïve Model
│   ├── ARIMA_Model.ipynb           # ARIMA Model Implementation
│   ├── Feature_Engineering.ipynb   # Creating Features (GARCH, RSI, MACD, etc.)
│   ├── LightGBM_Model.ipynb        # LightGBM Model Training & Evaluation
│   ├── LSTM_Model.ipynb            # LSTM Model Training & Evaluation
```

---

## 🛠️ How to Run This Project

### **🔹 Step 1: Clone the Repository**

```bash
git clone https://github.com/your-username/Forex-Forecasting-ML.git
cd Forex-Forecasting-ML
```

### **🔹 Step 2: Install Required Libraries**

Create a virtual environment (optional but recommended):

```bash
python -m venv env
source env/bin/activate  # Mac/Linux
env\Scripts\activate  # Windows
```

Install dependencies:

```bash
pip install -r requirements.txt
```

### **🔹 Step 3: Run the Notebooks in the Following Order**

1️⃣ `EDA_and_Naive_Model.ipynb` → Data visualization, statistical analysis, and Naïve model.  
2️⃣ `ARIMA_Model.ipynb` → Implementation of the ARIMA time series forecasting model.  
3️⃣ `Feature_Engineering.ipynb` → Creating technical indicators and GARCH-based volatility features.  
4️⃣ `LightGBM_Model.ipynb` → LightGBM regression model for Forex price prediction.  
5️⃣ `LSTM_Model.ipynb` → LSTM deep learning model for time series forecasting.  

Run each notebook **sequentially** in Jupyter Notebook or Google Colab.

---

## 📊 Data Description

### **Dataset 1: `forex_data.csv` (Raw Data)**

- **OHLCV (Open, High, Low, Close, Volume)** Forex price data.
- Used for **EDA & ARIMA Model**.

### **Dataset 2: `Forex_data_feature_added (Garch).csv` (Feature-Engineered Data)**

- Contains **technical indicators** like **RSI, MACD, Bollinger Bands**.
- Includes **volatility features** generated using **GARCH models**.
- Used for **LightGBM & LSTM models**.

---

## 🔍 Key Insights

✔ **Advanced ML models did not consistently outperform traditional methods.** While LightGBM and LSTM provided some improvements, they failed to significantly surpass ARIMA and even performed worse than the Naïve baseline in certain cases.  
✔ **The Efficient Market Hypothesis (EMH) plays a role in limiting prediction power.** Since Forex prices exhibit characteristics of a random walk, models struggle to find patterns beyond what is already known.  
✔ **Feature engineering, including GARCH-based volatility modeling, was beneficial but insufficient.** While additional features improved model performance, they did not drastically change the outcome.  
✔ **Walk-forward validation improved reliability.** This method provided a better measure of real-world performance but highlighted the challenges of predictive accuracy in financial markets.  
✔ **Computational limitations impacted LSTM performance.** More advanced tuning and deeper architectures could enhance its results, but constraints prevented full optimization.  

---

## 📌 Future Improvements

🔹 **Incorporate fundamental and macroeconomic data.** Including indicators such as interest rates, inflation, and geopolitical news may help models capture meaningful trends.  
🔹 **Enhance computational resources for deep learning models.** Using more powerful GPUs or cloud-based solutions could allow for deeper LSTM architectures and better hyperparameter tuning.  
🔹 **Explore hybrid models.** Combining ARIMA for short-term trends with deep learning models for capturing non-linear dependencies could yield better results.  
🔹 **Implement ensemble techniques.** Using multiple models in combination, such as blending LightGBM with LSTM, could improve robustness.  
🔹 **Expand validation techniques.** Applying extensive walk-forward validation across all models and testing different feature selection strategies could refine predictive accuracy.  

---

## 📝 Citation

If you use this work, please cite:

```
Hossein Asadi, "Enhancing Forex Forecasting Through Time Series Analysis", MSc Dissertation, University of Chester, October 2024.
```

📌 **Author:** Hossein Asadi  
📌 **Contact:** asadi.hossein90@gmail.com 
📌 **License:** MIT  

---


