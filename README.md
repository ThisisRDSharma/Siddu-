"To ensure the representativeness of the dataset used for modeling, multiple frequency tests were conducted. These tests validated that the distributions of key variables in the selected dataset closely aligned with those of the national pool of consumer demand deposit applicants. Although specific details of the distributions are not available

Data Quality Dependency

Limitation Description
The model quality is dependent on the accuracy of the data provided during development. For example, the model relies on client-provided data about forced DDA account closures. If clients provide inaccurate information, such as including non-DDA account closures or misclassifying forced closures, the data used may not accurately represent the intended population.

Impact on Business Use
Inaccurate data could lead to biased model outputs, resulting in incorrect risk assessments or suboptimal business decisions, such as improper classifications of accounts for closures or inappropriate predictions for forced closures.

Modeling Description
The model is specifically developed based on forced DDA account closures as provided by clients. Data quality monitoring processes are in place to assess the accuracy of the inputs and flag any inconsistencies or deviations over time.

Frequency
Ongoing data quality monitoring occurs at regular intervals to evaluate the consistency and accuracy of client-provided data and ensure alignment with model requirements

Performance Monitoring Plan Details
Source of Data Used in the Performance Monitoring Process:

The inquiry data provided by clients will be utilized as the primary source for performance monitoring. This data will be subject to periodic checks for completeness and accuracy.
Model Input Data Quality:

A sample of at least 100,000 randomly selected records will be reviewed to ensure the robustness and representativeness of the input data.
Data Period Monitored:

The model’s performance will be subject to periodic review, with monitoring intervals set at monthly or quarterly, based on the model’s risk profile and operational requirements.
Monitoring Frequency:

The monitoring will be conducted on a monthly or quarterly basis, ensuring continuous oversight of model performance and addressing any significant deviations.
Test Methodology:

The Population Stability Index (PSI) will be employed to assess the stability of scores and variables over time. PSI will identify shifts in the underlying population characteristics, indicating whether the model’s assumptions remain valid.
The Kolmogorov-Smirnov (KS) statistic will be utilized to evaluate the model's ability to distinguish between good and bad outcomes. The KS statistic will provide insight into the model's discriminatory power.
The Area Under the Curve (AUC) will be measured to assess the model’s discriminatory performance between positive and negative classes. A higher AUC indicates superior model performance in classifying outcomes correctly.
Test Metrics and Thresholds for Monitoring:

Population Stability Index (PSI):

PSI < 0.1: No significant changes in the population distribution (model stability is within acceptable limits).
PSI between 0.1 and 0.2: Minor changes detected, warranting closer monitoring and further investigation to ensure continued model stability.
PSI > 0.2: Significant shift in population distribution, suggesting a material change that could affect model performance. Immediate review and potential model adjustments may be required.
Kolmogorov-Smirnov (KS) Statistic:

KS ≥ 40%: Indicates excellent discriminatory power, with the model effectively distinguishing between the classes.
KS between 30% and 40%: The model demonstrates good discriminatory performance, but further improvements may be necessary.
KS between 20% and 30%: The model’s discriminatory power is fair, requiring attention and potential re-calibration to ensure better class separation.
KS < 20%: Poor discriminatory performance, suggesting that the model fails to effectively distinguish between the classes. Immediate corrective actions are required.
Area Under the Curve (AUC):

AUC ≥ 0.9: Exceptional model performance with robust ability to discriminate between classes.
AUC between 0.8 and 0.9: Good performance, indicating that the model is adequately discriminating between positive and negative outcomes.
AUC between 0.7 and 0.8: Fair model performance, requiring improvements to meet acceptable standards.
AUC < 0.7: Poor model performance with inadequate discriminatory power, necessitating a re-evaluation or re-development of the model.
Re-evaluation of the Performance Thresholds:

The performance thresholds for PSI, KS, and AUC will be subject to regular review to ensure they remain appropriate in light of evolving business requirements, regulatory expectations, or significant shifts in the data. Thresholds may be adjusted periodically, but any changes will be made in compliance with regulatory guidelines and after proper validation.
This version uses more formal and regulatory language, appropriate for MDR documentation. Let me know if any further adjustments are needed!









Performance Monitoring Thresholds
Metric	Excellent Performance	Good Performance	Fair Performance	Poor Performance
Population Stability Index (PSI)	PSI < 0.1: No significant changes in population (model stability is acceptable)	PSI 0.1 - 0.2: Minor changes in population (monitor and investigate as needed)	PSI > 0.2: Significant change in population (review and adjust model)	-
Kolmogorov-Smirnov (KS) Statistic	KS ≥ 40%: Excellent model discrimination (high discriminatory power)	KS 30% - 40%: Good model discrimination (acceptable separation)	KS 20% - 30%: Fair model discrimination (requires improvement)	KS < 20%: Poor model discrimination (needs significant adjustments)
Area Under the Curve (AUC)	AUC ≥ 0.9: Excellent performance (high discriminatory ability)	AUC 0.8 - 0.9: Good performance (adequate discrimination)	AUC 0.7 - 0.8: Fair performance (needs improvements)	AUC < 0.7: Poor performance (significant issues with model discrimination)

