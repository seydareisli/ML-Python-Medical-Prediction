# PREDICTING MEDICAL OUTCOMES with MACHINE LEARNING
_by Seyda Reisli | seydareisli@ gmail.com
---

In this repo, I utilize Python's scikit-learn and machine learning techniques to predict medical outcomes, specifically strokes. The dataset I work with contains history of patient visits with respective time points in addition to patient demographics. Through visual data exploration, data preprocessing, and the application of various machine learning models, I explore best techniques to predict potential stroke incidents. 

## DATA EXPLORATION STEP:
- Started by clinical thinking and lit research to hypothesize informative dataset features.
- Visualized clinical events vs. time stamps to understand temporal patterns.
- Discovered patterns. E.g., stroke hospitalizations happen typically within the last 300 days of a two-year timeframe.

## DATA PRE-PROCESSING STEP:
- Transformed long-format data to wide format for holistic analysis.
- Addressed:
  - Skewness using square root & logarithmic transformations.
  - Imbalance using SMOTE.
  - Disparate feature scales via standardization.

## MODEL IMPLEMENTATION STEP:
1. **Logistic Regression**:
   - Chosen for its simplicity and interpretability.
   - Strong performance with precision on test data (0.90) and ROC-AUC for both datasets (training: 0.887, test: 0.889).
   
2. **Decision Tree**:
   - Potential overfitting observed in initial implementation.
   - Improved performance after hyperparameter tuning, especially in test ROC-AUC (0.894) and accuracy (0.876).
   
3. **Random Forest**:
   - Faced overfitting like Decision Tree.
   - Tuned model showed consistent performance, notable metrics: test ROC-AUC (0.895) and accuracy (0.888).

4. **XGBoost**:
    - TBU

## HYPERPARAMETER TUNING:
- Utilized `GridSearchCV` for optimizing hyperparameters, ensuring peak performance across models.
- Used RepeatedStratifiedKFold on lin regression for imbalanced data

## MODEL EVALUATION METRICS I USED:
- **Precision**: Measures the model's accuracy in predicting positive instances. It assesses how often predictions of stroke are correct.
- **Recall (Sensitivity)**: Highlights the model's ability to detect positive cases. Checks how often strokes are detected when they actually occur.
- **Accuracy**: Overall indication of model's performance – determines how often predictions (stroke or no stroke) are correct.
- **ROC-AUC**: Evaluates the model's distinguishing capability between classes at varying thresholds. A score of 0.5 = random guessing. 1.0 = perfect classification.
- **F1 Macro**: A balanced measure, being the harmonic mean of precision and recall. 

---

_For detailed insights, visualizations, and methodologies, please feel free to reach out to me to obtain the my full report._
