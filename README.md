# Hypothesis Testing: Men's and Women's Soccer Matches

![Soccer Pitch](soccer-pitch.jpg)

In this project, I analyzed international soccer match data to investigate whether more goals are scored in women's soccer matches than in men's. This project was completed as part of a DataCamp assignment, following instructions to apply statistical hypothesis testing techniques on real-world sports data.

## Project Scope

The project focuses on analyzing goal-scoring trends specifically in **official FIFA World Cup matches** (excluding qualifiers) that took place since **January 1, 2002**. The analysis is based on two datasets:
- **`women_results.csv`**: Results of every official women's international match since the 19th century.
- **`men_results.csv`**: Results of every official men's international match since the 19th century.

## Hypothesis

The objective was to answer:
> **Are more goals scored in women's international soccer matches than men's?**

### Hypotheses

- **Null Hypothesis (H₀)**: The mean number of goals scored in women's international soccer matches is the same as men's.
- **Alternative Hypothesis (Hₐ)**: The mean number of goals scored in women's international soccer matches is greater than men's.

The analysis is conducted using a **10% significance level**.

## Data Preparation and Analysis Steps

1. **Data Exploration**: Loaded and examined both datasets to understand structure and content.
  
2. **Data Filtering**:
   - Filtered each dataset to include only FIFA World Cup matches held after January 1, 2002.
   - Calculated `total_goals` for each match by summing `home_score` and `away_score`.

3. **Hypothesis Test Selection**:
   - Conducted a **Shapiro-Wilk test** to assess the normality of the `total_goals` distribution for each dataset. The non-normal distribution observed led to using the **Mann-Whitney U test** (a non-parametric test) to compare distributions.
   - Used a one-sided test with the alternative hypothesis that the goal average in women’s matches exceeds that of men's.

4. **Hypothesis Testing**:
   - Performed the Mann-Whitney U test and stored the p-value and test result in a dictionary.

## Results

The test outcome is stored in the following dictionary format:

## python
**result_dict = {"p_val": p_val, "result": result}**


Here:
- **p_val**: P-value from the Mann-Whitney U test.
- **result**: Indicates `"reject"` or `"fail to reject"` the null hypothesis based on the p-value relative to the 10% significance level.

This README summarizes the project setup, methodology, and how the hypothesis test was applied to answer the initial question regarding goal-scoring trends across men’s and women’s international soccer matches. 
