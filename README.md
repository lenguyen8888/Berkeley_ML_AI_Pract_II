# Jupyter notebook link
[Project Notebook](https://github.com/lenguyen8888/Berkeley_ML_AI_Pract_II/blob/master/prompt_II.ipynb)

# Vehicle Inventory Analysis Report

## Introduction
This report presents the findings from our analysis of various features affecting vehicle pricing. We performed Linear Regression, Ridge Regression, and Lasso Regression to identify key features and their impact on pricing. The main audience for this report includes used car dealers looking to optimize their inventory based on data-driven insights.

## Features Analyzed
We analyzed the following features:
- **Numerical Features:** `odometer`, `car_age`
- **Categorical Features:** `title_status`, `transmission`

## Ridge Regression Findings
The Ridge Regression model provided the following insights:

| Feature                  | Coefficient        | Absolute Coefficient |
|--------------------------|-------------------:|---------------------:|
| title_status_missing     | -156186.221529     | 156186.221529        |
| title_status_clean       | 94976.899144       | 94976.899144         |
| car_age                  | 70521.429273       | 70521.429273         |
| title_status_parts only  | -51331.261367      | 51331.261367         |
| title_status_lien        | 50938.508161       | 50938.508161         |
| title_status_rebuilt     | 42688.374998       | 42688.374998         |
| transmission_manual      | -32103.708217      | 32103.708217         |
| transmission_automatic   | 20655.083360       | 20655.083360         |
| title_status_salvage     | 18913.700593       | 18913.700593         |
| transmission_other       | 11448.624865       | 11448.624865         |
| odometer                 | -1334.705733       | 1334.705733          |

### Interpretation
- Vehicles with a `missing` title status significantly reduce the price.
- A `clean` title status positively impacts the price.
- `Car age` also has a positive effect on the price.
- `Manual transmission` has a negative effect on the price compared to `automatic transmission`.

## Lasso Regression Findings
The Lasso Regression model provided the following insights:

| Feature                  | Coefficient        | Absolute Coefficient |
|--------------------------|-------------------:|---------------------:|
| title_status_missing     | -158145.345059     | 158145.345059        |
| car_age                  | 70041.587345       | 70041.587345         |
| title_status_clean       | 56687.191414       | 56687.191414         |
| transmission_manual      | -41458.516723      | 41458.516723         |
| transmission_automatic   | 9346.046231        | 9346.046231          |
| title_status_salvage     | -7948.103417       | 7948.103417          |
| odometer                 | -1270.613516       | 1270.613516          |

### Interpretation
- Similar to Ridge Regression, a `missing` title status significantly reduces the price.
- `Car age` positively impacts the price, though with slightly different magnitude compared to Ridge.
- Lasso Regression emphasizes fewer features but shows similar patterns in `transmission` effects.

## Conclusion
Both Ridge and Lasso Regression models highlight the significant impact of `title status`, `car age`, and `transmission` type on vehicle pricing. Dealers can use these insights to fine-tune their inventory strategies, focusing on vehicles with clean titles, newer age, and automatic transmissions to maximize their profit potential.
