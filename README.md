# 📊 Megaline Plan Recommendation Model

## 📌 Project Overview
This project predicts whether a **Megaline** mobile subscriber should be recommended the **Smart** or **Ultra** plan based on their monthly usage patterns.

The task was to build a classification model with at least **75% accuracy** on unseen data.

---

## 📂 Dataset
**Source:** Provided as part of the Intro to Machine Learning course.

Each row contains:
- `calls` — Number of calls
- `minutes` — Total call duration (minutes)
- `messages` — Number of text messages
- `mb_used` — Internet traffic used (MB)
- `is_ultra` — Target variable:  
  - `0` = Smart plan  
  - `1` = Ultra plan

**Class balance:**
- Smart: ~69%
- Ultra: ~31%

---

## 🛠 Project Workflow
1. **Data Exploration & Preprocessing**  
   - Checked for missing values (none found)  
   - Analyzed distributions & class balance  
   
2. **Data Splitting**  
   - 60% Training  
   - 20% Validation  
   - 20% Test  
   - Stratified to preserve class balance  

3. **Model Training & Comparison**  
   - Decision Tree Classifier  
   - Random Forest Classifier  
   - Logistic Regression  

4. **Hyperparameter Tuning**  
   - Decision Tree: `max_depth`  
   - Random Forest: `max_depth`, `n_estimators`  

5. **Final Model Selection**  
   - Best model: **Random Forest** with `max_depth=8`, `n_estimators=10`

---

## 📈 Results
| Model              | Validation Accuracy | Test Accuracy |
|--------------------|---------------------|---------------|
| Decision Tree      | 81.65%              | —             |
| Random Forest      | **83.20%**          | **81.49%**    |
| Logistic Regression| (lower)             | —             |

- **Baseline accuracy** (majority class): **69.36%**  
- Model improved accuracy by over **12 percentage points**.

---

## 💡 Key Takeaways
- Hyperparameter tuning and proper data splitting are essential for reliable results.
- Always compare to a baseline to prove the model’s value.
- Random Forest is a strong choice for classification problems with mixed feature importance.

---
