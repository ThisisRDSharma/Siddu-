Bridger Screening – Process Flow Overview
1. Screening Initiation
The process begins with the selection of the screening mode: real-time or batch.

Real-time screening is triggered immediately during events such as customer onboarding or real-time customer payment processing. As customer or payment data is entered, it is instantly forwarded for screening.

Batch screening is scheduled and performed using a pre-formatted spreadsheet containing multiple entity details, typically for periodic or large-scale compliance checks.

Based on the entity type, the required input details differ:

Individual Screening: Includes name fields, identification details (e.g., SSN, date of birth, national ID, citizenship), and address components (street, city, state, country, telephone).

Business Screening: Requires the business name, EIN, relevant identification fields (ID number, issuing country, issue date, expiration date), and address. For certain cases, additional parameters such as vessel, airport, and seaport information may be included to support extended OFAC checks.
2. Screening Execution
Once the entity or transaction information is submitted, it is directly screened against various internal and external watchlists (e.g., OFAC, PEPs, sanctions, adverse media lists).

Based on the results of this screening:

If no matches are found, the process concludes without any further action.

If one or more potential matches are identified, an alert is generated for further review.

3. Alert Generation & Initial Review
An alert is automatically created when the system detects potential watchlist matches.

The initial reviewer performs the following tasks:

Compares the submitted data of the screened entity or transaction against the watchlist records associated with the alert.

Assesses each match to determine whether it is a False Positive (FP) or a Potential Hit (PH).

Records a disposition for each match based on this analysis.

Two possible scenarios emerge:

Scenario A – All Matches are False Positives:
The entire alert is marked as a false positive and routed to an approver for secondary review.

Scenario B – Mixed/Unclear Matches:
The alert is marked as “undetermined” and a note (e.g., “second review requested”) is added. The alert is then escalated to Approver 1 for further assessment.

4. Secondary (Approver) Review Process
The designated approver receives the alert and:

Reviews the screened data, the matched watchlist records, and the disposition notes provided by the initial reviewer.

Based on this review, the following actions may be taken:

Confirmation & Closure:
If all matches are validated as false positives, the approver confirms the initial review, adds a note such as “verified disposition,” and closes the alert.

Reassignment to Initial Reviewer:
If discrepancies are found or the analysis is incomplete, the alert is sent back to the initial reviewer with comments for correction. Once updated, the reviewer resubmits the alert for approval.

Further Clarification Needed:
If the alert cannot be resolved at this stage, its status remains “undetermined” and it is forwarded to Approver 2 with a note such as “OFAC review requested.”

5. Regulatory Escalation
If the alert involves a confirmed match to a high-risk category such as PEPs, adverse media, or enforcement lists, it is referred to the bank compliance team. They may:

Close the alert, and

Mark the account as high risk in accordance with internal risk management policies.

In cases where the alert involves a potential match to sanctioned entities or individuals that cannot be ruled out as a false positive, the case is referred to the head office OFAC group for further analysis and decision-making.|


6. Batch Screening Specifics
For batch processes:

A spreadsheet containing multiple customer or business records is submitted for watchlist screening.

Any generated alerts appear in the alert inbox of the designated reviewer(s).

These alerts follow the same review, disposition, and escalation process as those in real-time screening.


4. Secondary (Approver) Review Process
The designated approver receives the alert and:

Reviews the screened data, the matched watchlist records, and the disposition notes provided by the initial reviewer.

Based on this review, the following actions may be taken:

Confirmation & Closure:
If all matches are validated as false positives, the approver confirms the initial review, adds a note such as “verified disposition,” and closes the alert.

Reassignment to Initial Reviewer:
If discrepancies are found or the analysis is incomplete, the alert is sent back to the initial reviewer with comments for correction. Once updated, the reviewer resubmits the alert for approval.

Further Clarification Needed:
If the alert cannot be resolved at this stage, its status remains “undetermined” and it is forwarded to Approver 2 with a note such as “OFAC review requested.”
The alert has now been reassigned to the bank compliance team for review.

5. Regulatory Escalation
After the alert is reassigned to the bank compliance team, they conduct a final assessment of the watchlist match and take one of the following actions:

For a true match to Politically Exposed Persons (PEPs), adverse media, or enforcement lists, the compliance team may:

