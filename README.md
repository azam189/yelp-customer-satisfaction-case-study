# yelp-customer-satisfaction-case-study
# 📍 Predicting Restaurant Check-Ins Using Yelp Data


# 🎯 Business Objective

* Identify the key drivers of restaurant check-in behavior
* Assess whether restaurant features (e.g., outdoor seating, parking) and external factors (weather, demographics) influence customer visits
* Evaluate the predictability of check-ins using machine learning models
* Translate analytical findings into **actionable business recommendations**

---

## 📊 Data Sources

### Primary Data

* **Yelp Academic Dataset**

  * Business
  * Reviews (reduced dataset for efficiency)
  * Check-ins
  * User, Tips, Photos (contextual)

Scope: Restaurants located in **Missouri**, selected for high weather variability.

### External & Enriched Data

* **Weather data** (Open-Meteo API): temperature, precipitation, humidity
* **Demographic data**: median age at county level
* **Business proximity metric** (custom engineered): competitive density of nearby restaurants

---

## 🔍 Analytical Approach

### 1. Data Preparation

* Filtering relevant restaurant businesses
* Cleaning and standardizing large-scale platform data
* Feature engineering (e.g., proximity, capped/scaled proximity)

### 2. Exploratory & Correlation Analysis

* Evaluated relationships between check-ins and:

  * Business attributes
  * Weather conditions
  * Demographics

### 3. Hypothesis Testing (Regression)

* **H1:** Outdoor seating impacts daily check-ins, moderated by weather and age
* **H2:** Parking garage availability impacts daily check-ins, moderated by weather and age

### 4. Machine Learning Models

Tested multiple models to predict daily check-ins:

* Linear Regression
* Random Forest
* Gradient Boosting
* **LightGBM (best-performing model)**

Evaluation metrics:

* MAE, MSE, RMSE
* R²

---

## 💡 Key Insights

* Individual restaurant attributes (e.g., outdoor seating, parking) show **limited standalone predictive power**
* External factors like weather and demographics alone are insufficient to explain check-in behavior
* **Daily review count** emerged as the most important predictor in feature importance analysis
* Customer engagement signals (reviews, activity) matter more than static attributes

---

## 📈 Business Implications & Recommendations

### For Restaurant Owners

* Actively encourage customers to leave reviews and interact online
* Treat digital engagement as a driver of physical foot traffic
* Focus less on single features and more on the overall customer experience

### For Investors & Analysts

* Check-in data can complement revenue and footfall estimates
* Review activity is a strong leading indicator of restaurant performance

### For Platform Strategy

* Improving review visibility and engagement tools can indirectly boost offline visits

---

## ⚠️ Limitations

* Check-ins used as a single KPI for customer satisfaction
* Limited sample size (state-level focus)
* Only one external factor (weather) included
* Some ambiance-related variables treated as control variables

---

## 🔮 Next Steps

* Incorporate **sentiment analysis** of review text
* Add additional external variables (events, pricing, competition trends)
* Explore causal inference approaches
* Extend analysis to multiple states or cities

---

## 🛠 Tech Stack

* Python (Pandas, NumPy, Scikit-learn, LightGBM)
* PostgreSQL
* API integration (Open-Meteo)
* Data visualization & exploratory analysis

---

## 📌 Why This Project Matters for Employers

This project simulates a real-world data science workflow:

* Translating noisy platform data into business insight
* Combining structured & unstructured data
* Balancing statistical rigor with practical decision-making
* Communicating results to non-technical stakeholders

