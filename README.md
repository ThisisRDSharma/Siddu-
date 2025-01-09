Logistic regression models the relationship between a binary dependent variable 
𝑌
Y (e.g., success/failure) and one or more independent variables 
𝑋
1
,
𝑋
2
,
.
.
.
,
𝑋
𝑘
X 
1
​
 ,X 
2
​
 ,...,X 
k
​
 . The model estimates the probability 
𝑃
(
𝑌
=
1
∣
𝑋
)
P(Y=1∣X) using the logistic function:





1. Stability of Future and Past Behavior
The model assumes that historical relationships between predictors (e.g., consumer attributes) and the outcome (charge-off) will remain stable over time.
If consumer behavior, economic factors, or market conditions change significantly, the model may yield inaccurate predictions.
2. Binary Dependent Variable
Logistic regression assumes the dependent variable is binary (e.g., charge-off = 1, no charge-off = 0).
For non-binary outcomes, alternate regression models like multinomial or ordinal logistic regression are required.
3. Probability of Event
The model predicts the probability of an event (e.g., charge-off) occurring based on the logistic function. This probability must lie between 0 and 1.
The logistic function ensures a smooth S-curve relationship between predictors and the probability of the event.
4. Model Fit
The model assumes that the predictors adequately explain the variation in the dependent variable.
Goodness-of-fit tests (e.g., Hosmer-Lemeshow test) and metrics like AUC-ROC are used to validate the fit.
5. Error Term
Logistic regression does not assume normality or homoscedasticity of residuals (unlike linear regression). However, the error terms are assumed to follow a Bernoulli distribution.
Independence of error terms is critical (i.e., no correlation between observations).
6. No Multicollinearity
Predictors should not be perfectly correlated with each other.
Perfect multicollinearity makes it impossible to estimate unique coefficients for the predictors, which can distort the model's reliability.
7. Linearity
Logistic regression assumes a linear relationship between the log-odds (logit) of the dependent variable and the independent variables.
Non-linear relationships can lead to biased results unless transformed or modeled explicitly.
8. Large Sample Size
The method relies on a sufficiently large sample size for stable and reliable parameter estimates.
A rule of thumb: at least 10 events (charge-offs) per predictor variable to avoid overfitting or underpowered models.
Logistic regression uses Maximum Likelihood Estimation (MLE) to estimate the model parameters
