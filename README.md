# Empirical Testing: R&D vs non-R&D Portfolios

## Introduction & Objective

This project examines the performance of firms with and without reported R&D expenditures through the construction and evaluation of value-weighted and equal-weighted portfolios. Using data spanning from 1980 to 2022, the portfolios' alphas and betas relative to the market are found and informed whether this factor can explain the variation in returns that other factors like small-minus-big, or high-minus-low might have missed. By incorporating WRDS datasets such as Compustat fundamentals, CRSP stock market returns, and linking tables, this exploration provides a comprehensive evaluation of whether R&D expenditure influences portfolio performance, and understanding how it shapes returns can lead to many different potential investment strategies for U.S. firms in the future.

## Methodology
### Data Retrieval & Cleaning
The Wharton Research Data Services (WRDS) database is a widely utilized data platform designed to support research in a multitude of disciplines. For this research, data was acquired from two WRDS datasets: Compustat/CRSP linked fundamentals annual data and CRSP (V2) stock monthly returns data. Compustat provided firm-level financial data, including R&D expenditures, while CRSP offered market return and capitalization details. The two data sets were merged on the year and a unique identifier (Year and PERMNO). The market factor data was loaded from the Kenneth R. French Data Library. This included the risk-free rate and excess market return factor for all months and was filtered accordingly for the date range. All datasets were cleaned and filtered according to numerous constraints, i.e.,  including U.S.only firms, and no pharma or financial firms to remove concentrated R&D industries.

## Portfolio Construction
Two types of portfolios were constructed: equal-weighted and value-weighted. Firms were categorized into two groups based on their R&D expenditure (XRD): those with R&D (XRD>0) and those without (XRD=0). Equal-weighted portfolio returns were calculated as the average return of all firms in a group on a given date, while value-weighted portfolio returns were calculated by weighting each firm's return by its market capitalization. This distinction captures two different dimensions of portfolio performance: equal-weighted portfolios emphasize the performance of smaller firms by giving all firms the same weight, while value-weighted portfolios reflect the influence of larger, more established firms that dominate market capitalization.

## Results 
<img width="681" alt="Screen Shot 2025-01-31 at 6 46 38 PM" src="https://github.com/user-attachments/assets/0bd492f0-1298-4b6a-adbc-00d49d74cb33" />

## Key Takeaways:
Alphas: None of the portfolios exhibit statistically significant alphas, suggesting no evidence of consistent outperformance or underperformance relative to the market after adjusting for risk.
Betas: All portfolios have significant betas, indicating strong correlations with market movements. R&D portfolios, particularly equal-weighted ones, show higher sensitivity to the market (beta > 1), suggesting that these portfolios are slightly more volatile compared to the market.
R-squared Values: Value-weighted portfolios consistently have higher R-squared values than equal-weighted ones, highlighting that larger-cap firms’ returns are more strongly tied to market movements.