Close the alert, and

Mark the account as high risk in accordance with internal risk policies.

For potential hits against sanctioned lists that cannot be dispositioned as false positives, the alert must be escalated to the head office OFAC group for further analysis and decision-making.



A False Positive Confidence Score indicates the likelihood that a match against a watchlist is not a true hit, helping to reduce unnecessary manual reviews. IMDS uses a set of rules to automatically evaluate matches by analyzing the input data, list details, and match attributes from XG searches. These rules look for evidence suggesting a false positive, and the results are used to calculate the confidence score.


A False Positive Confidence Score indicates the likelihood that a match against a watchlist is not a true hit, helping reduce manual effort on low-risk alerts. The bank defines rules within the IMDS framework to automatically evaluate matches by analyzing input data, list characteristics, and match attributes from XG searches. These rules identify patterns consistent with false positives, and the results are used to generate the confidence scores

BSA/AML Compliance Team
→ Uses outputs to investigate and report suspicious activity




 process of moving a validated model into a live environment, ensuring it's integrated smoothly and used for real-time decision-making by coordinating across development, IT, and business teams?s



Was SQL the only tool used for data extraction, or were there any additional tools or software involved in the process?





🧠 Estimation Methodology for Bridger Sanctions Screening Model
The Bridger XG sanctions screening model is designed to detect potential matches between customer input data and watchlist entities (e.g., OFAC, UN, EU lists). It uses a combination of fuzzy matching algorithms and automated false positive handling to balance detection accuracy with operational efficiency.

🔍 1. Fuzzy Matching Algorithm (XG Engine)
Bridger XG uses a fuzzy matching algorithm to compare the input entity (e.g., a customer’s name, address) against entries in sanction and watchlists.

Each potential match is assigned a match score, typically ranging from 70 to 100, which indicates the strength of the similarity between the input and the list entity.

🤖 2. Automatic False Positive Handling (IMDS Integration)
To address the issue of false positives, Bridger Insight XG integrates with IMDS (Integrated Matching Decision System):

The IMDS module allows the bank to develop and implement rules that automatically identify and process false positives, reducing manual review.

These rules can be customized to align with the institution's risk profile and list screening policies.

🧾 3. Rule-Based Decisioning – Standard Rules
Bridger XG comes with a set of standard rules, which the user can configure.

These rules evaluate conflicting data attributes between the input and list entity, including:

Date of birth (DOB) – with a user-defined tolerance (in months)

ID numbers

Gender

Addresses

Countries

If only the specified standard rules return true (indicating data conflicts), the system automatically classifies the match as a false positive.

⚠️ 4. Overrides for Critical Conflicts
However, if key identity elements like:

Addresses

Dates of birth

ID numbers

Phone numbers

... show a strong match (even if standard rules indicate a false positive), Bridger XG will override the standard rule logic and set the match status to automatic false positive to prevent potentially risky mismatches from being wrongly cleared.





Could you please provide a concise overview of the comprehensive data methodology employed, detailing the extraction process, reconciliation steps, applied transformations, underlying assumptions and limitations, quality controls and treatments, as well as the filtering and exclusion criteria?



Could you please provide details on the software platform and programming language used for model development, along with the process and outcomes of any vendor model tuning or customization?
Vendor model tuning customizes a pre-built model to work effectively in a specific environment. 

Could you please provide a summary of the model's assumptions, including the materiality of each assumption, alternative approaches explored, and details regarding any segmentation approach if performed?

Note: Based on our understanding, segmentation may not be applicable as the population data has not been segmented. Additionally, please clarify whether segmentation was performed based on entity type.

 Could you please share details on how the model’s overall performance has been tested, including whether any backtesting has been done? If so, please explain what kind of checks were performed during backtesting—such as comparing model results against actual outcomes—to assess how well the model is working.

Note: Tests for statistical assumptions, model fit, stability, overfitting/underfitting, and explainability are not applicable, as this is not a machine learning model and such issues do not arise.



Could you please provide details of the model parameters and their corresponding setting values used during model development?

Question 2: Could you also share information on model access and security controls, usage restrictions, and the process followed for deploying the model into production?s
Could you please confirm whether the model is used for customer screening, payment screening, or both, given that the same set of attributes appears to be used in each case?

