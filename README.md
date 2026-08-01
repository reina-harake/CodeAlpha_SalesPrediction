# Sales Prediction

**CodeAlpha Data Science Internship — Task 4**

A regression model that predicts sales based on advertising spend across TV, Radio, and Newspaper channels, with analysis of how channel combinations affect sales outcomes.

## Dataset

200 records of advertising spend (in thousands) across TV, Radio, and Newspaper channels, with corresponding Sales figures (in thousands of units). No missing values or duplicates.

## Workflow

1. **Data Exploration & Cleaning** — checked for missing values/duplicates (none found), visualized distributions and correlations.
2. **Feature Engineering** — created `Total_Spend` and a `TV_Radio_Interaction` term to test for synergy between channels.
3. **Model Training** — trained Linear Regression and Random Forest, each with and without the interaction term.
4. **Model Evaluation** — compared R², MAE, RMSE across all four model variants.
5. **Business Insights** — translated model findings into actionable marketing recommendations.

## Results

| Model | R² | MAE | RMSE |
|-------|-----|-----|------|
| Linear Regression (baseline) | 0.8994 | 1.4608 | 1.7816 |
| Linear Regression (with interaction) | 0.9742 | 0.6718 | 0.9025 |
| Random Forest (baseline) | 0.9813 | 0.6201 | 0.7686 |
| Random Forest (with interaction) | **0.9917** | **0.3992** | **0.5116** |

**Final model: Random Forest Regressor with TV × Radio interaction term**

## Key Insight

Adding a TV × Radio interaction term improved every model tested, with Linear Regression showing the largest gain (R² 0.899 → 0.974). This confirms a genuine synergy effect between TV and Radio advertising — the two channels are more effective combined than separately. Newspaper spend showed minimal correlation with Sales (0.23) throughout the analysis.

## Business Recommendations

- Prioritize joint TV + Radio campaigns over single-channel spend
- Reduce reliance on Newspaper advertising given its negligible impact on Sales
- TV's effectiveness increases substantially when paired with higher Radio spend

## Tools Used

Python, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, Jupyter Notebook

## Files

- `sales_prediction.ipynb` — full analysis notebook
- `Advertising.csv` — dataset
- `sales_prediction_model.pkl` — saved trained model
EOF
