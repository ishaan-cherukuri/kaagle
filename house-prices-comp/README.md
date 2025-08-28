# Kaggle: Ames Housing Competition 

This repository contains my work for the **Kaggle House Prices – Advanced Regression Techniques** competition.
Out of 4,300+ participants, I placed in the **top 5% (231st place at the time of publishing)**.

## Contents

* `cat_boost.ipynb` → Jupyter notebooks I used for exploration, preprocessing, and modeling.
* `submissions.csv` → Submission `.csv` file generated during the competition.
* `data/` → Data folder with files used for traning and testing as well as `data_description.txt`.
* `env.yml` → Conda env `yml` file  to install dependencies.

## Approach

My solution focused on keeping things simple yet effective:

1. **Data Preparation**

   * Split features into numerical, nominal, and ordinal.
   * Applied different imputations per feature type.
   * Analyzed each feature with the help of `data_description.txt`.
2. **Modeling**

   * Built a strong baseline using **CatBoost**.
   * Conducted RandomizedSearchCV for hyperparameter tuning.
   * Experimented with XGBoost, Random Forest, and stacking (meta-ensembles).
3. **Validation**

   * Relied on **cross-validation (3 folds)** instead of leaderboard chasing.

## Results

* **Best Model:** CatBoost
* **Leaderboard Score (RMSE):** \~0.1196
* Stacking/ensembling did not improve results beyond the CatBoost baseline.

## Further Improvements

While I analyzed every feature and gained a deeper understanding of meta-ensembles, my inexperience and limited computational power restricted their effectiveness. With more resources and refined ensemble strategies, the solution could potentially push beyond my current score.

## Notes

* All code snippets in my related article were simplified for illustration.
* The notebooks here contain more detailed steps and experiments.

## Related Article

I wrote a detailed breakdown of my approach here:
👉 [Read the full write-up on Medium](https://medium.com/@ishaan.cherukuri/introduction-fe44f0cea97c)

