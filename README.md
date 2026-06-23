# ananyadas_bitsom_ba_2511216_part3_regression_insights

# 1. Business Problem Summary

The retail chain's leadership team wants to understand which factors most strongly influence monthly store sales. They are considering actions such as increasing marketing spend, improving inventory availability, adjusting discount strategies, reallocating staff, and prioritizing specific store types or regions. This analysis uses regression techniques to identify the key drivers of sales and provide data-driven recommendations that can help improve overall business performance.

# 2. Dataset Description

The dataset contains monthly operational and performance metrics for retail stores across different regions and store types. The objective is to analyze the factors influencing monthly sales using regression analysis. Key variables include marketing spend, footfall, discounts, staff count, inventory availability, customer ratings, region, and store type.

## Data Cleaning and Preparation

To preserve data integrity, all cleaning activities were performed in a separate worksheet while retaining the original dataset unchanged.

### Missing Value Treatment

#### competitor_distance_km

* 6 missing values were identified.
* Missing values were replaced using **median imputation**.
* Median was chosen because distance-related variables may contain skewed values and the median is less sensitive to outliers.

#### customer_rating

* 8 missing values were identified.
* Missing values were replaced using **mean imputation**.
* The average customer rating was calculated and used to fill missing records.

### Duplicate Records

* Dataset was checked for duplicate observations.
* No duplicate records were identified.

### Data Validation

* Numerical variables were reviewed for invalid values.
* No negative sales, negative marketing spend, or other obvious data quality issues were detected.

# 3. Retail Sales Regression Analysis: Dependent and Independent Variable

## Dependent Variable
- Monthly Sales

## Independent Variables
- Marketing Spend
- Inventory Availability
- Discount Percentage
- Staff Count
- Customer Rating
- Footfall
- Competitor Distance
- Region
- Store Type

## Numerical Variables
- Marketing Spend
- Inventory Availability
- Discount Percentage
- Staff Count
- Customer Rating
- Footfall
- Competitor Distance
- Monthly Sales

## Categorical Variables
- Region
- Store Type

## Data Cleaning
- Checked for missing values
- Checked for duplicates
- Checked for invalid values

## Variables Excluded
- Store ID (identifier only)
- Transaction ID
- Serial Number

# 4. Regression Approach

The analysis followed a structured regression workflow to identify factors associated with monthly sales performance.

### Step 1: Data Preparation
- Reviewed and cleaned the dataset.
- Preserved the original data in a separate worksheet.
- Standardized categorical values and verified numerical fields.

### Step 2: Simple Regression Analysis
Two simple regression models were developed using monthly sales as the dependent variable:
1. Marketing Spend → Monthly Sales
2. Footfall → Monthly Sales

These models were used to evaluate the individual relationship between each predictor and sales.

### Step 3: Multiple Regression Analysis
A multiple regression model was developed using:
- Marketing Spend
- Footfall
- Inventory Availability Percentage
- Customer Rating
- Region Dummy Variables
- Store Type Dummy Variables

This model was used to evaluate the combined effect of multiple business factors on monthly sales.

---

# 5. Dummy Variable Approach

The dataset contained categorical variables that could not be directly included in a regression model.

### Region

Reference Category:
- West

Dummy Variables Created:
- Region_East
- Region_North
- Region_South

### Store Type

Reference Category:
- Residential

Dummy Variables Created:
- Store_Mall
- Store_HighStreet
- Store_Airport

Reference categories were excluded from the model to avoid multicollinearity and the dummy variable trap.

---

# 6. Model Comparison Summary

Three regression models were evaluated.

| Model | Independent Variables | R² | Key Finding |
|---------|---------|---------|---------|
| Simple Regression 1 | Marketing Spend | 0.167 | Marketing spend positively impacts sales |
| Simple Regression 2 | Footfall | (Insert Footfall R²) | Customer traffic strongly influences sales |
| Multiple Regression | Marketing Spend, Footfall, Inventory Availability, Customer Rating, Region Dummies, Store Type Dummies | 0.831 | Provides the strongest explanation of sales performance |

The multiple regression model substantially outperformed the simple regression models and was selected as the final model.

---

# 7. Final Model Selected

### Selected Model
Multiple Regression Model

### Variables Included

Numerical Variables:
- Marketing Spend
- Footfall
- Inventory Availability Percentage
- Customer Rating

Dummy Variables:
- Region_East
- Region_North
- Region_South
- Store_Mall
- Store_HighStreet
- Store_Airport

### Performance

- R² = 0.831
- Adjusted R² = 0.826

The model explains approximately 83.1% of the variation in monthly sales and provides strong predictive performance.

---

# 8. Business Recommendation

The analysis identified several factors that are strongly associated with monthly sales performance.

Leadership should prioritize:

- Increasing customer footfall through targeted marketing and customer engagement initiatives.
- Maintaining high inventory availability to reduce lost sales opportunities.
- Continuing strategic marketing investments that support store traffic and sales growth.
- Improving customer experience and customer satisfaction.
- Prioritizing Airport, Mall, and High Street store formats when evaluating future investments and expansion opportunities.

The findings suggest that operational execution, customer traffic, and store format play important roles in driving sales performance.

---

# 9. Assumptions and Limitations

### Assumptions

- Relationships between variables and sales are approximately linear.
- Observations are independent.
- Variables included in the model are measured accurately.
- Historical patterns are representative of current business conditions.

### Limitations

- Regression identifies association rather than causation.
- The dataset does not include competitor activity, seasonality, demographics, weather, or economic conditions.
- Some store-level operational factors may not be captured.
- Residual analysis indicates that additional unobserved factors influence sales performance.
- Results are based on historical data and may not fully predict future outcomes.

---

# 10. Screenshots Included

The following screenshots have been included as evidence of analysis:

- screenshots/simple_regression_output.png
- screenshots/multiple_regression_output.png
- screenshots/model_comparison_preview.png
- screenshots/residuals_preview.png

These screenshots provide supporting evidence for the regression models, model comparison, and residual analysis performed during the project.
