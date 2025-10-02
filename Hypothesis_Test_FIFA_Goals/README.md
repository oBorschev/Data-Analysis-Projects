# Hypothesis Test: Goals in Men's vs Women's FIFA Matches

## Objective
The goal of this project is to determine whether there is a statistically significant difference in the **mean number of goals** scored in men's vs women's FIFA World Cup matches since 2002.

## Hypotheses
- **Null hypothesis (H₀):** The mean number of goals scored in men's matches = the mean number of goals scored in women's matches.
- **Alternative hypothesis (H₁):** The means are not equal.

Significance level: **α = 0.10**

## Method
1. Data sources:
   - `men_results.csv`
   - `women_results.csv`
2. Data filtering:
   - FIFA World Cup matches only
   - From 2002-01-01 onwards
3. Test:
   - Two-sample Welch’s t-test (two-sided) using `scipy.stats.ttest_ind`.
   - Net goals per match calculated as `home_score + away_score`.
4. Decision rule:
   - If p-value < 0.10 → reject H₀
   - Else → fail to reject H₀

## Result
- Results stored in a Python dictionary:
```python
result_dict = {"p_val": p_val, "result": result}

