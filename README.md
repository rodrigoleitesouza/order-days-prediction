# 🧠 Predictive Modeling: Remaining Order Days

**Author:** Rodrigo Santos de Souza  

---

## 🎯 Objective

Predict the number of remaining order days during **August 2022** using historical transaction patterns. The main goal is to **optimize logistics allocation** by providing reliable forecasts for each user.

> 🔄 The model generates a `.csv` file with predictions for **32,944 users**.

---

## 🛠️ Technologies Used

- Python 3.10+
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Jupyter Notebook
- Parquet file format
- Git & GitHub

---

## 🗂️ Project Structure

The notebook is divided into clearly commented sections to facilitate understanding and replication:

1. **Imports and Setup**  
   Essential libraries for data manipulation, visualization, and machine learning (pandas, numpy, matplotlib, scikit-learn).

2. **Data Loading and Exploratory Data Analysis (EDA)**  
   Loads three `.parquet` files containing:
   - Historical order data  
   - Partial data for August  
   - Sales forecasts for August  
   Includes the `eda_report()` function for automated dataset analysis (dimensions, missing values, data types).

3. **Feature Engineering**  
   Creation of features based on:
   - Recency and frequency of orders  
   - Last order date per user  
   - Weekly trends and moving averages  

4. **Predictive Modeling**  
   - Algorithm used: `RandomForestRegressor`  
   - Validation strategy: `TimeSeriesSplit`  
   - Metric: `Mean Absolute Error (MAE)`  

5. **Cross-Validation and Results**  
   Evaluation of fold scores and analysis of prediction errors.

6. **Exporting Results**  
   Creates and saves the `order_days_prediction.csv` file with the final results per `account_id`.

---

## 🔍 Technical Highlights

- ✅ **Random Forest Regressor** with basic tuning  
- ✅ **Temporal cross-validation**, respecting the sequential nature of the data  
- ✅ **Automated EDA** using a modular function  
- ✅ Reproducible results with fixed random seed  

---

## 🧪 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/rodrigoleitesouza/order-days-prediction
   cd order-days-prediction
   ```

2. Install the dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the notebook:
   Open the `.ipynb` file in Jupyter Notebook, JupyterLab, or VSCode and execute it cell by cell.

> 📦 Make sure the required `.parquet` files are in the correct folder as specified in the notebook.

---

## 📁 Output

The file generated at the end of execution is:

```
order_days_prediction.csv
```

| account_id | prediction |
|------------|------------|
| 12345      | 4.00       |
| 67890      | 2.00       |

---

## 🧠 Final Thoughts

This project demonstrates a robust approach to forecasting customer behavior using modern machine learning techniques and time-series-based validation.

Feel free to open an issue or contribute improvements!

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).
