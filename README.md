Model Formula and Structure (Logistic Regression)
Model Type:

Logistic regression is used to predict whether a customer’s account will be forcibly closed (charged off) within the first 12 months of account opening due to abuse or suspected fraud.
Input Features (Predictors):

Customer attributes include:
Customer name
Date of birth (DOB)
Address
SSN (Social Security Number)
Dependent Variable (Target):

Binary outcome:
1: Account closed due to abuse or suspected fraud within 12 months by the same institution that conducted the inquiry.
0: Account not closed for these reasons within 12 months.
Feature Engineering and Transformations:

Continuous attributes (e.g., DOB, address details) are binned into categorical groups.
Binning is done to:
Separate "good" and "bad" accounts based on relative bad rates.
Optimize segmentation of the data to maximize the model's predictive power.
Decision tree software and chi-square tests are used to create bins with meaningful separation.
Variables are selected and adjusted iteratively:
Variables that behave counterintuitively (e.g., coefficients with signs opposite to expected behavior) are removed.
Parameters:

Proprietary information, but each variable is assigned a weight derived from logistic regression.
The goal of the parameter estimation process is to maximize the separation of values between "good" and "bad" accounts.
Model Output:

The model produces a score between 100 and 899, with exceptions for scores greater than 9,000.
Score Interpretation:
A base score of 500 corresponds to a 1:1 good-to-bad ratio (50% bad rate).
For every 50-point increase, the odds of being "good" double.
At:
Score 100: Bad rate ≥ 99.6%.
Score 899: Bad rate < 0.4%.


Validation of Variables:

Each variable's predictive power is assessed.
The model is re-run iteratively with different combinations of variables to improve performance.
Counterintuitive results (e.g., signs of coefficients inconsistent with expected behavior) lead to variable exclusion and re-fitting.
Binning Process:

The minimum and maximum values for each attribute are chosen such that:
Each bin has a higher or lower bad rate relative to other bins.
Bins allow for maximum separation between good and bad accounts.
Scoring Scale and Adjustments:

The model outputs scores on a scale of 100 to 899.
The score of 500 is the benchmark, where good-to-bad odds are 1:1.
The scaling allows for easier interpretation and aligns with industry standards.

Score Range and Base Score:

The model generates scores ranging from 100 to 899, with exceptions for scores above 9,000.
A base score of 500 represents a 1:1 good-to-bad odds ratio (50% bad rate).
Odds Scaling:

The odds double for every 50-point increase in the score.
For example:
At 550, the odds of being "good" are 2:1.
At 600, the odds are 4:1, and so on.
Conversely, the odds halve for every 50-point decrease in the score.
Score Interpretation by Bad Rates:

At a score of 100, the bad rate is ≥ 99.6%.
At a score of 500, the bad rate is 50%.
At a score of 899, the bad rate is < 0.4%.
Purpose of the Score:

The Qualifile score predicts the likelihood of an account being forcibly closed within 12 months due to abuse or suspected fraud.
The score helps rank-order customers by risk, allowing institutions to identify and manage high-risk individuals proactively.
