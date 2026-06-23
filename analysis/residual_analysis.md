# Residual Analysis

## Objective

The purpose of residual analysis is to evaluate how well the final multiple regression model predicts monthly sales and identify stores where actual performance differs substantially from model predictions.

The final regression model included:

* Marketing Spend
* Footfall
* Inventory Availability Percentage
* Customer Rating
* Region Dummy Variables
* Store Type Dummy Variables

Residuals were calculated using:

**Residual = Actual Monthly Sales − Predicted Monthly Sales**

Interpretation:

* Positive Residual → Model under-predicted sales.
* Negative Residual → Model over-predicted sales.

---

## Top 5 Positive Residuals (Under-Predicted Stores)

| Store ID | Actual Sales | Predicted Sales |   Residual |
| -------- | -----------: | --------------: | ---------: |
| STR-1028 |   713,611.16 |      597,763.09 | 115,848.07 |
| STR-1073 |   813,316.71 |      702,155.90 | 111,160.81 |
| STR-1019 |   788,087.68 |      697,722.39 |  90,365.29 |
| STR-1026 |   625,514.04 |      538,276.80 |  87,237.24 |
| STR-1050 |   735,786.64 |      648,629.27 |  87,157.37 |

### Business Interpretation

These stores achieved sales significantly higher than predicted by the model. This suggests that additional factors not included in the dataset may be contributing to their strong performance.

Possible explanations include:

* Strong local customer demand
* Effective store management
* Successful local marketing initiatives
* Superior customer service
* Favorable store location characteristics

### Observed Patterns

Among the stores with the largest positive residuals:

* Three stores belong to the East region.
* Two stores are Mall stores.
* One store belongs to the North region.

This indicates that certain East-region and Mall stores may be outperforming expectations due to factors not captured by the regression model.

---

## Top 5 Negative Residuals (Over-Predicted Stores)

| Store ID | Actual Sales | Predicted Sales |    Residual |
| -------- | -----------: | --------------: | ----------: |
| STR-1017 |   685,379.08 |      844,625.82 | -159,246.74 |
| STR-1023 |   627,171.90 |      769,804.18 | -142,632.28 |
| STR-1012 |   595,467.60 |      713,070.15 | -117,602.55 |
| STR-1007 |   800,451.94 |      914,982.03 | -114,530.09 |
| STR-1009 |   641,865.03 |      743,022.90 | -101,157.87 |

### Business Interpretation

These stores generated substantially lower sales than predicted by the model. This suggests that certain negative influences affecting performance were not captured by the available variables.

Possible explanations include:

* Strong local competition
* Operational inefficiencies
* Lower customer conversion rates
* Store-specific service issues
* Temporary economic or market challenges

### Observed Patterns

Among the stores with the largest negative residuals:

* Four stores belong to the West region.
* Two stores are Mall stores.
* One store is a High Street store.
* One store belongs to the North region.
* One store belongs to the South region.

This suggests that some West-region stores may be underperforming relative to expectations despite favorable characteristics captured by the model.

---

## Under-Prediction and Over-Prediction Analysis

The model does not appear to exhibit a strong systematic bias toward any single store format. Mall stores appear in both the positive and negative residual groups, indicating that store format alone does not explain the largest prediction errors.

However, regional patterns are visible:

* Several East-region stores appear among the largest positive residuals, suggesting that some East-region locations outperform model expectations.
* Several West-region stores appear among the largest negative residuals, suggesting that the model may overestimate performance for certain West-region locations.

These findings indicate that store-level factors beyond the variables included in the regression model continue to influence sales performance.

---

## Conclusion

The final multiple regression model achieved strong predictive performance, explaining approximately 83.1% of the variation in monthly sales (R² = 0.831). Nevertheless, residual analysis reveals that some stores continue to perform substantially above or below model expectations.

Large positive residuals indicate hidden success factors that are not currently measured, while large negative residuals suggest challenges or risks that are also not captured in the dataset.

To further improve prediction accuracy, future models could incorporate additional variables such as:

* Local demographics
* Competitor activity
* Seasonal demand patterns
* Promotional campaigns
* Store management quality
* Economic conditions

Overall, the residual analysis confirms that the model is highly useful for understanding sales drivers while also highlighting opportunities for future model enhancement.
