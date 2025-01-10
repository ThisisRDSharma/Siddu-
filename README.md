1. Initial Review and Reduction
The initial set of variables underwent a thorough review to eliminate redundant, irrelevant, or weak predictors.
Variables that did not add meaningful value to predicting the dependent variable (e.g., charge-off risk) were excluded at this stage.
2. Stepwise Logistic Regression
A stepwise logistic regression procedure was employed to further refine the list of variables. This process:
Iteratively evaluates independent variables to assess and rank their statistical significance in predicting the dependent variable.
Utilizes the Maximum Likelihood Estimation (MLE) function to determine the hierarchy of variables based on their predictive power.
Retains variables that demonstrate a strong statistical relationship with the dependent variable.
3. Generation of Candidate Models
The top-ranking variables identified through stepwise logistic regression were used to generate multiple candidate models for evaluation.
During this phase:
Each variable was assigned weights using logistic regression to optimize its contribution to the model.
Numerous combinations of variables were tested for each segment to identify the best-performing sets of predictors.
4. Handling Counterintuitive Results
If a variable produced counterintuitive results (e.g., a direction of influence contrary to domain expertise or business logic), the variable was removed.
The process was restarted with a different combination of variables to ensure logical consistency and predictive accuracy.
5. Final Model Selection
The stepwise procedure was repeated as necessary until a set of candidate models was developed for each segment.
The best-performing combination of variables—those that provided the highest predictive accuracy and alignment with business objectives—was selected for inclusion in the final model.
