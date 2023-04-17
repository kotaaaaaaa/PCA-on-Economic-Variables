# Principal Component Analysis on Economic Variables

This project performs a Principal Component Analysis (PCA) on economic variables, using the first principal component as the primary factor. The analysis is carried out on the following five variables:
- INDPRO
- S&P 500
- PAYEMS
- CPIAUCSL
- BUSINVx

## Dependencies

The code depends on the following libraries:
- numpy
- pandas
- seaborn
- matplotlib
- datetime
- statsmodels

## Data

The data used in this analysis is from the following sources:
- `2021-12.csv`: A CSV file containing the original data
- `fred_md_desc.csv`: A CSV file containing the description and transformation codes for the data
- `NBER_DATES.csv`: A CSV file containing the NBER recession dates

## Methodology

1. The data is first imported, cleaned, and transformed according to the transformation codes specified in `fred_md_desc.csv`.
2. Standardization is then applied to the transformed data.
3. PCA is performed, and the first principal component is extracted as the primary factor.
4. Visualizations are created for the primary factor, including a line plot and a histogram.
5. Autoregressive models are fitted for each of the five selected variables, with lagged values and the primary factor as predictors.
6. Model summaries are displayed for each variable.
7. Fitted values for each model are saved to a CSV file.
8. Scatter plots are created to compare the fitted values with the actual values, separated by NBER recession dates.

## Results

The results of the PCA and the fitted models are visualized in the following figures:
- `factor.pdf`: Line plot and histogram of the primary factor (1st principal component)
- `INDPRO.pdf`: Scatter plot comparing fitted and actual values for INDPRO
- `S&P 500.pdf`: Scatter plot comparing fitted and actual values for S&P 500
- `PAYEMS.pdf`: Scatter plot comparing fitted and actual values for PAYEMS
- `CPIAUCSL.pdf`: Scatter plot comparing fitted and actual values for CPIAUCSL
- `BUSINVx.pdf`: Scatter plot comparing fitted and actual values for BUSINVx