Bridger Insight® XG offers both standard and customizable rule-based approaches to enhance the accuracy of list screening and reduce false positives.​

Standard Rules: These are predefined rules that detect specific data conflicts between input and list entities. When a specified conflict is detected, the match is automatically flagged as a false positive. These rules have a limited scope, primarily targeting straightforward, predefined data conflicts.​

Intelligent Match Decision Solution (IMDS): IMDS allows banks to develop custom rules tailored to their screening programs and risk profiles. These rules combine input, list, and match attributes to evaluate matches, going beyond basic data element conflicts. IMDS generates a false positive confidence score, improving alert accuracy and aligning with the bank’s specific compliance requirements.

Bridger offers various search options that influence the final score for each match. The watchlists, alert thresholds, and associated search options can be configured through predefined searches, enabling customization for different screening processes, such as payment screening and customer screening. These search options include match options, general options, and payment screening options.

. The match confidence score thresholds range from 50 to 100, helping to determine the strength of each match.



Column Name 

Purpose 

application_id 

Unique ID for each applicant 

application_date 

For daily/weekly volume tracking 

product_type 

Helps to segment monitoring if needed 

acuant_api_triggered_flag 

1 if Acuant was triggered for applicant 

acuant_response_status 

Success or Failure of Acuant response 

acuant_response_time_sec 

Time from request to response in seconds 

acuant_final_decision 

Accept / Reject decision by Acuant 

photo_tampering_flag 

1 if photo tampering detected 

text_tampering_flag 

1 if text tampering detected 

physical_presence_flag 

1 if physical document spoof detected 

manual_review_required_flag 

1 if applicant was manually reviewed post-Acuant 

final_kyc_decision 

Approved / Rejected by the bank (final onboarding decision) 

document_upload_quality_flag 

1 if document upload was blurry or unreadable 

fraud_case_reported_flag 

1 if applicant later found to be fraud 


Column Name 

Purpose 

application_id 

Unique ID for each applicant 

application_date 

For daily/weekly volume tracking 

product_type 

Helps to segment monitoring if needed 

acuant_api_triggered_flag 

1 if Acuant was triggered for applicant 

acuant_response_status 

Success or Failure of Acuant response 

acuant_response_time_sec 

Time from request to response in seconds 

acuant_final_decision 

Accept / Reject decision by Acuant 

photo_tampering_flag 

1 if photo tampering detected 

text_tampering_flag 

1 if text tampering detected 

physical_presence_flag 

1 if physical document spoof detected 

manual_review_required_flag 

1 if applicant was manually reviewed post-Acuant 

final_kyc_decision 

Approved / Rejected by the bank (final onboarding decision) 

document_upload_quality_flag 

1 if document upload was blurry or unreadable 
5. Example with Hypothetical Numbers

Suppose in 1 day:

· 10,000 applicants

· 9,950 successfully processed by Acuant

· 100 flagged for photo tampering

· 50 flagged for text tampering

· 25 flagged for physical presence issues

· 5 fraud cases later reported from applicants Acuant accepted

Metrics would be:

· Acuant Utilization Rate = 9,950/10,000 = 99.5% ✅

· Photo Tampering Rate = 100/9,950 ≈ 1% ✅

· Text Tampering Rate = 50/9,950 ≈ 0.5% ✅

· Physical Presence Issue Rate = 25/9,950 ≈ 0.25% ✅

· False Negative Proxy Rate = 5/9,950 ≈ 0.05% ✅

All numbers within healthy, expected bands.

fraud_case_reported_flag 

1 if applicant later found to be fraud 
=IF(RANK(RAND(),$A$1:$A$10000)<=50,0,1)


Mode of Extraction:
Whether the development data was pulled automatically through ETL processes or manually using ad-hoc queries or exports.

Source Systems:
Systems or platforms from which the raw data was originally obtained.

Reconciliation Steps:
Methods used to verify that the extracted data aligns with source records, such as matching record counts or unique IDs.

Data Transformations:
Changes applied to raw data, including formatting, feature creation, or aggregation.

Assumptions Made:
Logic or filters applied during data preparation, such as using the latest available status or excluding certain values.

Dataset Limitations:
Known issues or gaps in the dataset that may affect model development, such as incomplete history or missing variables.

