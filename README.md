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
