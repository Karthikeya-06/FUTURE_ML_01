# FUTURE_ML_01
# 🛒 Superstore Sales Analysis & Forecasting

A complete end-to-end data science project analyzing retail sales data from a Superstore dataset. The project covers data cleaning, exploratory data analysis (EDA), feature engineering, machine learning model building, and future sales prediction using a **Random Forest Regressor**.

---

## 📁 Project Structure

```
Superstore_Sales_Dataset/
│
├── Superstore_Sales_Dataset.ipynb   # Main analysis notebook
├── sampledata.csv                   # Source dataset
└── README.md                        # Project documentation
```

---

## 🔧 Libraries & Tools Used

| Library | Purpose |
|---|---|
| `pandas` | Data loading, cleaning, and manipulation |
| `matplotlib` | Data visualization and plotting |
| `seaborn` | Statistical visualizations |
| `scikit-learn` | Machine learning model building & evaluation |
| `numpy` | Numerical computations |

---

## 📋 Workflow Overview

### 1. Data Loading & Preprocessing
- Loaded CSV with `latin1` encoding
- Converted `Order Date` and `Ship Date` columns to `datetime` format
- Removed null values and duplicate rows

### 2. Feature Engineering
- Extracted `Year` and `Month` from `Order Date` for time-series modeling

### 3. Exploratory Data Analysis (EDA)
Interactive visualizations were generated to uncover trends and patterns in the data.

### 4. Model Building
- Features: `Year`, `Month`
- Target: `Sales`
- Algorithm: **Random Forest Regressor**
- Train/test split: 80/20

### 5. Evaluation
- Metric: **Mean Absolute Error (MAE)**

### 6. Prediction
- Model can forecast future sales by specifying a target `Year` and `Month`

---

## 📊 Visualizations
### 📅 Yearly Sales Overview

Bar chart showing the total sales performance for each year in the dataset.

![Yearly Sales](plot_yearly_sales.png)
<img width="1200" height="750" alt="plot_yearly_sales" src="https://github.com/user-attachments/assets/12c571a7-e3b4-4534-b759-73fc1b15d355" />

---

### 🤖 Actual vs Predicted Sales
Comparison of actual sales values against the Random Forest model's predictions on the test set.

![Actual vs Predicted](plot_actual_vs_predicted.png)
<img width="1500" height="750" alt="plot_actual_vs_predicted" src="https://github.com/user-attachments/assets/3cc49eb5-9a07-4fa2-9651-66fda6973ad1" />

---

## 🚀 How to Run

1. **Clone or download** the repository.
2. Install dependencies:
   ```bash
   pip install pandas matplotlib seaborn scikit-learn numpy
   ```
3. Place `sampledata.csv` in the same directory as the notebook.
4. Open and run `Superstore_Sales_Dataset.ipynb` in Jupyter Notebook or JupyterLab.

---

## 🔮 Future Prediction Example

```python
future = pd.DataFrame({
    'Year': [2026],
    'Month': [7]
})

predicted_sales = model.predict(future)
print(f"Predicted Sales for July 2026: ${predicted_sales[0]:.2f}")
```

---

## 📌 Key Insights

- **Seasonal trends** are visible in monthly sales, with certain months consistently outperforming others.
- **Technology** tends to have higher individual sales values, while **Office Supplies** drive volume.
- The **Random Forest model** provides a baseline for sales forecasting, which can be improved with additional features like promotions, holidays, and product-level data.

---

## 📄 License

This project is for educational and analytical purposes.
