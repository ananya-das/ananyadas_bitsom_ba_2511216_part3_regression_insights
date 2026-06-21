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

## Multiple Regression Equation

Monthly Sales = β₀ + β₁(Marketing Spend) + β₂(Footfall) + β₃(Avg Discount %) + β₄(Staff Count) + β₅(Inventory Availability %) + β₆(Competitor Distance) + β₇(Customer Rating) + β₈(Holiday Flag) + β₉(Region_East) + β₁₀(Region_North) + β₁₁(Region_South) + β₁₂(Store_HighStreet) + β₁₃(Store_Airport) + β₁₄(Store_Mall) + ε

Where:

* West is the reference region.
* Residential is the reference store type.
* β₀ is the intercept.
* β₁ to β₁₄ are regression coefficients.
* ε represents the error term.

The dummy variables allow categorical information to be incorporated into the regression model while avoiding redundancy and multicollinearity.
