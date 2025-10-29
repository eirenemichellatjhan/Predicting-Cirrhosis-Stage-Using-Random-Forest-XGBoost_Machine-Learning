# Predicting-Cirrhosis-Stage-Using-Random-Forest-XGBoost_Machine-Learning

This project aimed to predict the clinical stage of liver disease (cirrhosis) from patient records containing biochemical and clinical features (e.g., Albumin, Bilirubin, Prothrombin, SGOT). The goal was to compare ensemble models and identify which biomarkers are most informative for stage prediction.

**Tools**: Python, Scikit-learn, Pandas, NumPy, Matplotlib

**Approach**: Trained and compared Random Forest and XGBoost classifiers. Performed hyperparameter tuning with GridSearchCV (multiple search spaces) and evaluated models on an independent test set using accuracy, precision/recall/F1 per class, and confusion matrices. Feature importance was extracted from the best model (Random Forest).

**Results**: Random Forest achieved ~50% test accuracy, while XGBoost reached ~44%. Both models struggled with underrepresented classes (notably class 0), performing best on classes 2 and 3. After tuning, Random Forest was selected as the best model. We also gained information that the most important features were Albumin (0.19), Prothrombin (0.17), Triglycerides (0.158), Alkaline Phosphatase (0.094), and SGOT (0.092).

**Key Insight**: Albumin and Prothrombin (liver function biomarkers) are the most important features for predicting cirrhosis stage. The model’s accuracy was affected by class imbalance and similar feature patterns between stages. Improving the data balance (usi
