# Intern Performance Prediction Model 🎯

##  Problem Statement:
Organizations often struggle to evaluate intern performance objectively.  
This project builds a **machine learning model** to classify interns into categories:
- Struggle
- Average
- Excel

based on features like task completion time, feedback rating, attendance, and performance score.

---

##  Dataset:
- **Size:** 6000 interns  
- **Features:**
  - `task_completion_time_hrs` (continuous)
  - `feedback_rating` (continuous)
  - `attendance_percent` (continuous)
  - `performance_score` (continuous)
- **Target:** `performance_category` (categorical)

---

##  Methodology:
1. **Exploratory Data Analysis (EDA)**  
   - Distribution plots, pairplots, correlation heatmap  
2. **Preprocessing**  
   - Train/Validation/Test split  
   - Stratified sampling for balanced categories  
3. **Modeling**  
   - Random Forest Classifier (baseline)  
   - Hyperparameter tuning with validation set  
4. **Evaluation**  
   - Confusion Matrix  
   - Classification Report (Precision, Recall, F1-score)  
   - Cross-validation for robustness  
5. **Feature Importance**  
   - Visualized to understand drivers of performance  

---

##  Results:
- **Validation Accuracy:** ~XX%  
- **Test Accuracy (Unseen Data):** ~YY%  
- Confusion matrix shows balanced predictions across categories.  
- Feature importance highlights `feedback_rating` and `performance_score` as key drivers.

---

##  Real-Time Prediction:
You can input intern data and get instant predictions:

```python
# Example: Real-time prediction
new_data = pd.DataFrame({
    'task_completion_time_hrs':[12],
    'feedback_rating':[4.5],
    'attendance_percent':[92],
    'performance_score':[78]
})

prediction = rf.predict(new_data)
print("Predicted Performance Category:", prediction[0])
# intern-performance-prediction
Machine Learning project to classify intern performance using Random Forest
