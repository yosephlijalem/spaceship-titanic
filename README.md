\# Spaceship Titanic — Kaggle



Binary classification to predict `Transported` for each passenger.



\## Current Results (Public LB)

\- CatBoost baseline (hold-out, best\_iter≈299): \*\*0.79939\*\*

\- 5-fold CV (n=145): \*\*0.80453\*\*

\- CV + Group features (n=201): \*\*0.80336\*\*

\- CV + Bins (AgeBin, LogTotalSpend, AnySpend) + Groups (n=340): \*\*0.80523\*\*  ← best so far



\## Cross-Validation

\- 5-fold Stratified CV, CatBoost handles categoricals natively.

\- Latest CV mean: ~0.818 (std ~0.007).



\## Approach (so far)

\- Parse `Cabin` → `CabinDeck`, `CabinNum`, `CabinSide`

\- Spending features: `TotalSpend`, `LogTotalSpend`, `AnySpend` from RoomService/FoodCourt/ShoppingMall/Spa/VRDeck

\- Group features from `PassengerId` prefix: `GroupID`, `GroupSize`, `IsAlone`

\- CatBoostClassifier with early stopping; refit on full data using CV-based `n\_estimators`



\## Reproduce

```bash

conda create -n stitanic python=3.11 -y

conda activate stitanic

pip install pandas numpy scikit-learn catboost lightgbm xgboost matplotlib jupyter ipykernel kaggle

jupyter notebook



