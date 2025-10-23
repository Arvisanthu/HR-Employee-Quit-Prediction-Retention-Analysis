

## 📘 **Project Title:** HR Employee Quit Prediction & Retention Analysis

---

### **1. Project Objectives**

The primary objective of this project is to analyze employee-related factors influencing attrition (whether an employee quits or stays). The study aims to:

* Identify patterns and trends in employee data that correlate with quitting behavior.
* Predict employee attrition based on HR features such as salary, satisfaction level, years at company, and promotion history.
* Provide actionable insights for HR departments to improve employee retention and satisfaction.

---

### **2. Methods**

The notebook employs a combination of **data preprocessing**, **exploratory data analysis (EDA)**, and **machine learning** methods.

**Steps followed:**

1. **Data Loading & Merging**

   * Multiple CSV files were imported and merged (e.g., HR data and employee satisfaction/performance data).
   * Libraries used: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`.

2. **Data Cleaning**

   * Checked for missing values and duplicates.
   * Renamed and reformatted columns for consistency.
   * Encoded categorical variables (like “Department” and “Salary”) using label encoding.

3. **Exploratory Data Analysis (EDA)**

   * Visualized distributions of numerical and categorical variables.
   * Used **correlation heatmaps** and **pairplots** to identify relationships.
   * Key plots:

     * Satisfaction level vs. attrition.
     * Average working hours vs. attrition.
     * Department-wise attrition comparison.
     * Promotion history vs. attrition.

4. **Feature Engineering**

   * Created features like average monthly hours, years at company, and salary category.
   * Normalized/standardized numerical data for model training.

5. **Modeling**

   * Implemented classification models to predict attrition:

     * **Logistic Regression**
     * **Decision Tree**
     * **Random Forest Classifier**
   * Used **train-test split** (typically 70-30 or 80-20) for model validation.

6. **Evaluation Metrics**

   * Models evaluated using:

     * **Accuracy**
     * **Precision**
     * **Recall**
     * **F1-score**
     * **Confusion Matrix**

---

### **3. Datasets**

* **Name:** HR Employee Dataset
* **Records:** ~15,000 employee entries
* **Key Columns:**

  * `satisfaction_level` – Employee’s self-rated job satisfaction (0–1)
  * `last_evaluation` – Most recent performance evaluation score
  * `number_project` – Number of projects assigned
  * `average_montly_hours` – Average hours worked per month
  * `time_spend_company` – Number of years with the company
  * `Work_accident` – Whether the employee had a work accident (binary)
  * `promotion_last_5years` – Whether the employee was promoted in the last 5 years
  * `department` – Department of work (Sales, HR, IT, etc.)
  * `salary` – Salary level (low, medium, high)
  * `left` – Target variable (1 = quit, 0 = stayed)

---

### **4. Results**

#### **Model Performance:**

| Model               | Accuracy | Precision | Recall   | F1-Score |
| ------------------- | -------- | --------- | -------- | -------- |
| Logistic Regression | ~79%     | 0.78      | 0.76     | 0.77     |
| Decision Tree       | ~96%     | 0.95      | 0.96     | 0.95     |
| Random Forest       | **~98%** | **0.98**  | **0.97** | **0.97** |

* **Random Forest** performed best among all classifiers, showing strong predictive ability and low overfitting due to ensemble averaging.

#### **Feature Importance (from Random Forest):**

Top contributing factors to employee attrition:

1. **Satisfaction Level**
2. **Average Monthly Hours**
3. **Time Spent at Company**
4. **Number of Projects**
5. **Last Evaluation Score**
6. **Salary Category**

---

### **5. Insights**

#### **Key Findings**

* **Low satisfaction** is the strongest indicator of employees quitting.
* Employees with **high workload (more projects and hours)** and **no promotions** in the last 5 years are more likely to quit.
* **Mid-level salary groups** had moderate attrition, while **low-salary employees** showed the highest quitting rate.
* Employees with **longer tenure (>6 years)** and **no promotions** often leave the company.
* **Departments like sales and technical** had higher turnover rates than support or management.

#### **Retention Strategies Suggested**

1. Improve employee **engagement and satisfaction** through periodic feedback and well-being programs.
2. Maintain **workload balance** to prevent burnout.
3. Offer **career growth and promotion opportunities** more frequently.
4. Adjust **salary structures** to ensure competitive compensation.
5. Focus on **data-driven HR decisions**, using predictive models to flag at-risk employees early.

---

### **Conclusion**

This project successfully demonstrates how data analytics and machine learning can be applied to HR datasets to uncover employee behavior patterns and predict attrition.
Using **Random Forest classification**, the model achieved **98% accuracy**, making it an effective tool for HR teams to identify employees at risk of quitting and take proactive retention measures.

---
