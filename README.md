# Heart Disease Prediction 

I tested multiple approaches (stacking, voting, deep learning, with/without SMOTE-ENN), and finally selected a leakage-safe CatBoost pipeline as the best practical model.

## Final Best Result
- **Model:** CatBoost (GPU), no SMOTE-ENN
- **Test Accuracy:** **0.7350**
- **Test ROC-AUC:** **0.7986**
- **Test LogLoss:** **0.5433**

## What I Tried
- XGBoost + RandomForest + Logistic stacking
- Voting ensemble
- IG-based feature selection + triple stack (XGB + RF + ANN)
- Calibrated ensemble variants
- Standalone deep neural network
- Leakage-safe train/validation/test workflow with CV tuning

## Why This Final Model
- Most stable result across repeated runs
- Better generalization than many trial-and-error variants
- Reproducible with saved model + metadata

## Project Files
- `code.ipynb` → all experiments and final report
- (Optional local artifacts not pushed): model files, plots, catboost logs, dataset

## How to Run
1. Open `code.ipynb`
2. Run cells in order
3. Check the final experiment and report cells for best metrics

## Notes
- This dataset tends to plateau around ~73.5%–74% test accuracy with robust tabular methods.
- The focus of this project is not only raw accuracy, but also clean validation and reproducibility.