Data Quality Checks:
Validation steps to ensure accuracy, such as checking for nulls, duplicates, or inconsistencies.

Data Treatments:
Handling of data issues through techniques like missing value imputation, outlier treatment, or text standardization.

Model parameters and settings are applicable only for AI/ML-based models; since this is not an AI/ML model, it is not applicable—however, please clarify if any such information is available or relevant.




Clarity on the model’s purpose, use, and existing implementation has been achieved; however, information on the unified process and data flow for Bridger XG’s transaction screening and customer screening is still needed.
thank you for providing clarity on the data extraction and reconciliation processes. To further our understanding, could you please share additional details regarding:

1. Regarding Software/Platform Used in Model Development

Please confirm the software platforms and tools utilized in developing the screening models. If this information is maintained by the vendor, kindly confirm and request the necessary details from them.

2. Regarding Model Assumptions, Materiality, Alternative Approaches, and Segmentation

Requesting information on the model's key assumptions and their materiality, any alternative methodologies considered, and whether segmentation based on entity type was performed. If these details are managed by the vendor, please confirm and obtain the relevant information from them.

Thank you for the clarity provided on the testing of the core logic. To further assess the overall performance, could you please share any internal metrics tracked by the vendor? If such metrics are maintained by the vendor, kindly request the relevant information from them.

As discussed during our recent call, you will be providing customer batch screening alert samples. Additionally, could you please provide alert samples for transaction screening as well?
Please share the bank's model risk monitoring plan, including key performance indicators (KPIs) used to track the model's effectiveness. If available, provide information on the frequency of monitoring and any established thresholds for these metrics
We require additional details from the bank regarding model usage controls, restrictions, and production deployment processes for Bridger XG



 data transformations performed, reconciliation processes, and filtering/exclusion criteria when data is screened through automated means.s

Thank you for the clarity on data extraction and reconciliation. Requesting further details on data transformation, reconciliation, filtering and exclusion criteria in automated screening, along with any data limitations and assumptions considered.
Thanks for the clarity. This information provides a good understanding of the


While basic clarity has been provided on the data extraction process, further details are needed on how EWB is performing extraction at their end, including the tools or systems used and the structure of the extracted data. In addition, a clearer understanding is required of how data transformation, reconciliation, and the application of filtering and exclusion criteria are being managed within the automated screening process. It would also be helpful to outline any data limitations and assumptions considered to ensure a complete and accurate understanding of the overall methodology.

Requesting details on the internal metrics proposed by the vendor to assess the performance and effectiveness of the automated screening process. Additionally, please share what specific data these metrics are being tracked on, including any benchmarks or thresholds being used for evaluation. 

Thanks for the explanation provided on the model output. Requesting the formal documentation that outlines the model output in detail.
Could you please provide sample alerts for customer batch screening? This would help in understanding the types of alerts generated and the criteria used for flagging them during the screening process.


In reference to the "Tuning Report" document, is the Paysafe model being used to screen wire transactions within the PayPlus system as part of the bank's legacy payment screening model? Could you please confirm if this integration is in place and provide any additional details on how it functions within the system?

[Add the line from the Tuning Report here]

The development data for LN is central to supporting the model’s objective: the accurate screening of customer and transaction information against regulatory watchlists to identify restricted or high-risk entities and ensure compliance with applicable regulations.
This dataset includes customer PII and payment instruction data with key attributes such as entity type, full name, date of birth, age, gender, address, unique identifiers (e.g., Social Security Number), and contact information. These attributes enable precise entity identification and verification.
The integration of mandated watchlists—such as those required under the USA PATRIOT Act, OFAC regulations, and other regulatory frameworks—enables the model to compare input data against sanctioned or restricted entities. Additionally, the inclusion of LN-administered FCC screening lists and enriched payment data further strengthens the model’s ability to evaluate all relevant elements within financial transactions.
Together, these data components ensure that the model is aligned with its compliance-focused objective and capable of supporting both real-time and periodic screening processes effectively.



In the detailed onboarding request, both the iAccepted time and event processed time are provided. These timestamps reflect the collective processing duration of the three models—Acuant, Azure, and iProov—used as part of digital onboarding for ID verification. Individual timestamps for each model are not available, so the specific processing time of each model cannot be determined separately.s



