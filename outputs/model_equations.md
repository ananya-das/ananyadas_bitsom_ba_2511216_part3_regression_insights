## Table of Contents

* [Dummy Variable Creation](#dummy-variable-creation)
* [Simple Regression Equations](#simple-regression-equations)
* [Multiple Regression Equation](#multiple-regression-equation)
* [Coefficient Explanations](#coefficient-explanations)
* [Region Dummy Variables](#region-dummy-variables)
* [Store Type Dummy Variables](#store-type-dummy-variables)
  
# Dummy Variable Creation and Model Specification

## Categorical Variables

The dataset contains two categorical variables that were converted into dummy variables for regression analysis:

* Region (East, West, North, South)
* Store Type (Residential, High Street, Airport, Mall)

To avoid the dummy variable trap and perfect multicollinearity, one category from each variable was selected as the reference category and omitted from the regression model.

## Region Dummy Variables

West was selected as the reference category.

The following dummy variables were created:

* Region_East
* Region_North
* Region_South

### Excel Formulas

Region_East

```excel
=IF(C2="East",1,0)
```

Region_North

```excel
=IF(C2="North",1,0)
```

Region_South

```excel
=IF(C2="South",1,0)
```

West is represented when all three dummy variables equal 0.

## Store Type Dummy Variables

Residential was selected as the reference category.

The following dummy variables were created:

* Store_HighStreet
* Store_Airport
* Store_Mall

### Excel Formulas

Store_HighStreet

```excel
=IF(D2="High Street",1,0)
```

Store_Airport

```excel
=IF(D2="Airport",1,0)
```

Store_Mall

```excel
=IF(D2="Mall",1,0)
```

Residential is represented when all three dummy variables equal 0.

# Model Equations and Variable Definitions

# Simple Regression Equations

## Model 1: Marketing Spend

### Regression Equation

Monthly Sales = 560,777.35 + 2.13(Marketing Spend)

### Interpretation

* Intercept = 560,777.35
* Marketing Spend Coefficient = 2.13
* R² = 0.1672
* P-value = 2.48 × 10⁻¹⁴

The positive coefficient indicates that higher marketing spending is associated with higher monthly sales. On average, a one-unit increase in marketing spend is associated with an increase of approximately 2.13 units in monthly sales. The very small p-value indicates that the relationship is statistically significant. However, the model explains only 16.72% of sales variation, suggesting that additional factors influence sales performance.

## Model 2: Footfall

### Regression Equation

Monthly Sales = β₀ + β₁(Footfall)

### Interpretation

* Footfall Coefficient = 35.68

The positive coefficient indicates that higher customer traffic is associated with higher monthly sales. A one-unit increase in footfall is associated with an increase of approximately 35.68 units in monthly sales. This aligns with business expectations because stores with more visitors generally generate more revenue.

---

# Multiple Regression Equation

Monthly Sales = β₀ + β₁(Marketing Spend) + β₂(Footfall) + β₃(Inventory Availability %) + β₄(Customer Rating) + β₅(Region_East) + β₆(Region_North) + β₇(Region_South) + β₈(Store_HighStreet) + β₉(Store_Airport) + β₁₀(Store_Mall) + ε

Where:

* β₀ = Intercept
* ε = Error Term

So, the final equation becomes:

Monthly Sales = 58,353.13 + 1.209(Marketing Spend) + 34.015(Footfall) + 3047.929(Inventory Availability %) + 13,439.363(Customer Rating) − 12,401.603(Region_North) + 1,618.413(Region_South) − 18,491.874(Region_East) + 29,382.285(Store_Mall) + 18,098.251(Store_HighStreet) + 42,659.145(Store_Airport)

### Model Performance
R² = 0.8311
Adjusted R² = 0.8257
Significance F = 5.43 × 10⁻¹¹³

Reference Categories:

* Region_West = Reference Region
* Store_Residential = Reference Store Type

### Model Interpretation

The model explains approximately 83.11% of the variation in monthly sales, indicating a very strong fit. The extremely small Significance F value shows that the overall regression model is statistically significant.

Key insights from the model include:

* Higher marketing spend is associated with higher sales.
* Higher footfall is associated with higher sales.
* Better inventory availability is expected to increase sales by reducing stock-outs.
* Higher customer ratings may indicate stronger customer satisfaction and repeat purchases.
* Regional dummy variables measure sales differences relative to West region stores.
* Store-type dummy variables measure sales differences relative to Residential stores.

---
# Coefficient Explanations

## Intercept

Coefficient = 58,353.13

P-value = 0.223

The intercept represents baseline monthly sales when all predictor variables are zero and the store belongs to the reference categories (West region and Residential store type). Since the p-value is greater than 0.05, the intercept is not statistically significant and has limited business interpretation.

## Marketing Spend

Coefficient = 1.209

P-value = 2.44 × 10⁻¹⁹

Marketing spend has a positive and statistically significant relationship with monthly sales. A one-unit increase in marketing spend is associated with an increase of approximately 1.21 units in monthly sales, holding all other variables constant.

## Footfall

Coefficient = 34.015

P-value = 6.25 × 10⁻¹⁰⁵

Footfall is the strongest predictor in the model. Each additional customer visit is associated with an increase of approximately 34.01 units in monthly sales. The extremely low p-value indicates a highly significant relationship.

## Inventory Availability Percentage

Coefficient = 3047.929

P-value = 1.20 × 10⁻¹⁰

Inventory availability has a strong positive and statistically significant impact on sales. Stores with better inventory availability tend to generate substantially higher sales because products remain available when customers want to purchase them.

## Customer Rating

Coefficient = 13,439.363

P-value = 0.0052

Customer rating has a positive and statistically significant relationship with monthly sales. Higher customer satisfaction appears to contribute to stronger store performance.

## Region_North

Coefficient = -12,401.603

P-value = 0.084

North region stores appear to generate lower sales than West region stores. However, the relationship is not statistically significant at the 5% level.

## Region_South

Coefficient = 1,618.413

P-value = 0.823

The South region shows almost no meaningful difference from the West region after controlling for other variables. This variable is not statistically significant.

## Region_East

Coefficient = -18,491.874

P-value = 0.0033

East region stores generate significantly lower sales than West region stores after controlling for all other variables. This relationship is statistically significant.

## Store_Mall

Coefficient = 29,382.285

P-value = 1.26 × 10⁻⁵

Mall stores generate significantly higher monthly sales than Residential stores, holding all other variables constant.

## Store_HighStreet

Coefficient = 18,098.251

P-value = 0.0027

High Street stores generate significantly higher monthly sales than Residential stores.

## Store_Airport

Coefficient = 42,659.145

P-value = 8.34 × 10⁻⁶

Airport stores generate the highest sales premium relative to Residential stores and show a strong statistically significant relationship.

### Statistically Weak Variables

The following variables are not statistically significant at the 5% level:

* Intercept (p = 0.223)
* Region_North (p = 0.084)
* Region_South (p = 0.823)

These variables should be interpreted cautiously because there is insufficient evidence that they meaningfully affect monthly sales after controlling for other factors.

---

