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



If the absolute deviation (increase or decrease) is 10 or less, the metric remains within the acceptable range and is classified as Green (No Action Required)."

2️⃣ Yellow: "If the absolute deviation (increase or decrease) is greater than 10 but not exceeding 20, the metric is classified as Yellow (Caution Zone), indicating a moderate deviation that may require monitoring."

3️⃣ Red: "If the absolute deviation (increase or decrease) is greater than 20, the metric is classified as Red (Critical), requiring immediate investigation and corrective action.





Estimation Methodology for Sanction Screening Model
The XG sanction screening tool utilizes rule-based logic and advanced matching algorithms to screen customers against predefined watchlists. The model works through a structured approach involving entity comparison, match scoring, and false positive identification to ensure efficient and accurate screening.

1. Entity Comparison and Match Detection
XG compares input entities (customer-provided details) with screening list entities (watchlist data).

If the input entity matches a list entity, it is classified as a true match.

If an input entity appears similar to, but is not the same as, a list entity, it is classified as a false positive.

2. Match Confidence Score Calculation
To measure how closely an input entity resembles a list entity, XG assigns a Match Confidence Score ranging from 70 to 100.

The LexisNexis Search Core calculates a match score for each data element (e.g., name, address, date of birth).

For each entity, it identifies:

Best Match Attribute – The attribute with the highest match score.

Best Score Attribute – The highest match score assigned to any data element.

A high match score suggests a strong similarity between the input and list entities.

3. Identifying False Positives Using IMDS
Since sanction screening may produce false positives, the Intelligent Management Decision Support (IMDS) module applies predefined rules to assess whether a match is genuinely suspicious or an error.

IMDS calculates a False Positive Confidence Score ranging from 0 to 10.

This score is compared against a confidence threshold to determine if a match should be automatically classified as a false positive.

4. Intelligent Management Decision (IMD) Processing
When an alert is generated, IMDS provides an Intelligent Management Decision (IMD), which includes:

✅ False Positive Confidence Score – The probability that a match is a false positive.
✅ Reason Codes – Explanations for why a match was classified as a false positive.
✅ Applied Rules – The set of rules used in the evaluation.
✅ Rule File (XML Format) – A document containing all configured rules.

5. Rule-Based Evaluation for False Positives
IMDS determines false positives based on a rule file, which consists of:

Intercept: A baseline value representing the default likelihood of a false positive.

Rules: Each rule contains:

Condition – A test that checks if an attribute meets specific criteria.

Coefficient – A weight that adjusts the false positive confidence score.

Reason Code – An audit trail explanation.

Each condition evaluates as True or False based on whether an entity attribute (such as name, address, or date of birth) meets a predefined threshold.

6. Attributes Used in IMDS
IMDS analyzes multiple attributes to assess potential matches. These attributes are categorized as:

📌 Input Attributes – Describe the entities being screened.
📌 List Attributes – Represent the entities stored in the watchlist database.
📌 Match Attributes – Provide results from the LexisNexis Search Core, which calculates match scores.

Entities can be associated with multiple data elements, such as names, dates of birth, addresses, ID numbers, citizenships, and phone numbers. The LexisNexis Search Core assigns match scores to each data element and selects the best match based on the highest confidence score.



One key setting is the targeted good-to-bad ratio, which is set between 3:1 and 5:1. This ratio is used as a threshold to help minimize false positives by ensuring that for every fraudulent alert (bad), the system verifies that there are at least 3 to 5 legitimate transactions (good) under similar conditions.

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


The modeling approach is a rule-based system that relies solely on manually written rules. These rules are developed by querying and analyzing previously confirmed fraud data to identify patterns indicative of fraudulent activity.


**Business Objectives:**  
- Provide real-time detection of fraudulent Zelle transactions.  
- Increase detection accuracy and reduce unnecessary alerts.

**Business Background:**  
- FIS offers a Zelle fraud monitoring service using IBM Safer Payments' rules engine.  
- The system uses manually written rules derived from previously confirmed fraud data.

