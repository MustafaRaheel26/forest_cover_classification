# Forest Cover Type Classification 🌲

## 📌 Project Overview
This project predicts the **type of forest cover** based on cartographic and environmental features.  
We use the **Covertype dataset (UCI ML Repository)** and apply multi-class classification models to evaluate performance.

---

## ⚙️ Tools & Libraries
- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- XGBoost  
- Matplotlib / Seaborn  

---

## 📂 Dataset
- Source: [Covertype Dataset (UCI ML Repository)](https://archive.ics.uci.edu/ml/datasets/covertype)  
- Rows: 581,012  
- Features: 54 cartographic/environmental variables  
- Target: `Cover_Type` → 7 forest categories  

---

## 🛠️ Steps
1. **Data Loading & Exploration**
   - Loaded dataset
   - Assigned feature names manually
   - Checked class distribution

2. **Preprocessing**
   - Encoded categorical features (`Wilderness_Area`, `Soil_Type`)
   - Standardized numerical features
   - Shifted labels (1–7 → 0–6) for XGBoost compatibility

3. **Model Training (Multi-class)**
   - Logistic Regression
   - Decision Tree
   - Random Forest
   - XGBoost

4. **Evaluation**
   - Accuracy, Precision, Recall, F1-score (macro & micro averages)
   - Confusion Matrix
   - Feature Importance (tree-based models)

5. **Imbalance Handling**
   - Applied **SMOTE** to oversample minority classes

---

## 📊 Results
- **Random Forest & XGBoost** achieved the best accuracy  
- Logistic Regression struggled due to high dimensionality  
- SMOTE improved recall for underrepresented classes  

---

## 🚀 How to Run
### In Google Colab
1. Upload this notebook (`Forest_cover_type.ipynb`) to Colab  
2. Run all cells sequentially  
3. Results (confusion matrix, feature importance) will be displayed  

### Locally
```bash
git clone https://github.com/MustafaRaheel26/forest-cover-classification.git
cd forest-cover-classification
pip install -r requirements.txt
jupyter notebook forest_cover_classification.ipynb
