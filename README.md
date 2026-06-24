<img width="1996" height="600" alt="Designer (2)" src="https://github.com/user-attachments/assets/46442ea4-fe56-4576-8455-11f6818ba441" />


---

## 📌 Project Overview  
This project analyzes the results of an A/B test conducted by an e‑commerce company to determine whether a new website variation improves user engagement and conversions.  
The goal is to evaluate experiment integrity, measure lift, and provide clear, data‑driven recommendations.

This project demonstrates my ability to:
- Design and evaluate controlled experiments  
- Clean and prepare experiment datasets  
- Perform statistical testing (t‑tests, proportions tests)  
- Interpret results and communicate insights clearly  
- Build a reproducible Python analysis workflow  

---

## 🗂️ Dataset Description  
The dataset includes user‑level experiment data with the following fields:

- **user_id** — unique visitor identifier
- **timestamp** — visit time 
- **group** — A (control) or B (treatment) 
- **landing_page** — control (A) → old page
                     treatment (B) → new page 
- **converted** — whether the user completed the target action(binary: 1=Yes, 0=No)
  

---

## 🧹 Data Cleaning & Preparation  
Key steps performed:

- Removed duplicate user IDs — One user appeared twice (repeat visits). Since the experiment unit is the user, not the session, I kept                                only the first occurrence to ensure each user is counted once.
- Ensured proper group assignment — Verified that control users saw old_page and treatment users saw new_page; removed mismatched rows.
- Checked for timestamp anomalies — Converted timestamps to datetime and validated that traffic patterns over time were consistent.
- Validated sample ratio (SRM check) — Confirmed that control and treatment groups were split as expected.
- Standardized categorical fields — Ensured consistent formatting for group, landing_page, and converted.
- Created derived metrics — Computed conversion rates, lift, confidence intervals, and time‑based metrics for analysis.

---

## 📊 Experiment Evaluation  
### 1. **Sample Ratio Mismatch (SRM)**  
- Verified whether the actual A/B split matched the expected allocation  
- Ensured randomization integrity before proceeding with analysis  

### 2. **Conversion Rate Analysis**  
- Calculated conversion rates for both groups  
- Visualized differences using bar charts and confidence intervals  

### 3. **Statistical Testing**  
Performed hypothesis testing to determine whether the observed lift is statistically significant:

- **Two‑sample t‑test** (continuous metrics, if applicable)  
- **Two‑proportion z‑test** (conversion rate comparison)  
- **95% confidence intervals** for lift estimation  

---

## 📈 Key Findings  
- **Relative Lift:** –1.33% (Treatment performed slightly worse than control)
- **Statistical Significance:** No
- **p‑value:** 0.4869
- **95% Confidence Interval**: –0.0056 to 0.0027

## 📌 Interpretation
The treatment group showed a small decrease in conversion (–1.33%), but the difference is not statistically significant.
The confidence interval crosses zero and the p‑value is well above 0.05, indicating that the observed difference is likely due to random variation rather than a true effect.


## 🧠 Conclusion
The experiment does not provide evidence that the treatment outperforms the control.
A follow‑up test with improved experiment design or a larger effect size may be needed to detect meaningful differences.

---

## 🛠️ Tools & Technologies  
- **Python** (Pandas, NumPy, SciPy, Statsmodels)  
- **Matplotlib / Seaborn** for visualization  
- **Jupyter Notebook / Google Colab**  
- **GitHub** for version control  

---

## 🚀 How to Reproduce  
1. Clone the repository  
2. Install dependencies  
3. Open the notebook  
4. Run all cells to reproduce the analysis  

---

## 📬 Contact  
If you’d like to discuss this project or my work:  
**Aleksandra Burmester**   
LinkedIn: *https://www.linkedin.com/in/aleksandra-burmester-1823b72a/*  

