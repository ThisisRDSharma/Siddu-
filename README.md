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







