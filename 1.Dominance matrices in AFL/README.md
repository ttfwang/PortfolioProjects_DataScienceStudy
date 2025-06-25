# AFL Dominance Matrix Forecasting – Predicting Team Rankings

## Project Overview

This project explores the use of dominance matrices to predict AFL (Australian Football League) team rankings before the season ends. The primary objective is to evaluate the accuracy of various dominance-based ranking methods and determine how many rounds of match data are needed to make reliable predictions. This project was completed as part of my Master of Data Science studies.

## Objectives

- **Forecast Team Rankings:** Use dominance matrices to estimate AFL team performance based on score ratios instead of simple win/loss records.
- **Evaluate Predictive Accuracy:** Compare different ranking methods and measure accuracy at various points during the season.
- **Enhance Understanding of Ranking Algorithms:** Examine the impact of weighting adjustments and second/third-order dominance measures on predictions.

## Data

The dataset is based on the AFL 2022 season match results and was sourced from [FootyWire](https://www.footywire.com/). The data includes round-by-round match results and point differentials between teams.

## Files in this Repository

- `README.md`: Project documentation.
- `afl_dominance_forecasting_calculation spreadsheet.excel`: implementing dominance matrix ranking and accuracy analysis.
- `afl_2022_match_data.csv`: Raw data file used to build dominance matrices and calculate predictions.
- `dominance_matrix_report.pdf`: Final assessment report submitted for Master of Data Science coursework.

## Methodology

The forecasting methodology relies on constructing dominance matrices and deriving ranking scores:

1. **Dominance Matrix D(m):**
   - Represents the relative score ratios between teams for the first `m` rounds.
   - Each matrix cell indicates how much one team dominated another based on cumulative scores.

2. **Ranking Algorithms:**
   - **R1:** Direct dominance (net score ratio).
   - **R2:** Strength of opponents, based on the square of the dominance matrix.
   - **R3:** Tertiary ranking using cubic transformation.
   - **Weighted Model:** Combines R1 + n₁ × R2 + n₂ × R3 to test prediction accuracy with different weighting schemes.

3. **Evaluation:**
   - Compared predicted rankings with actual final AFL standings.
   - Accuracy tracked across different rounds (m = 3 to 22).

## Key Insights

- **Low early-round accuracy:** Predictions below 20% before Round 10 due to limited data and unstable dominance trends.
- **Improved accuracy later:** Models achieved over 50% accuracy from Round 16 onward.
- **Best model:** R1 + R2 × n₁ performed best (56% accuracy at Round 20).
- **Score margin matters:** Teams with narrow wins were often underrated by dominance-based models.

## Comparison of predicted rankings vs. actual D(3-22) ladder (Screenshot)
![Comparison of predicted rankings vs. actual D(3-22) ladder](https://github.com/ttfwang/PortfolioProjects_DataScienceStudy/blob/main/1.Dominance%20matrices%20in%20AFL/Comparison%20of%20predicted%20rankings%20%26%20actual%20ladder%20(screenshot).PNG)

## Model Comparison (Screenshot)
![Model Comparison](https://github.com/ttfwang/PortfolioProjects_DataScienceStudy/blob/main/1.Dominance%20matrices%20in%20AFL/Model%20Comparison%20(screenshot).PNG)

## Conclusion

This project demonstrates how mathematical modelling using dominance matrices can provide moderately accurate team rankings based on score performance alone. It highlights the importance of data volume, weighting adjustments, and interpretation in predictive analytics.

## Acknowledgment

This project was completed for the Mathematics for Data Science subject at La Trobe University as part of my Master of Data Science program. It reflects my interest in predictive analytics and model validation.

## Contact

Feel free to connect with me on [LinkedIn](https://www.linkedin.com/in/tengfei-wang) or reach out via email at tengfeiwang1989@gmail.com.
