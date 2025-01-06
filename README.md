Indeterminate cases were removed from the development sample to ensure the quality and consistency of the dataset, enabling accurate and unbiased model development.
To create the model development and testing datasets, a robust statistical sampling approach was employed. The total development sample was split into two parts: an estimation sample and a validation sample. This approach ensures that the model is not overfitted and is capable of performing well on an entirely separate set of accounts.

The estimation sample was used to fit the model, while the validation sample served to test the model's performance and confirm its robustness. Specifically:

Development Sample: Comprised 60% of the scorecard inquiries and was used to build the model.
Validation Sample: Comprised the remaining 40% of the scorecard inquiries and was used to validate the model's performance.
To ensure reliability, the robustness of the final model was tested using several different hold-out samples. Once confirmed, the final model was applied to the entire scorecard population.

The development sample typically consisted of hundreds of thousands of observations, including tens of thousands of "bad" accounts, to ensure it was fully representative of the intended model population. A large sample size is crucial not only to ensure representativeness but also to allow the model to identify and separate patterns between the two values of the dependent variable (e.g., "good" vs. "bad" accounts).

All variables were binned for analysis, and no other transformations were performed.
|
