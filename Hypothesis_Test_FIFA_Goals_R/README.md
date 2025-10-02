# Hypothesis Test (R): Goals in Men's vs Women's FIFA World Cup Matches

## Objective
Determine whether there is a statistically significant difference in the **mean number of goals** scored in men's vs women's FIFA World Cup matches since **2002-01-01**.  
We assume matches are independent and use a **10% significance level**.

## Hypotheses
- **H₀:** mean goals (men) = mean goals (women)  
- **H₁:** mean goals (men) ≠ mean goals (women)  
- Test: Welch’s two-sample t-test (two-sided, α = 0.10)

## Data
- Input files (not included in repo due to size limits):  
  - `men_results.csv`  
  - `women_results.csv`  
- Required columns: `date`, `tournament`, `home_score`, `away_score`.

## Method
1. Filter FIFA World Cup matches with `date >= 2002-01-01`.
2. Compute **total goals per match** as `home_score + away_score`.
3. Run Welch’s two-sample t-test using `t.test()`.
4. Decision rule:  
   - If _p-value_ < 0.10 → **reject** H₀  
   - Else → **fail to reject** H₀.

## Results
Results are stored in a data frame:

```r
result_df <- data.frame(p_val = p_val, result = decision)

