# E-commerce customers: app or website?

A short supervised-learning exercise from my Big Data & AI master's. A fictional online retailer wants to know where to invest next: its mobile app or its website. The dataset has 500 customers with their average session length, time on the app, time on the website, years as a member, and yearly amount spent.

The notebook is in French.

## What I did

1. Explored the data (distributions, pair plots, correlation matrix).
2. Fitted a linear regression with `statsmodels` to read the coefficients, then with `scikit-learn` on a 70/30 train/test split.
3. Checked the residuals and the test metrics.

## Results

| Variable | Effect on yearly spend (per extra unit) |
|---|---|
| Years as a member | +61 $ |
| Time on the app (min) | +39 $ |
| Session length (min) | +26 $ |
| Time on the website (min) | +0.19 $ |

Test set: MAE 7.2 $, RMSE 8.9 $, R² 0.99. The data is synthetic, which is why the fit is that clean.

**Takeaway:** time on the website brings almost nothing, time on the app does. Loyalty (years as a member) matters even more than either channel.

## Run it

```bash
pip install pandas numpy matplotlib seaborn statsmodels scikit-learn jupyter
jupyter notebook "Clients E-commerce/Yassine_Megherbi_Clients_E_Commerce.ipynb"
```

The CSV sits next to the notebook; update the path in the first `read_csv` cell if you are not running on Colab.

## Author

Yassine Megherbi – [LinkedIn](https://www.linkedin.com/in/yassine-megherbi-b7b277263/) · [GitHub](https://github.com/yasinemegherbi21-byte)
