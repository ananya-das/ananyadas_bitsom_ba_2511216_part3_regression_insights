# Model Comparison

## Overview

Three regression models were evaluated to understand the drivers of monthly sales performance.

---

## Model 1: Simple Regression – Marketing Spend

### Variables Used

Dependent Variable:

* Monthly Sales

Independent Variable:

* Marketing Spend

### R-Squared

R² = 0.167

The model explains approximately 16.7% of the variation in monthly sales.

### Significant Variables

* Marketing Spend (p < 0.05)

### Business Usefulness

This model demonstrates that marketing spend has a positive and statistically significant relationship with monthly sales. It can be useful for evaluating marketing effectiveness.

### Limitations

The model only considers one variable and ignores other important factors such as customer traffic, inventory availability, customer satisfaction, region, and store type.

---

## Model 2: Simple Regression – Footfall

### Variables Used

Dependent Variable:

* Monthly Sales

Independent Variable:

* Footfall

### R-Squared

R² = 0.736

### Significant Variables

* Footfall (p < 0.05)

### Business Usefulness

This model measures the impact of customer traffic on sales performance. It provides useful insight into the importance of attracting customers to stores.

### Limitations

The model does not account for marketing, inventory, customer ratings, regional differences, or store format.

---

## Model 3: Multiple Regression

### Variables Used

Dependent Variable:

* Monthly Sales

Independent Variables:

* Marketing Spend
* Footfall
* Inventory Availability Percentage
* Customer Rating
* Region_East
* Region_North
* Region_South
* Store_Mall
* Store_HighStreet
* Store_Airport

### R-Squared

R² = 0.831

The model explains approximately 83.1% of the variation in monthly sales.

### Significant Variables

Statistically Significant:

* Marketing Spend
* Footfall
* Inventory Availability Percentage
* Customer Rating
* Region_East
* Store_Mall
* Store_HighStreet
* Store_Airport

Not Statistically Significant:

* Region_North
* Region_South

### Business Usefulness

This model provides the strongest explanation of monthly sales performance and captures operational, customer, regional, and store-type effects. It is highly useful for business decision-making because it identifies the key drivers of sales and quantifies their impact.

### Limitations

The model does not include external influences such as economic conditions, competitor promotions, seasonality effects, local demographics, or weather-related factors. Therefore, some variation in sales remains unexplained.

---

## Overall Comparison

The multiple regression model is the preferred model because it explains substantially more variation in monthly sales (83.1%) than either simple regression model. The results indicate that footfall, inventory availability, marketing spend, customer ratings, and store format are important drivers of sales performance. Therefore, business decisions should be based primarily on the multiple regression model.