**Related Regulated Requirements:**  
- Adhere to financial regulations mandating transaction monitoring and fraud reporting.  
- Comply with industry standards for real-time detection of suspicious transactions.




Business Objectives:

Provide real-time detection and alerting of potentially fraudulent transactions for retail digital payment products such as Zelle.
Enhance the accuracy of fraud monitoring to support timely investigation by the bank.
Business Background:

FIS offers a premier transaction monitoring service powered by IBM Safer Payments.
The service is designed for retail digital payment products and is implemented using a rule-based system.
Manually written rules are developed by analyzing historical, client-confirmed fraud data, which drive the transaction monitoring and alerting process.
Related Regulated Requirements:

Compliance with financial regulations requiring continuous transaction monitoring and prompt reporting of suspicious activity.
Adherence to AML and KYC standards mandated by banking regulatory authorities.

UAT testing for IBM Safer Payments is conducted as part of FIS’s comprehensive change management and SDLC procedures. When updating data feeds or applying tool enhancements (such as upgrades, patches, and maintenance), the following process is followed:

Change Management & SDLC:
FIS adheres to established change management procedures for all updates feeding into IBM Safer Payments, ensuring that tool enhancements are rigorously planned, tested, and documented.

UAT Testing:
In the UAT environment, each new rule is reviewed by a dedicated analyst for accuracy—this review confirms that the rule’s configuration is correct without altering the original logic.

If a rule’s alerts exceed predefined thresholds, it is escalated to a manager for additional review and correction before moving to production.
Production Rollout:
After successful UAT testing, the updates are deployed to production, where ongoing monitoring ensures performance aligns with FIS’s fraud detection objectives.




In the production environment, the bank uses Zelle for digital payments, integrated within its mobile and online banking platforms. FIS, which owns both Zelle and IBM Safer Payments, manages the entire fraud detection process. When a Zelle transaction is initiated, transaction data is automatically collected from the digital banking channels. IBM Safer Payments then screens this data in real time using a rule-based fraud monitoring system. This managed solution ensures that every transaction is checked for suspicious activity before it is processed, with alerts generated if any risk is detected.


One key setting is the targeted good-to-bad ratio, which is set between 3:1 and 5:1. This ratio is used as a threshold to help minimize false positives by ensuring that for every fraudulent alert (bad), the system verifies that there are at least 3 to 5 legitimate transactions (good) under similar conditions.


Input Data:

The system receives transaction data, which includes the Zelle receiver token and the transaction amount.
Rule Evaluation:

The IBM Safer Payments rules engine processes this data using manually written rules to assess the transaction’s risk.
Decision Making:

High Risk: The transaction is declined.
Mid Risk: The transaction is accepted but flagged for review.



Purpose & Scope

FIS IBM Safer Payments is used for real-time fraud transaction monitoring in the Digital Banking production environment.
It helps identify and mitigate fraudulent transactions as part of the fraud detection program.
Process & Review

The Digital Payments Fraud Team (FIS) reviews cases flagged by FIS IBM Safer Payments.
Cases are triggered when transactions show fraud indicators or have a history of fraud, as identified by the FIS team.
If a transaction is not fraudulent, the case is closed.
If fraud is confirmed, the affected account and any linked accounts are blocked.
Handling Suspicious Transactions

Some cases require further investigation before a final decision can be made.
In such cases, the Digital Payments Fraud Team (FIS) contacts the bank for additional validation.
Extra verification measures should be in place when the bank reaches out to customers to avoid engaging with potential fraudsters.
Response to Confirmed Fraud

If fraud is confirmed, the bank should:
Immediately suspend access to the Zelle profile.
Notify the Digital Payments Fraud Team (FIS) about fraudulent activity and any related transactions.
Ensure compliance with network participation requirements

This section is not applicable as the model operates on a rule-based framework. There are no parameters learned from the data since no model training is performed. The decision-making process relies entirely on predefined rules rather than statistical or machine-learning-based optimization.




