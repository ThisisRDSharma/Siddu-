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




[iProov_random_data.csv](https://github.com/user-attachments/files/19835780/iProov_random_data.csv)Session_ID,User_ID,Device_Type,Age,Ethnicity,Verification_Outcome,Timestamp
S1000,U1000,iOS,22,White/Caucasian,Pass,2025-04-21 12:04:25
S1001,U1001,iOS,43,Asian,Pass,2025-04-21 12:13:25
S1002,U1002,Web,37,Hispanic/Latino,Fail_FR,2025-04-21 12:07:25
S1003,U1003,Android,46,Hispanic/Latino,Pass,2025-04-21 12:14:25
S1004,U1004,iOS,30,Hispanic/Latino,Drop_off,2025-04-21 12:09:25
S1005,U1005,Web,72,Black/African,Pass,2025-04-21 12:14:25
S1006,U1006,Android,53,White/Caucasian,Pass,2025-04-21 11:48:25
S1007,U1007,Web,74,Black/African,Pass,2025-04-21 12:20:25
S1008,U1008,iOS,25,Asian,Pass,2025-04-21 12:15:25
S1009,U1009,Web,71,White/Caucasian,Pass,2025-04-21 12:36:25
S1010,U1010,Web,70,White/Caucasian,Drop_off,2025-04-21 12:30:25
S1011,U1011,Android,30,Asian,Drop_off,2025-04-21 12:10:25
S1012,U1012,Android,68,Black/African,Pass,2025-04-21 11:57:25
S1013,U1013,Web,67,White/Caucasian,Drop_off,2025-04-21 11:43:25
S1014,U1014,iOS,61,White/Caucasian,Fail_FR,2025-04-21 12:01:25
S1015,U1015,Android,33,Black/African,Drop_off,2025-04-21 12:25:25
S1016,U1016,Web,66,Black/African,Fail_FR,2025-04-21 11:46:25
S1017,U1017,Android,51,White/Caucasian,Pass,2025-04-21 12:20:25
S1018,U1018,Android,72,Black/African,Pass,2025-04-21 12:19:25
S1019,U1019,Android,59,Asian,Fail_FR,2025-04-21 12:00:25
S1020,U1020,Android,69,Hispanic/Latino,Pass,2025-04-21 12:26:25
S1021,U1021,iOS,38,Hispanic/Latino,Fail_FR,2025-04-21 12:26:25
S1022,U1022,iOS,58,Black/African,Pass,2025-04-21 12:30:25
S1023,U1023,Web,42,Hispanic/Latino,Pass,2025-04-21 12:28:25
S1024,U1024,Web,40,Hispanic/Latino,Drop_off,2025-04-21 12:02:25
S1025,U1025,iOS,62,Hispanic/Latino,Drop_off,2025-04-21 11:39:25
S1026,U1026,iOS,56,Asian,Fail_FR,2025-04-21 11:48:25
S1027,U1027,iOS,50,Asian,Fail_FR,2025-04-21 11:54:25
S1028,U1028,iOS,51,Hispanic/Latino,Fail_FR,2025-04-21 12:32:25
S1029,U1029,Web,35,Asian,Drop_off,2025-04-21 11:46:25
S1030,U1030,Android,59,White/Caucasian,Pass,2025-04-21 11:56:25
S1031,U1031,Android,18,Black/African,Fail_FR,2025-04-21 12:06:25
S1032,U1032,Android,50,Hispanic/Latino,Pass,2025-04-21 12:01:25
S1033,U1033,iOS,54,Hispanic/Latino,Drop_off,2025-04-21 12:36:25
S1034,U1034,Android,68,Black/African,Fail_FR,2025-04-21 12:15:25
S1035,U1035,Android,66,White/Caucasian,Drop_off,2025-04-21 12:34:25
S1036,U1036,Android,50,Asian,Drop_off,2025-04-21 12:27:25
S1037,U1037,Android,40,Black/African,Pass,2025-04-21 12:07:25
S1038,U1038,Web,69,Black/African,Pass,2025-04-21 12:11:25
S1039,U1039,Android,28,Black/African,Pass,2025-04-21 12:25:25
S1040,U1040,Android,19,Asian,Drop_off,2025-04-21 12:10:25
S1041,U1041,iOS,38,Hispanic/Latino,Drop_off,2025-04-21 12:06:25
S1042,U1042,Android,59,Hispanic/Latino,Pass,2025-04-21 12:35:25
S1043,U1043,Android,45,White/Caucasian,Fail_FR,2025-04-21 11:53:25
S1044,U1044,Web,29,Hispanic/Latino,Pass,2025-04-21 12:13:25
S1045,U1045,Web,37,Black/African,Drop_off,2025-04-21 12:15:25
S1046,U1046,Web,70,White/Caucasian,Drop_off,2025-04-21 12:00:25
S1047,U1047,Android,58,Asian,Drop_off,2025-04-21 11:58:25
S1048,U1048,iOS,34,Asian,Fail_FR,2025-04-21 11:39:25
S1049,U1049,iOS,55,Hispanic/Latino,Pass,2025-04-21 11:42:25
S1050,U1050,Web,46,Hispanic/Latino,Pass,2025-04-21 12:30:25
S1051,U1051,iOS,26,Asian,Drop_off,2025-04-21 11:50:25
S1052,U1052,Android,42,Black/African,Pass,2025-04-21 12:08:25
S1053,U1053,Web,59,Hispanic/Latino,Fail_FR,2025-04-21 12:11:25
S1054,U1054,Web,43,Hispanic/Latino,Pass,2025-04-21 11:54:25
S1055,U1055,iOS,22,Black/African,Fail_FR,2025-04-21 11:38:25
S1056,U1056,Web,53,Hispanic/Latino,Drop_off,2025-04-21 12:12:25
S1057,U1057,iOS,32,Hispanic/Latino,Pass,2025-04-21 11:55:25
S1058,U1058,Android,24,White/Caucasian,Pass,2025-04-21 12:15:25
S1059,U1059,iOS,65,Black/African,Drop_off,2025-04-21 12:01:25
S1060,U1060,Android,30,White/Caucasian,Drop_off,2025-04-21 12:33:25
S1061,U1061,iOS,69,Hispanic/Latino,Pass,2025-04-21 11:53:25
S1062,U1062,Android,69,Asian,Drop_off,2025-04-21 12:07:25
S1063,U1063,iOS,60,Hispanic/Latino,Fail_FR,2025-04-21 12:17:25
S1064,U1064,iOS,26,White/Caucasian,Drop_off,2025-04-21 11:58:25
S1065,U1065,Web,69,White/Caucasian,Drop_off,2025-04-21 11:44:25
S1066,U1066,Android,48,Asian,Pass,2025-04-21 12:31:25
S1067,U1067,Web,37,Hispanic/Latino,Fail_FR,2025-04-21 11:51:25
S1068,U1068,Android,33,White/Caucasian,Drop_off,2025-04-21 12:07:25
S1069,U1069,Android,49,Hispanic/Latino,Fail_FR,2025-04-21 12:32:25
S1070,U1070,Android,51,White/Caucasian,Pass,2025-04-21 12:00:25
S1071,U1071,Web,30,Black/African,Pass,2025-04-21 12:03:25
S1072,U1072,Web,37,White/Caucasian,Pass,2025-04-21 11:53:25
S1073,U1073,iOS,75,Asian,Drop_off,2025-04-21 11:57:25
S1074,U1074,Web,20,Black/African,Fail_FR,2025-04-21 11:59:25
S1075,U1075,iOS,31,Hispanic/Latino,Pass,2025-04-21 12:29:25
S1076,U1076,Android,44,White/Caucasian,Drop_off,2025-04-21 12:28:25
S1077,U1077,iOS,61,Asian,Drop_off,2025-04-21 12:22:25
S1078,U1078,iOS,28,Hispanic/Latino,Pass,2025-04-21 11:39:25
S1079,U1079,Web,25,Asian,Fail_FR,2025-04-21 11:52:25
S1080,U1080,Android,50,Asian,Drop_off,2025-04-21 12:14:25
S1081,U1081,Web,27,Hispanic/Latino,Fail_FR,2025-04-21 12:15:25
S1082,U1082,Web,71,White/Caucasian,Drop_off,2025-04-21 12:14:25
S1083,U1083,Android,60,Hispanic/Latino,Fail_FR,2025-04-21 11:58:25
S1084,U1084,Android,65,Black/African,Drop_off,2025-04-21 11:53:25
S1085,U1085,Android,20,Asian,Fail_FR,2025-04-21 12:05:25
S1086,U1086,Android,62,White/Caucasian,Fail_FR,2025-04-21 11:42:25
S1087,U1087,Web,31,Black/African,Pass,2025-04-21 11:39:25
S1088,U1088,Android,24,Hispanic/Latino,Drop_off,2025-04-21 11:51:25
S1089,U1089,Android,44,Black/African,Pass,2025-04-21 12:20:25
S1090,U1090,Android,55,White/Caucasian,Pass,2025-04-21 11:39:25
S1091,U1091,Android,19,Hispanic/Latino,Fail_FR,2025-04-21 12:22:25
S1092,U1092,iOS,71,Black/African,Fail_FR,2025-04-21 12:28:25
S1093,U1093,Android,54,Black/African,Pass,2025-04-21 12:30:25
S1094,U1094,iOS,44,Asian,Fail_FR,2025-04-21 12:25:25
S1095,U1095,iOS,35,Black/African,Fail_FR,2025-04-21 12:10:25
S1096,U1096,Android,25,Asian,Pass,2025-04-21 11:45:25
S1097,U1097,iOS,64,White/Caucasian,Fail_FR,2025-04-21 12:34:25
S1098,U1098,Web,32,Hispanic/Latino,Fail_FR,2025-04-21 11:58:25
S1099,U1099,Android,64,Asian,Fail_FR,2025-04-21 11:52:25


