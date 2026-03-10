# ✈️ Airline Time Series Analysis and Forecasting

## 📌 Project Overview
Airline demand changes over time due to factors such as seasonality, economic trends, and travel patterns. Understanding these patterns is important for airlines to optimize scheduling, manage capacity, and improve operational efficiency.

This project performs **time series analysis on historical airline passenger data** to identify trends, analyze seasonal patterns, and forecast future passenger demand using statistical forecasting models.

The analysis uses the **SARIMA (Seasonal AutoRegressive Integrated Moving Average)** model to capture both trend and seasonal components in the data.

---

## 🎯 Objectives

The main objectives of this project are:

- Analyze airline passenger trends over time
- Identify seasonal patterns in passenger traffic
- Test stationarity of the time series
- Apply differencing to stabilize the data
- Build a **SARIMA forecasting model**
- Forecast future airline passenger demand
- Evaluate model performance using **RMSE**

---

## 📊 Datasets Used

### 1️⃣ AirPassengers Dataset

This dataset contains **monthly totals of international airline passengers** from **1949 to 1960**.

| Column | Description |
|------|-------------|
| Month | Date of observation |
| Passengers | Number of airline passengers |

**Total Observations:** 144

This dataset is widely used for **time series forecasting demonstrations**.

---

### 2️⃣ US Airline Flight Dataset

This dataset contains **flight operation information** including airports, delays, and flight activity.

Key columns include:

| Column | Description |
|------|-------------|
| FL_DATE | Flight date |
| ORIGIN_AIRPORT | Departure airport |
| DEST_AIRPORT | Destination airport |
| ARR_DELAY | Arrival delay (minutes) |
| DEP_DELAY | Departure delay |

**Total Records:** ~1.2 million flights

This dataset was used for **data exploration and operational context**.

---

## 🛠️ Technologies Used

- **Python**
- **Pandas** – Data manipulation
- **NumPy** – Numerical computing
- **Matplotlib** – Data visualization
- **Statsmodels** – Time series modeling
- **pmdarima** – Auto ARIMA model selection
- **Scikit-learn** – Model evaluation

---

## 🔎 Project Workflow

The project follows a standard **time series analysis pipeline**.

### 1️⃣ Data Loading
Import datasets and convert date columns into time series format.

### 2️⃣ Data Inspection
- Check dataset structure
- Examine dataset size
- Review sample records

### 3️⃣ Data Cleaning
- Handle missing values
- Remove incomplete records
- Ensure proper time indexing

### 4️⃣ Time Series Visualization
Passenger counts are plotted to observe:
- Long-term trends
- Seasonal patterns

---

### 5️⃣ Rolling Statistics
Rolling mean and rolling standard deviation are calculated to observe variations over time.

---

### 6️⃣ Seasonal Decomposition
The time series is decomposed into:

- **Trend**
- **Seasonal component**
- **Residual component**

This helps understand underlying patterns in airline passenger traffic.

---

### 7️⃣ Stationarity Testing
The **Augmented Dickey-Fuller (ADF) Test** is applied to determine whether the time series is stationary.

Since the original series is **non-stationary**, differencing is applied.

---

### 8️⃣ Differencing
Differencing is used to stabilize the mean of the time series and remove trend components.

---

### 9️⃣ ACF and PACF Analysis
Autocorrelation and partial autocorrelation plots are used to determine suitable parameters for the SARIMA model.

---

### 🔟 SARIMA Model Building
A **Seasonal ARIMA model** is built using `auto_arima` to automatically determine the best parameters.

Best model selected:

SARIMA(2,1,1)(0,1,0)[12]

This model captures both:

- Non-seasonal components
- Seasonal patterns in monthly data

---

### 1️⃣1️⃣ Forecasting
The trained model is used to forecast **future passenger demand for the next 24 months**.

Forecast results show expected passenger trends based on historical patterns.

---

### 1️⃣2️⃣ Model Evaluation
Model performance is evaluated using **Root Mean Squared Error (RMSE)**.

RMSE ≈ 55

This indicates the model provides a **reasonable forecasting accuracy**.

---

## 📈 Key Insights

- Airline passenger traffic shows a **clear upward trend** over time.
- Strong **seasonal patterns** are observed in passenger demand.
- The SARIMA model effectively captures both **trend and seasonality**.
- Forecasting helps airlines plan **capacity, scheduling, and operations**.

---

## 📂 Project Structure

```
Airline-Time-Series-Analysis/
│
├── Airline_Time_Series_Analysis.ipynb
├── Air_Passengers.csv
├── Airline_dataset.csv
├── README.md

```

---

## 🚀 How to Run the Project

### 1️⃣ Clone the repository

git clone https://github.com/Keerthana-gopal29/Airline-Time-Series-Analysis-and-Forecasting.git

### 2️⃣ Install required libraries

pip install pandas numpy matplotlib statsmodels pmdarima scikit-learn

### 3️⃣ Run the Jupyter Notebook

jupyter notebook

Open the notebook and run all cells to reproduce the analysis.

---

## 📌 Future Improvements

Possible improvements for this project include:

- Adding more recent airline passenger datasets
- Comparing SARIMA with **Prophet or LSTM models**
- Building an **interactive dashboard**
- Incorporating external factors such as weather and economic indicators

---

## 👩‍💻 Author

**Keerthana Gopal**

Aspiring **Data Analyst / Data Scientist**

---

⭐ If you found this project useful, feel free to **star the repository**.