This section is not applicable for SecurLock but is applicable for FICO Falcon, as SecurLock operates by leveraging the risk scores generated by FICO Falcon within its decision-making process.








Black Box Search Parameters – No Fine-Tuning
The Bridger search options allow users to configure certain parameters beyond the list screening score, but these parameters function as black box settings. This means they can only be activated or deactivated, with no option for fine-tuning or customization beyond turning them on or off.




The Alert to Transaction Ratio (ATR) measures the proportion of transactions that trigger an alert in a monitoring system. It helps assess the effectiveness and efficiency of the model in identifying suspicious activities.

A higher ratio may indicate that the model is generating too many alerts (possibly false positives), while a lower ratio may suggest that the model is not capturing enough suspicious transactions.

Formula
Alert to Transaction Ratio
=
Number of Alerts
Number of Transactions Processed
Alert to Transaction Ratio= 
Number of Transactions Processed
Number of Alerts
​
The Alerts-to-Transaction Ratio for each quarter is presented in the table.

The results indicate a trend in alert activity, reflecting the overall transaction monitoring behavior.
 


The Alert-to-SAR Ratio measures the efficiency of the alerting system by comparing the total number of alerts generated to the number of Suspicious Activity Reports (SARs) filed (or confirmed issues). It helps in assessing whether the alert thresholds are appropriately set and if the monitoring system is effectively identifying true suspicious activity.




The SAR-to-Alert Ratio measures the proportion of total alerts that result in actual Suspicious Activity Reports (SARs) or confirmed suspicious cases. This metric helps assess the effectiveness of the alerting system—whether it generates meaningful alerts or too many false positives.


Threshold Descriptions:
SAR-to-Alert Ratio > 20% → Highly Effective Alerting System (Green)

A high proportion of alerts result in SAR filings, indicating that the system generates high-quality alerts.

Suggests well-calibrated detection rules with minimal false positives.

SAR-to-Alert Ratio between 5% and 20% → Moderately Effective Alerting System (Amber)

A reasonable number of alerts lead to SARs, but there are still some false positives.

The system captures suspicious activities but may require fine-tuning to improve precision.

SAR-to-Alert Ratio < 5% → Inefficient Alerting System (Red)

A very low proportion of alerts result in SAR filings, indicating a high false positive rate.

The system may be generating too many unnecessary alerts, leading to wasted resources.

Requires adjustments to risk thresholds, filtering rules, or detection models to improve efficiency.



We have computed alerts by segments for each quarter, and the results are shown below.

The results indicate a [consistent/fluctuating/increasing/decreasing] trend for the particular segment.



The alerts by segment have been analyzed to identify trends over the monitoring periods. Based on the alert volumes and changes observed, the following thresholds categorize the trends:

Stable Trend (Green) → No Significant Change

The number of alerts within the segment has remained relatively consistent across quarters.

Indicates a stable transaction pattern with no major shifts in risk exposure.

Moderate Shift (Amber) → Noticeable Change in Alerts

The segment shows a gradual increase or decrease in alerts over time.

May indicate evolving transaction behaviors, requiring ongoing monitoring.

Further analysis may be needed to determine if the shift is due to business changes or risk factors.

Significant Spike or Drop (Red) → High-Risk Indicator

A sharp increase in alerts suggests a potential rise in suspicious activities, requiring further investigation.

A steep decline in alerts may indicate missed detections or changes in screening thresholds.

Requires immediate review to assess potential risks and ensure compliance effectiveness.

This framework helps in effectively tracking segment-wise alert trends and ensuring timely risk assessment and mitigation.





False Positive Ratio in Fraud Monitoring Model
Definition:
The False Positive Ratio in a fraud monitoring model measures the proportion of flagged alerts that turn out to be non-fraudulent upon investigation. A high false positive ratio indicates that the model is generating too many incorrect alerts, leading to unnecessary investigations and wasted resources.