frameAvailable = true indicates that the iProov SDK is successfully loaded on the user's device. It means the SDK has been initialized, the camera is active, and the system is ready for biometric verification.

This status confirms that the SDK is operational and processing the camera feed

frameAvailable can be used to check the iProov load event indicator because it confirms that the SDK has initialized, the camera is active, and frame capture has started—implying the SDK is fully loaded and operational on the device.
Authentication time can be derived by calculating the difference between eventProcessedTime and iAcceptedTime. However, this represents the total time taken by the entire identity verification flow, including Acuant, Azure, and iProov, and not the time taken by each individual component

The authentication outcome, represented as 'passed' (True/False), is stored in the iProov JSON file. A value of 'True' indicates that the verification process was successful, meaning there was an exact match between the document image and the selfie, along with a successful liveness check. A value of 'False' indicates that either the images did not match or the liveness test faileds

Face Match Transaction ID is considered a better match as a unique technical identifier because it is generated uniquely for each authentication attempt. Unlike a user ID or token ID, which remains the same across multiple sessions, the transaction ID allows for accurate tracking of individual attempts

number of times a user attempts authentication after failing one or more times.t increments with each subsequent attempt until a successful authentication or a defined maximum limit is reached.
This refers to the platform or environment where the user performs the selfie verification:


uccess Rate by Channel

Formula: Successful authentications / Total sessions per channel

Use: Measure performance across platforms.

Average Time to Authenticate by Channel (if time is available)

Use: Gauge speed and efficiency per platform.

Drop-off Rate by Channel

Formula: Abandoned sessions / Total sessions per platform


Average Retry Count

Formula: Total retry attempts / Total sessions

Use: Measure how many tries users usually need.

First Attempt Success Rate

Formula: (Sessions where retry_count = 0 and status = success) / Total sessions

Use: Shows how often users get verified on the first try.

Does a true value for frameAvailable mean that the iProov SDK has loaded successfully and camera frames are being captured, while a false value indicates that frames are not available, suggesting the SDK did not load properly?
Success Rate by Channel

Formula: Successful authentications / Total sessions per channel

Use: Measure performance across platforms.
Liveness Rate (%) = (Number of Successful Liveness Checks / Total Authentication Attempts) × 100
Face Match Rate (%) = (Number of Successful Face Matches / Total Authentication Attempts) × 100


 1. Success Rate by Channel
Definition: % of successful verifications per platform (Web/iOS/Android).
Importance: Highlights platform-specific issues; helps improve user experience and performance.

✅ 2. First Attempt Success Rate
Definition: % of users who pass on the first try.
Importance: Indicates user ease; higher rate means smoother onboarding and lower drop-offs.

✅ 3. Average Retry Count
Definition: Average number of attempts before success.
Importance: Tracks user effort; high values suggest friction or usability problems.

✅ 4. Match Rate
Definition: % of attempts where selfie matches ID photo.
Importance: Measures accuracy of face match; low rate can signal quality or algorithm issues.

✅ 5. Liveness Rate
Definition: % of users who pass the liveness (anti-spoof) check.
Importance: Key for fraud prevention and regulatory compliance.s




Fraud Loss Prevention (FLP)

Formula:

FLP
=
Total Fraud Losses
−
Recovered Fraud Losses
FLP=Total Fraud Losses−Recovered Fraud Losses
Use: Tracks the amount of fraud prevented or recovered. A high FLP suggests that the system is minimizing fraud-related losses.

Customer Churn Due to Fraud

Formula:

Churn Rate
=
Customers Lost Due to Fraud
Total Customers
×
100
Churn Rate= 
Total Customers
Customers Lost Due to Fraud
​
 ×100
Use: Tracks how fraud detection systems impact customer retention. A higher churn rate indicates a negative impact on customer loyalty.

Precision and Recall

Precision:

Precision
=
True Positives
True Positives
+
False Positives
Precision= 
True Positives+False Positives
True Positives
​
 
Recall:

Recall
=
True Positives
True Positives
+
False Negatives
Recall= 
True Positives+False Negatives
True Positives
​
 
Use: Precision tells you how many of the flagged fraud cases are actually fraud, while recall tells you how many fraud cases were actually detected by the system.


