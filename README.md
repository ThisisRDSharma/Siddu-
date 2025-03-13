Bridger XG uses rule-based logic and advanced matching algorithms to screen and match input details such as names, date of birth, countries, ID numbers, addresses, citizenship, SSN, and phone numbers.

These details are compared against the lists available in XG 5, which include:

Global sanctions and enforcement lists to detect restricted entities.
Extensive PEP (Politically Exposed Persons) coverage to assess risks tied to high-profile individuals.
Profiled adverse media to flag entities linked to financial crimes or fraud.
SWIFT/BIC information for due diligence on financial institutions.
The rules are developed by the bank to automatically process list matches in a way that aligns with the bank’s list screening program and risk profile. These rules leverage input, list, and match attributes from LexisNexis Bridger Insight XG searches to test for evidence of false positives. The Intelligent Match Decisioning System (IMDS) analyzes the results and determines a False Positive Confidence Score.

These details are compared with WorldCompliance™ Data—a global repository maintained by LexisNexis Risk Solutions that contains various watchlists used for sanctions screening and risk assessment. The lists available in XG 5 include:


IBM Safer Payments is a real-time, rules-based fraud transaction monitoring system that leverages customer banking transaction data as its core development data for rule preparation. The FIS Analytics team performs trend analysis on previously confirmed fraud transactions received from clients. They isolate data on completed fraud and genuine transactions by running specific queries on historical transaction data.

Once a rule is written and staged—using queries on the existing fraud data—the team can simulate how many completed fraud or genuine transactions the rule would have fired on if it had been active at the time. This approach ensures that only effective and accurate rules are deployed for real-time monitoring. Essentially, the development phase here is about using detailed customer transaction information to pre-test and refine rules, rather than traditional software development.

The data source used for data preparation is the historical customer banking transaction data. This includes the transaction records provided by clients that detail both previously confirmed fraud cases and genuine transactions.


First of all, this is not a model—it's a rule-based engine. The rules are developed using historical customer banking transaction data. The rule syntax includes a combination of attributes designed to identify high-risk transactions and suspicious activity. These attributes include payment amounts, payee name, brand ID, transaction type, transaction time, frequency/velocity, account creation date, email fraud scores, and other consumer details. Since the customer banking transaction data incorporates these key attributes, it is highly relevant and appropriate for developing and testing the rules that drive the fraud monitoring system


The data used for creating rules is historical customer banking transaction data provided by the client. This data includes both confirmed fraud and genuine transactions. The FIS Analytics team runs queries on this data to perform trend analysis and isolate patterns in completed fraud cases versus genuine transactions. They then use this historical data to simulate how a new rule would have performed in the past. If a rule triggers too many false positives on this data, additional conditions are added to refine it.


The development data is a collection of past banking transactions that includes both fraud and non-fraud examples. This data is prepared through these simple steps:

Collect transaction records from the bank's systems
Separate the transactions into two groups:

Transactions that customers reported as fraud
Transactions that are genuine (not fraud)


Organize this data so it can be easily analyzed

This development data is then used to create fraud detection rules. When making a rule, analysts look at the fraud transactions to spot patterns. They test each rule against the development data to see if it catches the known fraud without flagging too many genuine transactions as suspicious. If a rule creates too many false alarms, they add more specific conditions to make it more accurate.

Run specific queries on this transaction data to isolate patterns
Conduct trend analysis on the confirmed fraud transactions to identify common characteristics
Organize this data so it can be easily analyzed

This development data is then used to create fraud detection rules. When making a rule, analysts run queries on the confirmed fraud transactions to spot trends and patterns. They test each rule against the development data to see if it catches the known fraud without flagging too many genuine transactions as suspicious. If a rule creates too many false alarms, they add more specific conditions to make it more accurate.




