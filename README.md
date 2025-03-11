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
