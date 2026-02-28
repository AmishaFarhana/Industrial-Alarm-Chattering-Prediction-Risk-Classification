# Industrial Alarm Chattering Prediction & Risk Classification

> Built machine learning models to detect alarm chattering in industrial evaporator systems, optimizing anomaly detection while minimizing critical missed alarms.

**Author:** Amisha Farhana Shaik  
**Project Type:** Predictive Maintenance | Classification Modeling | Industrial Analytics  

---

## Business Context

In industrial plants, alarm “chattering” creates alarm floods that distract operators and increase the risk of missing critical failures.  

False negatives (missed chattering events) are especially dangerous — they can lead to equipment damage, safety hazards, or plant shutdowns.

This project develops and compares classification models to accurately predict alarm chattering while minimizing operational risk.

---

## What I Did

### 1️⃣ Built Multiple Classification Models

Developed and compared:

- k-Nearest Neighbors (kNN)
- Decision Trees
- Random Forest
- Gradient Boosting
- Logistic Regression

Target Variable:
- `chb` (chattering alarm indicator)

Dataset included alarm system metrics such as:
- Flow-related measures
- Pressure
- Temperature
- Level
- Time-of-day indicators
- Weekly indicators
- Alarm tag identifiers

---

### 2️⃣ Focused on Critical Evaporator Systems

Restricted analysis to evaporator 1–4 systems (critical plant components).

Best evaporator model:
- kNN (k=6) → **90.13% validation accuracy**
- False Negative Rate: 0.21

This ensured modeling efforts targeted the highest operational impact systems.

---

### 3️⃣ Prioritized High-Risk Alarm Tags

Identified top 10 alarm tags responsible for **58% of chattering events**.

Re-engineered dataset by:
- Encoding high-frequency tags individually
- Grouping remaining tags as “other_alarms”

Best performance:
- kNN (k=4) → **90.5% validation accuracy**

This improved signal strength while reducing noise from rare alarms.

---

### 4️⃣ Applied Category Simplification & Feature Engineering

Reduced unique alarm tag categories from 452 → 52 by simplifying tag structure.

Tested advanced models:

- Random Forest → **91.5% validation accuracy**
- kNN (k=3) → 91% accuracy (FNR: 0.18)
- Logistic Regression → 90% accuracy

Final optimized Decision Tree achieved:
- **91.68% accuracy**
- Strong balance between precision and recall

---

## Model Selection Strategy

Although kNN showed high overall accuracy, false negatives were prioritized due to operational risk.

Logistic Regression with all predictors achieved:
- **Lower False Negative Rate (0.16)**  
- More stable interpretability

This aligns with industrial risk management principles:
> Minimizing missed critical alarms is more important than minimizing false positives.

---

## Model Interpretation

Logistic regression coefficients revealed:

- Higher **temperature** significantly increases chattering risk  
- Higher **flow** reduces probability of chattering  

These insights provide actionable engineering guidance for process monitoring and preventive control.

---

## Business Impact

- Reduced alarm flood risk
- Improved operator focus
- Lower probability of critical failure being missed
- Provided interpretable risk factors for engineering teams
- Enabled data-driven alarm system optimization

---

## Skills Demonstrated

- Classification Modeling (kNN, Trees, RF, Logit)
- Feature Engineering & Category Reduction
- Imbalanced Risk Evaluation (False Negative Minimization)
- Industrial Risk Interpretation
- Model Comparison & Validation
- Predictive Maintenance Analytics

---

This project demonstrates applications in:

Industrial Analytics | Predictive Maintenance | Anomaly Detection | Operational Risk Modeling | Process Optimization