For data sampling, a random sampling method was applied to evaluate the performance of the production rules. Out of a total of 1883 rules in production, a random sample of 29 rules was selected for testing. During the sampled period, the actual total alert count was 23,270, while the sample accounted for 1,464 alerts, representing approximately 6% of the total.


Explanatory variables for fraud transaction monitoring are the attributes used to identify high-risk transactions and suspicious patterns. In our system, these variables include:

Payment Amounts: Unusually high or inconsistent amounts can indicate risk.
Payee Name: Helps verify whether the recipient is associated with known high-risk entities.
Brand ID: Links transactions to specific merchants or service providers with historical fraud indicators.
Transaction Time: Abnormal timing (e.g., off-hours) may signal suspicious behavior.
Frequency/Velocity: The rate or clustering of transactions can reveal rapid, repetitive activity.
Account Creation Date: Recently created accounts may be more likely used for fraud.
Email Fraud Scores: Risk scores assigned to email addresses based on past fraudulent activity.
Consumer Age: Can help flag anomalies when customer age deviates from typical patterns.



Explanatory variables in a rule-based fraud transaction monitoring system are the individual transaction or customer attributes that are used as criteria in rules to flag suspicious behavior. Here’s how the given attributes serve as explanatory variables:

Payment Amounts: Unusually high or inconsistent amounts can signal risk. Rules may flag transactions that exceed a typical threshold, indicating potential money laundering or fraud.
Payee Name: Comparing the payee name against known high-risk or blacklisted entities helps detect potential fraudulent transfers.
Brand ID: Transactions associated with a specific merchant or brand that has a history of high fraud rates can be flagged for further review.
Transaction Time: Out-of-hours transactions or unexpected timing patterns may indicate suspicious activity.
Frequency/Velocity: A sudden increase in the number of transactions or rapid successive transactions (velocity) may be a red flag.
Account Creation Date: New accounts might be used to perpetrate fraud, so rules can be set to scrutinize transactions from recently created accounts.
Email Fraud Scores: Email addresses with higher risk scores—perhaps due to previous involvement in fraudulent activities—can serve as indicators of potential fraud.
Consumer Age: Age can correlate with risk; for example, transactions from very young or unusually old consumers may trigger additional checks if they deviate from the norm.




Assumption:
FIS has a feedback loop where tagged fraud cases are reviewed and analyzed to improve fraud detection rules. Once a transaction is identified as fraudulent, it is labeled in the system, and these cases are systematically assessed to detect fraud patterns and weaknesses in existing rules. Based on this analysis, fraud detection rules are refined or new ones are created, ensuring continuous improvement in fraud prevention measures.

Rationale:
This assumption is important because a lack of a feedback loop would mean that fraud detection rules remain static, making them ineffective against evolving fraud techniques. By continuously updating rules based on real fraud cases, the system can adapt to new fraud patterns, reduce false positives and negatives, and enhance overall fraud prevention. This process also improves operational efficiency by minimizing manual intervention and ensuring proactive fraud mitigation.

The customer banking transaction data, received from the client, contains both fraud and genuine transactions. Through the data filtering process, completed fraud and genuine transactions are isolated by running queries on the transaction data. Once filtered, rules are created by querying previously reported fraud cases, ensuring that rule development is based solely on historical fraud patterns rather than the entire dataset.


Data quality treatments have not been performed because built-in controls ensure a low-risk environment for data issues. Within the Zelle UI, predefined data field requirements prevent incorrect or incomplete transactions from being processed. Transactions that do not meet these criteria fail before reaching the Safer Payments environment.

Additionally, fully automated data flows ensure data moves through the system without manual intervention. Programmed data field parameters define what type of data can be entered in each field. Data type restrictions ensure fields contain only the correct format, such as numbers in an amount field. Dedicated monitoring continuously tracks data for accuracy.



As a product under FIS, IBM Safer Payments follows the three-year data retention policy established by FIS. This policy ensures compliance with regulatory requirements while maintaining historical transaction data for fraud detection and analysis.
