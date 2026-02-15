# ✈️ A/B Test Analysis: Search Ranking System Optimization

## 📌 Project Overview
This project evaluates the impact of a newly developed search ranking algorithm for a leading Online Travel Agency (OTA). The primary goal was to determine if the new system improves the **Conversion Rate (CVR)** without negatively impacting the **Time to Book** (Guardrail Metric). 

The analysis provides a data-driven "Go/No-Go" recommendation for the product's full rollout based on rigorous statistical testing.

## 📊 Business Problem
The Product team wants to improve how travel options are ranked in search results. A full rollout is contingent on:
1.  **Primary Metric:** A statistically significant increase in the Conversion Rate.
2.  **Guardrail Metric:** No significant increase in the average Time to Book (to ensure user experience isn't compromised).

## 📁 Dataset Description
* `users_data.csv`: Contains user-level information including the group assignment (`Control` vs. `Variant`).
* `sessions_data.csv`: Session-level data tracking bookings and the time taken to complete a booking.

## 🛠️ Analysis Workflow
### 1. Data Integrity & SRM Check
* Performed **Sample Ratio Mismatch (SRM)** validation using a Chi-squared test to ensure the randomization process was not biased.

### 2. Hypothesis Testing (Primary Metric)
* **Metric:** Conversion Rate (Bookings / Total Sessions).
* **Test:** Two-sample **Z-test** for proportions.
* **Confidence Level:** 90% Confidence Interval.

### 3. Guardrail Monitoring (Secondary Metric)
* **Metric:** Average Time to Book.
* **Test:** Two-sample **T-test** to compare the means of the Control and Variant groups.

### 4. Data Visualization
* Visualized distribution of booking times and conversion lifts across groups using Seaborn and Matplotlib.

## 🚀 Key Findings

* **SRM Validation:** **Passed** (P-value: `0.66`). 
    * *Interpretation:* Since p > 0.05, there is no evidence of Sample Ratio Mismatch, meaning the randomization was successful and the groups are comparable.
* **Conversion Lift:** The new ranking system delivered a **14.2%** increase in conversion rate.
* **Statistical Significance:** **Highly Significant** (P-value ≈ `0.00`).
    * *Interpretation:* We can say with nearly 100% confidence that the observed improvement is not due to chance.
* **Guardrail Check:** **Successful**. The "Time to Book" was actually **reduced**, which indicates that the new system helps users find and book travel options faster, improving the overall user experience.

## 💡 Recommendation: GO 🟢
**Decision: Full Rollout**

The A/B test results are conclusive. The new search ranking system significantly improves the primary business metric (Conversion) while simultaneously optimizing the guardrail metric (Time to Book). Given the 14.2% lift and the high statistical significance, I recommend a 100% rollout to all users.


---
**Author:** [Youssef Ahmed](https://github.com/youssef-ahmed7373)  
**Role:** Data Scientist