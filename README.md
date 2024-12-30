# Cereal Market Share and Demand Estimation

## Project Overview

This project focuses on demand estimation for cereal brands using market-level data from 1992. The data, aggregated from household-level scanner data, provides insights into the market shares, prices, and characteristics of the top-selling cereal brands across several markets. The goal is to estimate demand and the market share of the outside good, using both Ordinary Least Squares (OLS) and Instrumental Variables (IV).

## Data Description

The dataset contains the following variables:

- **price**: Price paid for the cereal.
- **const**: A column of 1’s.
- **sugar**: Amount of sugar in the cereal.
- **mushy**: How mushy the cereal becomes with milk.
- **share**: Market share of the cereal in each market (between 0 and 1).
- **cdid**: Market identifier.
- **product_id**: Identifier for the cereal product.
- **IV1-IV20**: 20 constructed instrumental variables.

## Methodology

In this project, we estimate demand using the following steps:

1. **Market Share of Outside Good**: Calculated the market share of the outside good in each market.
2. **OLS Regression**: Estimated a share regression using **mushy**, **sugar**, and **price** as explanatory variables.
3. **Instrumental Variables**: Used IVs to instrument for **price** and address potential endogeneity.
4. **First Stage F-test**: Conducted a first stage F-test to check the strength of the instruments.
5. **Second Stage Sargan Test**: Performed a second stage Sargan test to check the independence of instruments from the error term.

## Tools and Libraries Used

- **Programming Language**: R
- **Key Libraries**: `ivreg`, `lm`, `ggplot2`, `dplyr`

## How to Run

1. Clone this repository to your local machine.
2. Open the R Markdown file in RStudio.
3. Run the analysis by knitting the file.

## License

This project is open-source under the [MIT License](LICENSE).
