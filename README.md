Binary Dependent Variable

Assumption: Logistic regression assumes the dependent variable is binary (0 or 1). The logistic function transforms log-odds into a probability bounded between 0 and 1, which requires a binary dependent variable.
Testing: During development, frequency distributions were analyzed to ensure the dependent variable was binary.
Monitoring: Ongoing frequency distributions are reviewed to verify that the dependent variable remains binary in production.
Probability of Event

Assumption: Logistic regression estimates the probability of the dependent variable being equal to 1, as defined by the performance metric. The dependent variable must consistently represent the event (value of 1) within the targeted population.
Testing: Frequency distributions were used during development to confirm that the dependent variable equaled 1 for the defined performance metric.
Monitoring: Ongoing reviews ensure that the dependent variable remains 1 for the targeted population, with checks against the defined performance metric.
Model Fit

Assumption: The model must not overfit the development dataset to maintain stability and generalizability to new data. Overfitting would result in poor performance metrics on new datasets.
Testing: Data samples were split into development (60%) and validation (40%) sets to ensure nearly identical performance metrics across both datasets.
Monitoring: Independent validation samples from different time periods are analyzed to ensure consistent performance over time.
Error Term

Assumption: Independent variables must not be derived from the dependent variable or future activities. This ensures that the model performs as expected in production without introducing bias or circular logic.
Testing: Dates of dependent variable occurrences were compared with inquiry dates to confirm that events occurred after the inquiry.
Monitoring: Ongoing comparisons of dependent variable occurrence dates and inquiry dates are conducted on additional testing and validation datasets.
Linearity

Assumption: Logistic regression assumes a linear relationship between independent variables and the log-odds (logit) of the dependent variable. Regression coefficients for independent variables have a linear impact on the logit of the dependent variable.
Testing: During development, log-odds plots were created to confirm linear relationships between independent variables and the logit of the dependent variable.
Monitoring: Continuous comparison of relationships between independent variables and the logit of the dependent variable is performed on additional testing and validation datasets.
