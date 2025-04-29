# ElevateLabs Internship 
## Task 4: Logistic Regression

## 📌 Objective
Build a binary classification model using **Logistic Regression** to predict whether a tumor is **malignant** or **benign** using the Breast Cancer dataset.

---

## 📁 Dataset
- Source: UCI Machine Learning Repository
- Features: 30 numerical attributes (mean, standard error, worst) of cell nuclei
- Target: `diagnosis` — **M (Malignant)** or **B (Benign)**

---

## ✅ Steps Performed

1. **Data Preprocessing**
   - Removed unnecessary columns (`id`, `Unnamed: 32`)
   - Encoded target: `M` → 1, `B` → 0

2. **Train-Test Split & Scaling**
   - Scaled features using `StandardScaler`
   - Split into 80% training and 20% testing sets

3. **Logistic Regression Model**
   - Trained a logistic regression model using `sklearn.linear_model.LogisticRegression`

4. **Evaluation Metrics (Before Threshold Tuning)**
   - **Confusion Matrix:**
     ```
     [[70  1]
      [ 2 41]]
     ```
   - **Classification Report:**
     ```
                      precision    recall  f1-score   support

             0          0.97      0.99      0.98        71
             1          0.98      0.95      0.96        43

      accuracy                              0.97       114
     macro avg          0.97      0.97      0.97       114
     weighted avg       0.97      0.97      0.97       114
     ```
   - **ROC-AUC Score:** 1.00

5. **Threshold Tuning & Sigmoid Function**
   - Used sigmoid output (probabilities) from logistic regression
   - Tuned decision threshold to observe its effect on prediction

   **After Threshold Change (Custom threshold):**
   - **Confusion Matrix:**
     ```
     [[67  4]
      [ 1 42]]
     ```

---

## 🔧 Tools Used
- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib
