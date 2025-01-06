Indeterminate cases were removed from the development sample to ensure the quality and consistency of the dataset, enabling accurate and unbiased model development.
To create the model development and testing datasets, a robust statistical sampling approach was employed. The total development sample was split into two parts: an estimation sample and a validation sample. This approach ensures that the model is not overfitted and is capable of performing well on an entirely separate set of accounts.

The estimation sample was used to fit the model, while the validation sample served to test the model's performance and confirm its robustness. Specifically:

Development Sample: Comprised 60% of the scorecard inquiries and was used to build the model.
Validation Sample: Comprised the remaining 40% of the scorecard inquiries and was used to validate the model's performance.
To ensure reliability, the robustness of the final model was tested using several different hold-out samples. Once confirmed, the final model was applied to the entire scorecard population.

The development sample typically consisted of hundreds of thousands of observations, including tens of thousands of "bad" accounts, to ensure it was fully representative of the intended model population. A large sample size is crucial not only to ensure representativeness but also to allow the model to identify and separate patterns between the two values of the dependent variable (e.g., "good" vs. "bad" accounts).

All variables were binned for analysis, and no other transformations were performed.
|
The dependent variable for this model is whether the consumer account was reported as charged off due to abuse or suspected fraud within 12 months of the inquiry, with the reported closure originating from the same institution that conducted the inquiry.

A critical aspect of any model-building process is the proper classification of accounts into good, bad, and indeterminate categories. The performance definitions for this project are as follows:

Bad Account: An account that experienced an involuntary (forced) closure due to abuse or suspected fraud within one year of account opening at the inquiring institution.
Good Account: An account with no forced closure within one year of the inquiry.
Indeterminate Account: Any inquiry that cannot be classified definitively as good or bad.
This classification ensures clear, consistent definitions for the performance variable, which are essential for accurate model development and evaluation.

