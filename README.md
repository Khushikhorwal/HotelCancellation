# Hotel Booking Cancellation Prediction

This project focuses on analyzing and predicting hotel booking cancellations using machine learning techniques. The goal is to understand booking behavior and develop a model that can accurately predict whether a booking will be canceled or not.

## Dataset

The dataset contains **14,684 rows** and **32 columns** and includes features such as:
- Booking details (lead time, stay duration, etc.)
- Guest details (adults, children, babies)
- Reservation information (meal type, room type, market segment)
- Target: `is_canceled` (1 = canceled, 0 = not canceled)

> Note: Dataset includes missing values that were handled during preprocessing.

## 🛠️ Features Created

- `total_guests`: Sum of adults, children, and babies.
- `is_family`: 1 if children or babies > 0, else 0.
- `lead_time_bucket`: Categorical bucket based on lead time (Short, Medium, Long).

##  Data Preprocessing

- Missing values handled with appropriate strategies (e.g., fillna with 0 or "Unknown").
- Categorical columns label encoded.
- Dropped unnecessary or leakage-prone columns:
  - `arrival_date_*`, `agent`, `company`, `country`, `reservation_status`, `reservation_status_date`

##  Train-Test Split

- 80/20 split using `train_test_split`
- Stratified by `is_canceled` to maintain class distribution

| Split      | Rows   |
|------------|--------|
| Training   | 11,747 |
| Testing    | 2,937  |

Class distribution in both sets:
- ~69% canceled (`1`)
- ~31% not canceled (`0`)

## 📊 Model Building (To Be Added)

*Planned models:*
- Logistic Regression
- Random Forest
- XGBoost
- Evaluation using accuracy, precision, recall, F1-score, ROC-AUC

## 📦 Requirements

- Python 3.x
- pandas
- numpy
- scikit-learn
- matplotlib / seaborn (for visualization, optional)

Install dependencies with:
```bash
pip install -r requirements.txt