Metric | Formula | Business Impact
Fraud Rate (bps) | Fraud Losses ($)÷Total Payment Value ($)×10,000\text{Fraud Losses (\$)} \div \text{Total Payment Value (\$)} \times 10,000Fraud Losses ($)÷Total Payment Value ($)×10,000 | % of payments lost to fraud. High fraud rate means bigger financial leakage.
Fraud Volume Rate (%) | Confirmed Fraud Count÷Total Transactions Count×100\text{Confirmed Fraud Count} \div \text{Total Transactions Count} \times 100Confirmed Fraud Count÷Total Transactions Count×100 | Shows how common fraud is among all transactions.
Revenue Lost Due to Fraud ($) | Total Confirmed Fraud ($)−Recovered Fraud ($)\text{Total Confirmed Fraud (\$)} - \text{Recovered Fraud (\$)}Total Confirmed Fraud ($)−Recovered Fraud ($) | Actual revenue that the business loses permanently.
Fraud Loss Prevention (FLP) | Total Fraud Losses−Recovered Fraud Losses\text{Total Fraud Losses} - \text{Recovered Fraud Losses}Total Fraud Losses−Recovered Fraud Losses | Shows effectiveness of fraud systems to minimize net losses.
Fraud Recovery Rate (%) | Recovered Fraud Losses÷Total Fraud Losses×100\text{Recovered Fraud Losses} \div \text{Total Fraud Losses} \times 100Recovered Fraud Losses÷Total Fraud Losses×100 | Shows how effective recovery efforts are.
Average Fraud Ticket Size ($) | Total Fraud Losses ($)÷Fraud Count\text{Total Fraud Losses (\$)} \div \text{Fraud Count}Total Fraud Losses ($)÷Fraud Count | Average loss per fraud event — indicates if attacks are small or massive.
Average Transaction Size ($) | Total Payment Value ($)÷Transaction Count\text{Total Payment Value (\$)} \div \text{Transaction Count}Total Payment Value ($)÷Transaction Count | Business health view: frauds targeting large vs small transactions.
Metric | Formula | Business Impact
True Positive Rate (TPR) / Fraud Detection Rate (FDR) (%) | TP÷(TP+FN)×100\text{TP} \div (\text{TP} + \text{FN}) \times 100TP÷(TP+FN)×100 | How much actual fraud you are successfully detecting.
False Positive Rate (FPR) (%) | FP÷(FP+TN)×100\text{FP} \div (\text{FP} + \text{TN}) \times 100FP÷(FP+TN)×100 | How much good business you are hurting by wrongly flagging.
Precision (Positive Predictive Value) (%) | TP÷(TP+FP)×100\text{TP} \div (\text{TP} + \text{FP}) \times 100TP÷(TP+FP)×100 | How accurate your fraud alerts are. Reduces investigation waste.
Recall (%) | Same as TPR/FDR | Same — are you catching most frauds.
F1 Score | 2×(Precision×RecallPrecision+Recall)2 \times \left( \frac{\text{Precision} \times \text{Recall}}{\text{Precision} + \text{Recall}} \right)2×(Precision+RecallPrecision×Recall​) | Balanced view: accuracy + coverage of fraud detection.
Alert Hit Rate (%) | Confirmed Fraud Alerts÷Total Alerts Generated×100\text{Confirmed Fraud Alerts} \div \text{Total Alerts Generated} \times 100Confirmed Fraud Alerts÷Total Alerts Generated×100 | How many alerts are actually useful — indicator of alert quality.
Metric | Formula | Business Impact
Alert-to-Action Time (hours or minutes) | Average Time between Alert and Disposition\text{Average Time between Alert and Disposition}Average Time between Alert and Disposition | Speed of reaction — critical for fraud containment.
Investigator Productivity (alerts/day) | Total Alerts Closed÷Total Investigation Hours\text{Total Alerts Closed} \div \text{Total Investigation Hours}Total Alerts Closed÷Total Investigation Hours | How many cases a fraud analyst is handling — impacts fraud cost.
Fraud per Investigator ($) | Total Fraud Detected ($)÷Number of Investigators\text{Total Fraud Detected (\$)} \div \text{Number of Investigators}Total Fraud Detected ($)÷Number of Investigators | Individual contribution to saving business money.
Manual Review Rate (%) | Manually Reviewed Alerts÷Total Alerts×100\text{Manually Reviewed Alerts} \div \text{Total Alerts} \times 100Manually Reviewed Alerts÷Total Alerts×100 | Indicates operational burden and automation needs.






