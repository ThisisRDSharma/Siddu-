The data extraction process ensures that the input datasets are comprehensive, accurate, and relevant for model development. To achieve this, proprietary consumer search algorithms were utilized to refine the extracted data and enhance its usability for analytical purposes.



Objective:
To ensure the completeness, accuracy, and alignment of the development data with the source systems and production environment, the following reconciliation steps were undertaken for the Qualifile model development process.

Reconciliation Details:

Consistency of Data Sources:

The data sources used for the Qualifile model development are identical to those used in production. This ensures that the development process reflects real-world production conditions, minimizing the risk of discrepancies due to differing sources.
Validation of Data Values:

A comparison of key data calculations was performed between the production environment and the development dataset. Results confirmed that data values in production align with those in development, ensuring accuracy in both environments.
Verification of Data Frequency and Retention:

The frequency of data updates in the production environment was verified to match that of the development dataset. Furthermore, the retention periods in both environments were confirmed to be consistent, ensuring that historical data availability is aligned between development and production.
Population Alignment:

The populations included in both the production and development datasets were verified to be identical. Both datasets consist of incoming inquiry transactions for demand deposit accounts, ensuring that the model is trained and tested on a population representative of actual production conditions.
Raw Data Quality Assessment:

Missing Values:

Records with missing critical fields, such as names and addresses, were excluded from the model development sample. This step was necessary to maintain the accuracy and representativeness of the dataset.
Indeterminate Groups:

Records belonging to indeterminate groups, which could not be clearly classified, were removed from the development sample to avoid introducing noise or ambiguity into the model.
Sample Size Validation:

A minimum sample size of 100,000 randomly selected records was used to validate the overall quality of the input data. This approach ensured that the data utilized for development was representative of the broader population and free from sampling bias.

The quality of the model is highly dependent on the accuracy and completeness of the data provided during the development effort. For instance, if clients provide inaccurate information about forced account closures or demand deposit account closures, the resulting dataset would misrepresent the population and affect model performance.

To mitigate this risk, ongoing data quality monitoring has been implemented to continuously assess the accuracy of incoming data and ensure it remains suitable for use in the model.

