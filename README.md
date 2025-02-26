The Bridger Insight system is designed to ensure compliance with key regulatory frameworks governing financial institutions. It aligns with the following regulatory and compliance requirements:

1. USA PATRIOT Act Compliance
Bridger Insight facilitates adherence to the USA PATRIOT Act by enabling a Customer Identification Program (CIP) and Know Your Customer (KYC) processes. The system verifies customer identities, assesses risk levels, and helps prevent illicit financial activities, including money laundering and terrorism financing.

2. OFAC (Office of Foreign Assets Control) Compliance
Bridger Insight supports compliance with OFAC regulations by performing sanctions screening against OFAC's watchlists, including the Specially Designated Nationals (SDN) list. This ensures that transactions do not involve sanctioned entities or individuals, reducing financial and legal risks.

3. Bank Secrecy Act (BSA) and KYC Requirements
The system enhances BSA/AML (Anti-Money Laundering) compliance through:

Automated risk assessments and transaction monitoring.
Screening and flagging of potentially suspicious activities.
Support for regulatory reporting obligations, including Suspicious Activity Reports (SARs) and Currency Transaction Reports (CTRs).
Monitoring Qualifile Model Data Limitations



S
I have included a data limitation for a Qualifile model that 
Data is only approved for dda origination cannot be used for any other purpose other than that 

Soni have to include a monitoring description & frequency of the same 
So it's been provided by the bank
Quarterly cadence and annual artifacts of mrm validation and scorecard will work .
But there is one confusion 
It's that model limitation is of development side

Edit
Let me help clarify this monitoring description for your Qualifile model.

Based on your information, I understand that:

You have a data limitation specifying that the data can only be used for DDA origination
You need to include a monitoring description and frequency
The bank has specified quarterly cadence and annual MRM validation and scorecard
You're confused because the model limitation relates to the development side
This sounds like a typical model risk management framework for banking models. Here's my suggestion for resolving your confusion:

Even though the data limitation is on the development side, it's still important to monitor this in production to ensure the model isn't being used outside its approved scope. The quarterly monitoring cadence would allow you to verify that:

The model is only being used for DDA origination purposes
The data inputs remain consistent with what was used during development
Any drift in model performance is identified early
The annual MRM validation and scorecard would provide a more comprehensive review to confirm long-term compliance with the data limitation.

Would it help if I drafted some specific monitoring language to include in your documentation that addresses this development-side limitation while fitting with the quarterly/annual cadence requirement?




Retry
S
Yes a precise one which is safe to include

Edit
Here's a precise monitoring description you can safely include:

"Model Monitoring Description: This Qualifile model will be subject to quarterly monitoring to ensure compliance with data usage limitations. Monitoring will verify that model utilization remains restricted to DDA origination purposes only, as specified in the development constraints. Key performance indicators and usage metrics will be reviewed quarterly to detect any unauthorized applications or data drift. Annual Model Risk Management (MRM) validation and comprehensive scorecard reviews will be conducted to provide thorough assessment of the model's adherence to its approved scope and data limitations. All monitoring outcomes will be documented and reported to relevant stakeholders according to established governance protocols."

This language establishes clear monitoring frequency, specifies what will be monitored, aligns with your quarterly and annual cadence requirements, and acknowledges the development-side limitation while making it part of the ongoing monitoring process.




Retry
S
The quarterly monitoring cadence would allow you to verify that:

The model is only being used for DDA origination purposes
The data inputs remain consistent with what was used during development
Any drift in model performance is identified early

The annual MRM validation and scorecard would provide a more comprehensive review to confirm long-term compliance with the data limitation

Rewrite it more explanatory as I have to include into 
Monitoring description & frequency (of model limitation) section

Edit
Here's a more explanatory version for your "Monitoring Description & Frequency (of Model Limitation)" section:

"Monitoring Description & Frequency (of Model Limitation):

This Qualifile model will be monitored through a structured approach to ensure strict adherence to its critical data limitation - that data is only approved for DDA origination and cannot be used for any other purpose.

Quarterly Monitoring:

Usage Assessment: Comprehensive review of all model applications to verify the model is exclusively used for DDA origination purposes as stipulated in the development parameters.
Data Input Verification: Examination of data sources and inputs to confirm consistency with the development dataset, ensuring no unauthorized data expansion.
Performance Drift Analysis: Evaluation of key performance metrics to identify any deviations that might indicate use outside approved boundaries.
Documentation of findings in quarterly reports with remediation plans for any identified issues.
Annual Monitoring:

Full Model Risk Management (MRM) validation will be conducted to thoroughly assess the model's compliance with its approved scope.
Comprehensive scorecard review will provide in-depth analysis of the model's performance and usage patterns throughout the year.
Annual certification process will formally document adherence to the data limitation requirement.
Results will be presented to appropriate governance committees for oversight and approval.
Any detected non-compliance with the model limitation will trigger immediate notification to model stakeholders and implementation of corrective actions following established governance protocols."




Retry
S
Quarterly cadence means quarterly meeting with vendor

Edit
I understand the clarification now. Let me revise the monitoring description to specifically reflect that quarterly cadence refers to meetings with the vendor:

"Monitoring Description & Frequency (of Model Limitation):

This Qualifile model will be monitored through a structured approach to ensure strict adherence to its critical data limitation - that data is only approved for DDA origination and cannot be used for any other purpose.

Quarterly Monitoring:

Quarterly meetings with the vendor will be conducted to review and verify: • Usage Assessment: Confirmation that the model is exclusively used for DDA origination purposes as stipulated in the development parameters. • Data Input Verification: Examination of data sources and inputs to confirm consistency with the development dataset, ensuring no unauthorized data expansion. • Performance Drift Analysis: Evaluation of key performance metrics to identify any deviations that might indicate use outside approved boundaries.
Documentation of findings from vendor meetings in quarterly reports with remediation plans for any identified issues.
Annual Monitoring:

Full Model Risk Management (MRM) validation will be conducted to thoroughly assess the model's compliance with its approved scope.
Comprehensive scorecard review will provide in-depth analysis of the model's performance and usage patterns throughout the year.
Annual certification process will formally document adherence to the data limitation requirement.
Results will be presented to appropriate governance committees for oversight and approval.