Metric	Formula	Business Impact
Alert-to-Action Time (hours or minutes)	
Average Time between Alert and Disposition
Average Time between Alert and Disposition	Speed of reaction — critical for fraud containment.
Investigator Productivity (alerts/day)	
Total Alerts Closed
÷
Total Investigation Hours
Total Alerts Closed÷Total Investigation Hours	How many cases a fraud analyst is handling — impacts fraud cost.
Fraud per Investigator ($)	
Total Fraud Detected ($)
÷
Number of Investigators
Total Fraud Detected ($)÷Number of Investigators	Individual contribution to saving business money.
Manual Review Rate (%)	
Manually Reviewed Alerts
÷
Total Alerts
×
100
Manually Reviewed Alerts÷Total Alerts×100	Indicates operational burden and automation needs.


Metric	Formula	Business Impact
True Positive Rate (TPR) / Fraud Detection Rate (FDR) (%)	
TP
÷
(
TP
+
FN
)
×
100
TP÷(TP+FN)×100	How much actual fraud you are successfully detecting.
False Positive Rate (FPR) (%)	
FP
÷
(
FP
+
TN
)
×
100
FP÷(FP+TN)×100	How much good business you are hurting by wrongly flagging.
Precision (Positive Predictive Value) (%)	
TP
÷
(
TP
+
FP
)
×
100
TP÷(TP+FP)×100	How accurate your fraud alerts are. Reduces investigation waste.
Recall (%)	Same as TPR/FDR	Same — are you catching most frauds.
F1 Score	
2
×
(
Precision
×
Recall
Precision
+
Recall
)
2×( 
Precision+Recall
Precision×Recall
​
 )	Balanced view: accuracy + coverage of fraud detection.
Alert Hit Rate (%)	
Confirmed Fraud Alerts
÷
Total Alerts Generated
×
100
Confirmed Fraud Alerts÷Total Alerts Generated×100	How many alerts are actually useful — indicator of alert quality.



Metric	Formula	Business Impact
Fraud Rate (bps)	
Fraud Losses ($)
÷
Total Payment Value ($)
×
10
,
000
Fraud Losses ($)÷Total Payment Value ($)×10,000	% of payments lost to fraud. High fraud rate means bigger financial leakage.
Fraud Volume Rate (%)	
Confirmed Fraud Count
÷
Total Transactions Count
×
100
Confirmed Fraud Count÷Total Transactions Count×100	Shows how common fraud is among all transactions.
Revenue Lost Due to Fraud ($)	
Total Confirmed Fraud ($)
−
Recovered Fraud ($)
Total Confirmed Fraud ($)−Recovered Fraud ($)	Actual revenue that the business loses permanently.
Fraud Loss Prevention (FLP)	
Total Fraud Losses
−
Recovered Fraud Losses
Total Fraud Losses−Recovered Fraud Losses	Shows effectiveness of fraud systems to minimize net losses.
Fraud Recovery Rate (%)	
Recovered Fraud Losses
÷
Total Fraud Losses
×
100
Recovered Fraud Losses÷Total Fraud Losses×100	Shows how effective recovery efforts are.
Average Fraud Ticket Size ($)	
Total Fraud Losses ($)
÷
Fraud Count
Total Fraud Losses ($)÷Fraud Count	Average loss per fraud event — indicates if attacks are small or massive.
Average Transaction Size ($)	
Total Payment Value ($)
÷[Fraud_Metrics_Calculator_Complete.xlsx](https://github.com/user-attachments/files/19941945/Fraud_Metrics_Calculator_Complete.xlsx)

Transaction Count
Total Payment Value ($)÷Transaction Count	Business health view: frauds targeting large vs small transactions.



Hit Rate = Number of Bad Accounts / Number of Times Fraud Rule Fired
Explanation: Hit rate indicates the accuracy of a fraud detection rule by measuring the proportion of alerts raised by the rule that correctly identified fraudulent accounts. A higher hit rate suggests better rule performance with fewer false positives.



Metric thresholds have not been predefined; appropriate thresholds and corresponding escalation triggers will be determined based on performance analysis once sufficient data is available




