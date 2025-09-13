# 🚀 Spaceship Titanic (Kaggle)

Predict which passengers were **Transported** after a spacetime anomaly.  
This repo contains a clean, reproducible workflow (CV → features → models → ensembling) and ready-to-submit files.



**Public Leaderboard (rolling):** **0.80944** — top ~3% (≈ #48 / 1544)  
**Best run:** Seed-averaged CatBoost + LightGBM, blended (α=0.60)

---

📈 Results (Public LB)

Approach	Score
CatBoost baseline (hold-out, best_iter≈299)	0.79939
5-fold CV (n≈145)	0.80453
CV + Group features	0.80336
CV + Age bins + LogTotalSpend + AnySpend + Groups	0.80523
Blend: CatBoost + LightGBM (50/50)	0.80734
Seed-averaged (3 seeds) 50/50 blend	0.80921
Seed-averaged blend (α=0.60)	0.80944


🙌 Acknowledgments

Competition: Kaggle – Spaceship Titanic

Photos: Joel Filipe, Richard Gatley, ActionVance (Unsplash)
