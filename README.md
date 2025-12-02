# AI-Based Blood Pressure Prediction from PPG and Demographic Features

**Developed by:** Warda Aziz  
**Project done for:** Leslie Leung  
**Date:** September 27, 2025  

---

## Project Overview
Hypertension is a major global health concern, and continuous blood pressure (BP) monitoring is essential. This project predicts Systolic Blood Pressure (SBP) and Diastolic Blood Pressure (DBP) using photoplethysmogram (PPG) signals and demographic features (age, BMI, heart rate, etc.) from the **PPG-BP dataset**.  

Three models were developed and compared:
- **Random Forest (RF)**  
- **XGBoost (XGB)**  
- **Neural Network (NN)**  

The **Neural Network** achieved the best performance (SBP MAE: 7.1 mmHg, DBP MAE: 5.9 mmHg). SHAP (Shapley Additive Explanations) was used to interpret model predictions, highlighting **age, BMI, and heart rate** as key predictors.

---

## Dataset
- **Original Dataset:** [PPG-BP Dataset – Nature Scientific Data](https://www.nature.com/articles/sdata201820)  
- **Processed Data used in this project:** [Download from Google Drive](https://drive.google.com/uc?export=download&id=1Y01vFJudo4anAiaLh9HRw4MblVdtv249)  
- **License / Terms:** Check the original source for reuse guidelines.

**Features:**
- Demographic: Age, Sex, Height, Weight, BMI  
- Physiological: Heart Rate, SBP, DBP  
- Medical History: Hypertension, Diabetes, Cerebrovascular disease  

> **Note:** For convenience, the processed dataset is included in the `data/` folder when cloned.

---

## Files Included
- `notebooks/AI_BP_Prediction.ipynb` — Jupyter Notebook with full code  
- `report.pdf` — Detailed project report  
- `graphs/` — Folder containing visualizations (accuracy plots, confusion matrix, SHAP plots)  
- `data/` — Folder with the processed dataset (from Google Drive)  
- `requirements.txt` — Python dependencies  

---

## Methodology
1. **Data Preprocessing:** Cleaned, normalized, and encoded features.  
2. **Model Training:** Random Forest, XGBoost, and Neural Network.  
3. **Evaluation Metrics:** MAE, RMSE, R².  
4. **Explainability:** SHAP values for feature importance and model interpretation.  
5. **Visualization:** Scatter plots, feature importance plots, SHAP summary plots, training curves.

---

## Results
- Neural Network performed best with lowest errors:  
  - SBP MAE: 7.1 mmHg  
  - DBP MAE: 5.9 mmHg  
- SHAP analysis revealed age, BMI, and heart rate as the most significant predictors.  
- Visualizations confirmed strong correlation between predicted and actual BP values.  

**Key Observations:**
- Demographics strongly influence BP prediction.  
- Heart rate and medical history improve prediction accuracy.  

---

## Limitations
- Small dataset size (219 participants)  
- Lack of raw PPG waveform features  
- Limited generalizability across populations  

---

## Future Work
- Incorporate raw PPG waveform deep learning models (CNN/LSTM)  
- Use larger datasets for improved generalization  
- Deploy as a real-time wearable or mobile health assistant  

