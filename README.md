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
