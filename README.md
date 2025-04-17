# Programming-For-Data-Science-UOL-
# Flight Delay Analysis – Summary of Insights & Machine Learning

This project analyzes U.S. domestic flight data (2000–2004) to uncover insights on flight delays and builds a machine learning model to predict the likelihood of delay based on time, date, and aircraft features.

---

## Part 1: Best Day of the Week to Travel (Minimizing Delays)

**Objective:**  
Identify which days of the week have the least and most average flight delays over time.

**Methodology:**
- Grouped the data by `Year` and `DayOfWeek`
- Calculated the **average total delay**
- Visualized results using bar charts

**Findings:**
- **Tuesdays and Wednesdays** had the **lowest average delays**
- **Fridays and Sundays** consistently had the **highest average delays**



---

## Part 2: Best Time of Day to Travel

**Objective:**  
Analyze how the **time of day** and **day of week** affect flight delays.

**Methodology:**
- Divided flight times into **3-hour intervals** (e.g. 0600–0859 hrs)
- Created a **pivot table** and a **heatmap** showing mean delays by time slot and day
- Ranked combinations by average delay

**Findings:**
- **Early morning flights (before 9 AM)** have the **least delays**
- **Evening flights (after 3 PM)** generally show **higher delays**
- **Monday mornings** and **Friday afternoons** had some of the highest delays

---

## Part 3: Predicting Flight Delays Using Machine Learning

**Objective:**  
Build a predictive model to determine whether a flight will be delayed using historical flight data.

**Steps:**

1. **Feature Engineering:**
   - Created a binary target: `DelayIndicator` (`1` if delay > 15 mins, else `0`)
   - Input features: `Year`, `DayOfWeek`, `TimeInterval`, `Aircraft Age`

2. **Preprocessing:**
   - Categorical features were one-hot encoded (`DayOfWeek`, `TimeInterval`)
   - Numerical features (like aircraft age) were standardized using `StandardScaler`

3. **Balancing the Dataset:**
   - Used **SMOTE (Synthetic Minority Over-sampling Technique)** to balance delayed and non-delayed flight samples

4. **Model Training & Evaluation:**
   - Model: **Logistic Regression**
   - Evaluation Metrics:
     - **ROC Curve**
     - **AUC Score** for classification performance

**Outcome:**
- The trained model effectively predicts whether a flight will be delayed
- Provides valuable insights for travelers and airline operations

---

## Tools & Libraries Used

- **Python**, **Pandas**, **NumPy**
- **Seaborn**, **Matplotlib** – for data visualization
- **Scikit-learn (sklearn)** – for model building and evaluation
- **imblearn** – for SMOTE oversampling
- **Statsmodels** – for statistical exploration

---

> This project provides both data-driven insights and a predictive solution for minimizing the risk of flight delays. Ideal for travelers, airline planners, and anyone interested in transportation analytics.