Formula:
False Positive Ratio
=
False Positive Alerts
Total Alerts Generated
False Positive Ratio= 
Total Alerts Generated
False Positive Alerts
​
 
Interpretation:
Higher False Positive Ratio → The model is flagging too many legitimate transactions as fraudulent, leading to excessive manual reviews.

Lower False Positive Ratio → The model is effectively identifying actual fraudulent activities with minimal false alerts, improving efficiency.

Thresholds for False Positive Ratio (RAG Status)
False Positive Ratio < 20% (Green) → Highly Efficient Model

The majority of flagged alerts are genuine fraud cases, indicating a well-tuned fraud detection system.

Minimal wasted effort on false investigations.

False Positive Ratio between 20% and 50% (Amber) → Moderate Efficiency

A moderate number of false positives, meaning the model is somewhat effective but requires fine-tuning.

Some resources are spent on investigating non-fraud cases, but fraud detection remains reliable.

False Positive Ratio > 50% (Red) → Poor Model Performance

More than half of the alerts flagged by the model are false alarms, leading to excessive manual reviews.

Indicates overly strict rules or misaligned thresholds that need adjustment to improve accuracy.

Results Interpretation Statement:
"The results indicate a [stable/increasing/decreasing] false positive trend, suggesting that the fraud monitoring model [is performing optimally/requires further tuning to reduce false alerts]."

Would you like any refinements based on specific fraud scenarios? 😊






The False Positive Ratio in a fraud monitoring model represents the percentage of alerts that are later determined to be non-fraudulent upon investigation. A well-balanced fraud detection system should minimize false positives while ensuring that genuine fraudulent activities are detected effectively.

Formula:
False Positive Ratio
=
False Positive Alerts
Total Alerts Generated
False Positive Ratio= 
Total Alerts Generated
False Positive Alerts
​
 
Interpretation:
A higher false positive ratio may indicate that the model is generating a large number of alerts that do not correspond to actual fraudulent activities, leading to additional manual reviews and operational inefficiencies.

A lower false positive ratio suggests that the model is successfully distinguishing between fraudulent and non-fraudulent transactions, ensuring a more efficient and accurate monitoring process.

Thresholds for False Positive Ratio (RAG Status)
False Positive Ratio < 20% (Green) → Well-Calibrated Model

The majority of flagged alerts are confirmed fraud cases, indicating that the model is performing efficiently.

Investigations are well-targeted, minimizing unnecessary manual reviews.

False Positive Ratio between 20% and 50% (Amber) → Moderate Efficiency

Some false positives are present, suggesting the need for further refinement of detection rules.

While the model is reasonably effective, adjustments may enhance its accuracy.

False Positive Ratio > 50% (Red) → High False Positive Rate

A significant proportion of alerts do not result in confirmed fraud, leading to increased operational workload.

Fine-tuning the model parameters could help improve precision and reduce unnecessary alerts.

Results Interpretation Statement:
"The results indicate a [stable/slightly increasing/slightly decreasing] false positive trend, suggesting that the fraud monitoring model is [performing well/could benefit from minor refinements/may require further optimization to enhance accuracy]."

Would you like any modifications to align with specific requirements? 😊








You said:
Thresholds for False Positive Ratio (RAG Status)
False Positive Ratio < 20% (Green) → Well-Calibrated Model

The majority of flagged alerts are confirmed fraud cases, indicating that the model is performing efficiently.

Investigations are well-targeted, minimizing unnecessary manual reviews.

False Positive Ratio between 20% and 50% (Amber) → Moderate Efficiency

Some false positives are present, suggesting the need for further refinement of detection rules.

While the model is reasonably effective, adjustments may enhance its accuracy.

False Positive Ratio > 50% (Red) → High False Positive Rate

A significant proportion of alerts do not result in confirmed fraud, leading to increased operational workload.

Fine-tuning the model parameters could help improve precision and reduce unnecessary alerts
i want description of thresholds as above.


