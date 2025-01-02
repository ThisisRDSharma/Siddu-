Overview of Model Development Data
The model is designed to support the opening of demand deposit accounts (DDA) for customers with Social Security Numbers (SSNs) through all available deposit account opening channels, including digital onboarding platforms and in-branch processes.

Data Sources and Coverage:
Internal Data: Debit bureau data, sourced from internal systems.
External Data: Public record data from external sources.
Optional Feature: The model has the flexibility to incorporate external credit bureau attributes and credit scores to assess potential customer behavioral risk.
Data Characteristics:
Time Periods: Both the internal and external datasets cover a historical period of 3 to 5 years, consistent with retention policies.
Update Frequency: The datasets are updated daily to ensure the model operates with the most current and accurate information.
Consistency: The data utilized is aligned with organizational data governance and compliance standards.
Scope:
The model development data provides comprehensive coverage of customer attributes relevant to the demand deposit account opening process across all channels. The optional feature of leveraging external credit bureau data further enhances the model's ability to evaluate customer behavioral risk, contributing to more informed decision-making.

The model utilizes a combination of internal and external data sources to ensure comprehensive coverage and accuracy in decision-making.

Internal Data: Debit Bureau Data
The internal data is sourced from various debit bureau files and includes the following:

Chex Systems Open Inquiry File (DDA): Contains inquiries related to demand deposit accounts.
Chex Systems Open Inquiry File (Non-DDA): Includes inquiries for accounts other than demand deposit accounts.
Check Printing Order History Files: Maintains a record of customer check printing orders.
Returned Checks Files: Tracks details of returned checks for transaction history.
External Data: Public Record Data
The external data is obtained from public records and is used to supplement internal data for enhanced model performance.

Data Characteristics:
Time Periods: Both datasets cover a historical period of 3 to 5 years, consistent with data retention policies.
Update Frequency: The datasets are updated daily to ensure real-time relevance and model accuracy.
