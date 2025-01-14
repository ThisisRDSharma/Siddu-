1. Introduction

The Qualifile V4 model evaluates consumers applying for new demand deposit accounts. Its primary objective is to predict which new accounts may be closed within one year. The model incorporates logistic regression to assess the risk associated with prior closure history, high levels of demand deposit account (DDA) and payday lending inquiry activity, and negative check-writing activity. Consumers with such historical behaviors are typically riskier than others.

2. Feature Selection and Business Relevance

Feature Selection:

Variables are selected using a combination of stepwise logistic regression and business domain knowledge.

Feature transformations include binning to improve interpretability and performance.

Multicollinearity Testing:

A Pearson correlation matrix is created during model development.

Any two variables with a correlation greater than 0.5 are examined, leading to variable removal or the creation of hybrid variables.

Business Relevance:

Features directly address risk factors such as prior closures, high inquiry activity, and negative financial behaviors.

3. Odds Ratio Interpretation

Key Transformation:

The model applies a "points to double the odds" transformation, common in credit risk scoring, for easier interpretation of outputs.

A center score of 500 indicates a goods-to-bads ratio of 1:1.

Odds double for every increment in score points:

Minimum Score (100): Goods-to-bads ratio of 1:256; bad rate ≥99.6%.

Maximum Score (899): Goods-to-bads ratio of 256:1; bad rate <0.4%.

Interpretation Example:

A higher score corresponds to a significantly lower probability of account closure, with scores translating into easily understandable metrics for risk assessment.

4. Sensitivity Analysis

Population Stability Testing:

Monthly population stability reports monitor the model's performance.

Objective: Assess how changes in consumer behavior and economic factors affect the model’s predictive performance.

Insight: Stability reports ensure the model adapts to shifts in external conditions while maintaining predictive power.

5. Fairness and Bias Testing

Compliance Measures:

To adhere to Regulation B, the Fair Housing Act, and applicable state laws, the model avoids using attributes or proxies for:

Race

Color

Ethnicity

Although no explicit fairness testing is documented, compliance with regulatory requirements ensures the model does not discriminate against protected groups.

6. Model Fit and Predictive Power

Performance Metrics:

AUC Statistics:

Scorecard 1: 0.6364

Scorecard 2: 0.769

Scorecard 3: 0.700

Scorecard 4: 0.702

KS Statistic: 37.51

Cumulative Accuracy Profile (CAP):

At 20% depth, the Qualifile model identifies 125% more closed accounts than a random sample of the population, demonstrating strong rank-ordering capability.

7. Business Logic Validation

Overrides and Adjustments:

Business rules as part of acquisition strategy.

Business decisions to override acquisition strategy rules for account declination.

Post-account opening management practices (e.g., varying conservatism levels).

Changes in marketing strategies altering applicant mix.

Variations in portfolio bad rates between development and application phases.

8. Improvements Over Qualifile V3

Performance Enhancements:

A 12% improvement in performance compared to Version 3.

Combines both positive and negative behavioral attributes to create a more balanced score.

Allows for consumers previously declined due to negative attributes to be approved based on positive data.

New Data Sources:

Incorporates payday loan inquiries and public record data, enhancing risk evaluation capabilities.