ChatGPT said:
Thresholds for False Positive Ratio (RAG Status)
False Positive Ratio < 20% (Green) → Well-Calibrated Model
The model is effectively distinguishing between fraudulent and non-fraudulent activities, ensuring a low false positive rate.

Investigations are efficiently targeted, minimizing unnecessary manual reviews.

The fraud detection system is well-optimized, resulting in a high level of accuracy.

False Positive Ratio between 20% and 50% (Amber) → Moderate Efficiency
A moderate level of false positives is observed, suggesting that the model is performing reasonably well but has room for improvement.

Some legitimate transactions may be incorrectly flagged, requiring additional manual reviews.

Fine-tuning detection rules and refining risk parameters could enhance accuracy while maintaining a balance between fraud detection and operational efficiency.

False Positive Ratio > 50% (Red) → High False Positive Rate
A significant proportion of alerts turn out to be non-fraudulent, leading to excessive manual investigations and resource inefficiencies.

The high false positive rate may indicate overly strict detection rules or misaligned model thresholds.

Adjusting model parameters, refining screening criteria, or incorporating additional fraud indicators could help reduce unnecessary alerts and improve precision.

This structured approach helps in assessing fraud detection effectiveness while ensuring an optimal balance between risk identification and operational efficiency.




The Alerts by Segment Ratio reflects the proportion of fraud or compliance alerts within specific customer or transaction segments. A lower ratio is preferable, as it indicates that screening measures are effectively distinguishing between legitimate and suspicious activity without generating excessive alerts.

Formula:
Alerts by Segment Ratio
=
Total Alerts in a Segment
Total Transactions in that Segment
Alerts by Segment Ratio= 
Total Transactions in that Segment
Total Alerts in a Segment
​
 
Thresholds (RAG Status):
🟢 Green (< 5%) – Well-Controlled Segment
A low alert-to-transaction ratio suggests that risks in this segment are well managed, with minimal disruption to legitimate transactions. The screening model is effectively calibrated.

🟠 Amber (5% - 15%) – Emerging Risk Segment
A moderate alert rate indicates potential concerns, warranting closer observation. Refinements to screening parameters may be needed to maintain a balance between detection accuracy and operational efficiency.

🔴 Red (> 15%) – High-Risk Segment
A high alert frequency suggests increased fraud or compliance risks. This segment may require enhanced monitoring, stricter controls, or fine-tuning of detection thresholds to reduce unnecessary alerts.

Results Interpretation Statement:
"The results reveal a [stable/increasing/decreasing] trend in alerts for this segment, signaling [effective screening, the need for closer oversight, or potential recalibration of detection criteria] to optimize risk management."





If the absolute deviation (increase or decrease) is 10 or less, the metric remains within the acceptable range and is classified as Green (No Action Required)."

2️⃣ Yellow: "If the absolute deviation (increase or decrease) is greater than 10 but not exceeding 20, the metric is classified as Yellow (Caution Zone), indicating a moderate deviation that may require monitoring."

3️⃣ Red: "If the absolute deviation (increase or decrease) is greater than 20, the metric is classified as Red (Critical), requiring immediate investigation and corrective action.

We have calculated the ATR metrics for recent quarters. Additionally, we compare the current quarter’s results with the rolling average of the past two quarters to smooth short-term fluctuations, capture underlying trends, and enhance stability in performance assessment


Our approach involves calculating the absolute difference between the recent quarter's ATR ratio and the six-month rolling average, then evaluating whether the quarterly values fall within the predefined thresholds to ensure a stable and consistent performance assessment.


The False Positive Rate (FPR) measures the proportion of total alerts that were ultimately classified as "Not Suspicious." It is calculated as:

False Positive Rate
=
Alerts Classified as "Not Suspicious"
Total Alerts
False Positive Rate= 
Total Alerts
Alerts Classified as "Not Suspicious"
​
 
A high FPR indicates that a significant number of alerts are being incorrectly flagged as suspicious, leading to operational inefficiencies, increased manual review workload, and unnecessary investigations.

However, a low FPR may suggest that the system is too restrictive, potentially missing legitimate suspicious activity and increasing the risk of undetected fraud or compliance violations.





The Q4 SAR-to-Alert Ratio is 5.22%, compared to the rolling average of the previous two quarters at 2.69%, resulting in an absolute percentage difference of 94.10%, which exceeds the 20% threshold and raises concerns about the model’s reliability.

Similarly, in Q4, the SAR-to-Alert Ratio is 1.45%, whereas the rolling average of the previous two quarters is 3.73%, leading to an absolute percentage difference of 61.13%, which exceeds the 20% threshold. In this case, the ratio is decreasing, which also indicates potential model instability.

Since any absolute percentage difference beyond 20% is considered suspicious, these deviations suggest possible model inconsistencies, changes in alerting patterns, or shifts in underlying risk trends, warranting a thorough investigation.



The absolute percentage difference for FPR is 1.15% for Q3 and 6.2% for Q4, both classified as Green, as they fall within the 10% threshold. This indicates that the FPR for Q3 and Q4 aligns with the previous two rolling quarters, suggesting model stability with no significant deviations warranting concern.




Alert by Segments monitors shifts in the number of alerts across different population groups, providing insight into changes in alert patterns. A high drift may indicate that the model is generating excessive alerts, potentially increasing false positives, whereas a low drift may suggest the model is missing suspicious transactions. Continuous monitoring helps ensure balanced detection and model effectiveness.



Green (Stable): The value is within ±2 standard deviations of the rolling average of the previous two quarters, indicating no significant drift.

Red (Critical): The value is outside ±2 standard deviations of the rolling average of the previous two quarters, signaling a potential shift in alert patterns that requires further investigation.



The results indicate that the Alert-to-Transaction Ratio has remained stable across quarters, with minimal deviation from the rolling average. Since the absolute percentage difference for Q3 (2.43%) and Q4 (5.61%) falls within the Green threshold, there are no signs of significant drift in alert generation.



We use the rolling average as it smooths short-term fluctuations, captures trends over time, and reduces the impact of temporary spikes or anomalies. S

The analysis indicates that the false positive rate is within the expected range. The absolute percentage differences across Q1, Q2, Q3, and Q4 remain within the green threshold (i.e., within 10% of the rolling average), demonstrating consistent model behavior and effective control over false positives.



For Q3 and Q4, the total alerts to total transactions ratio is within the expected range, with absolute percentage differences remaining within the 10% threshold. This indicates that the alert levels are aligned with the transaction volumes.


This difference is subsequently compared against established thresholds to assess the model's performance and verify that it operates within stable and consistent parameters. The rolling average is used to smooth out short-term changes, reduce volatility, and provide a strong basis for analyzing trends. This method enhances anomaly detection and supports data-driven, well-informed decision-making.



Based on the analysis for Q1, Q2, Q3, and Q4, the absolute percentage difference between the current quarter's ratio and the rolling average has consistently exceeded 20%, resulting in all quarters being flagged in red. This significant deviation indicates that the model's performance is not meeting expected benchmarks, suggesting potential anomalies in alert generation or shifts in underlying activity patterns. A detailed investigation is recommended to identify the root causes and implement appropriate corrective measures.



Based on the analysis for Q1, Q2, Q3, and Q4, the absolute percentage difference between the current quarter's false positive rate and the rolling average of the previous two quarters has consistently remained within 10%, resulting in all quarters being flagged in green. This indicates that the false positive rates are within the expected range, reflecting stable and consistent performance. Such consistency suggests that the model is effectively managing false positives, and no significant fluctuations are present that would otherwise necessitate further investigation


Based on the analysis for Q1, Q2, Q3, and Q4, all quarters are flagged in green, indicating that the false positive rates remain within the acceptable range (within 10%). This outcome demonstrates that the model's handling of false positives is both stable and consistent, reflecting effective performance management without significant fluctuations.




Based on the analysis for Q3 and Q4, both quarters are flagged in green for the total alerts to total transaction volume metric, with the absolute percentage difference within 10%. This indicates that the alert levels remain within the expected range, reflecting stable performance relative to transaction volume.




The bank is currently using a Phase 1 implementation of the Actimize model, which is based on predefined rules. This approach lacks independent measures to validate the success of the detection models, thereby limiting objective performance assessment. With the transition to Phase 2, the SAM model will evolve into a machine learning framework. This advancement will facilitate a more predictive approach and enable the use of robust statistical measures—such as ROC curves, KS statistics, and other relevant metrics—to independently evaluate and validate model performance




Based on the quarterly analysis for Q1, Q2, Q3, and Q4, the SAR to Total Alerts ratio is within the acceptable threshold (within 5%) for Q1, Q2, and Q4, with these quarters flagged in green. However, Q3 exceeds the 5% threshold and is flagged in yellow. This indicates that, for Q3, the proportion of suspicious activity reports relative to total alerts is higher than anticipated. 



Q1 Analysis of Alerts by Segment
The absolute percentage difference in alert volumes across different segments has been categorized into green (≤10%), yellow (10%-20%), and red (>20%) zones based on predefined thresholds.

Segments in the Green Zone (≤10%) – Changes in Alerts Within Expected Range
The following segments exhibit changes in alert volumes that remain within the expected range, indicating stability:

Low-Risk High Net Worth (including Digital Banking)

Medium-Risk

Organizational – High

Organizational – Low

For these segments, no immediate concerns arise as the alert levels are consistent with expectations.

Segments in the Yellow Zone (10%-20%) – Noticeable Change in Alerts
The absolute percentage difference for the following segments falls within the yellow zone, indicating a noticeable change in alert volumes:

High-Risk

Low-Risk Low Net Worth – Digital Banking

These segments should be monitored to assess whether the trend continues and to identify potential contributing factors.

Segments in the Red Zone (>20%) – Significant Change in Alerts
Only the Low-Risk Low Net Worth segment falls within the red zone, reflecting a significant change in alert volumes. This segment requires further investigation to determine underlying causes and assess potential risks.

Conclusion
While most segments remain within the expected range, the low-risk low net worth segment shows a significant change and requires immediate attention. Segments in the yellow zone should also be closely monitored to track ongoing trends and potential shifts in alert patterns.



Overall, the analysis shows that while most segments maintain alert changes within the expected range (green zone), the high-risk segment and the low-risk low net worth digital banking channel exhibit noticeable changes (yellow zone). The traditional low-risk low net worth segment, however, presents a significant change (red zone) and warrants further investigation.



Most segments exhibit stable alert volumes within the expected range. However, the high-risk segment and the low-risk low net worth digital banking channel show noticeable deviations, requiring ongoing monitoring to assess potential risks. The traditional low-risk low net worth segment, with a significant change in alert volumes, demands a deeper investigation to identify underlying causes and mitigate any emerging issues.



All bank customers undergo sanctions screening as part of the bank's compliance framework. As of December 31, 2024, EWB's total assets amount to $75.98 billion.

Since the model is applied for sanctions screening across all customer transactions, the historical transaction volume and trends would align with the bank's overall transaction activity. 



Bridger XG allows customization of search options (Match, General, and Payment Screening), which can be activated or deactivated. It also supports configurable watchlists, where specific regulatory or internal lists can be selected for screening; alert thresholds, which define the sensitivity for flagging potential matches; and false positive thresholds, which help reduce unnecessary alerts by adjusting match confidence levels. Predefined searches enable tailored settings for different screening processes, such as payment vs. customer screening.

Existing Models

Before implementing Bridger XG, the bank used Paysafe as its legacy payment screening model. The transition to Bridger was undertaken to enhance screening effectiveness, improve compliance with regulatory requirements, and reduce false positives through advanced search configurations and optimized alert thresholds.
