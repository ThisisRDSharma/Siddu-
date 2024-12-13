1. Objective

The purpose of this performance monitoring plan is to evaluate the fairness and effectiveness of the biometric system by ensuring it does not exhibit significant bias toward any demographic group, including age, gender, or ethnicity. This evaluation will involve analyzing pass rates and their variation across different demographic groups over specific time periods, based on systematically collected data.

2. Reporting Schedule

Four performance reports will be generated annually:

First Customer Report (Q2 Data): Covers data from April, May, and June 2024.

Second Customer Report (Q4 Data): Covers data from October, November, and December 2024.

Additional Reports:

Q1 Data Report: Covers data from January, February, and March 2024.

Q3 Data Report: Covers data from July, August, and September 2024.

Each report will offer detailed insights into the system's performance during its respective quarter.

3. Data Collection

Time Periods: Data collection for each report corresponds to the respective quarter.

Sampling Strategy:

Equal representation for each demographic group (age, gender, ethnicity) will be ensured where feasible.

Samples may originate from any biometric device, with preference for commonly used devices when practical.

The sampling approach aims to ensure adequate coverage across all demographic groups for reliable comparisons.

4. Metrics

The following metrics will be calculated for each demographic group:

Pass Rate: The percentage of successful authentications.

95% Confidence Intervals: To account for statistical variability and ensure reliability of the metrics.

Metrics will be reported as follows:

Quarterly Aggregate Metrics: Aggregated across all three months of the quarter. Pass rates will be represented as data points, with confidence intervals displayed as error bars in a "Quarterly Aggregate Figure."

Transformed Y-Axis: For ease of interpretation, the y-axis is transformed. The horizontal line at y=0 represents the mean pass rate for the entire dataset, with the points/circles and confidence intervals in the figure showing the percentage difference from this mean.

Monthly Metrics: Metrics will also be calculated for each month individually to observe variations in performance over time.





5. Data Analysis

Quarterly and Monthly Insights: Examine metrics to identify any significant changes over time, focusing on trends in pass rates across different demographic groups.

Group Comparisons: Evaluate performance across demographic groups (age, gender, ethnicity) to detect potential biases or disparities.

Fairness Validation: Ensure no demographic group is disproportionately impacted by analyzing pass rates and their confidence intervals. The goal is to verify that the system operates equitably across all groups.



Dynamic Authentication(Ios only)
A small performance discrepancy has been observed in the 18-30 age group for dynamic authentication on both iOS and Android devices. This discrepancy was not present in previous monitoring periods. The difference appears to be due to an increased number of users in this age group attempting authentication in bright sunlight conditions, which tends to lower the success rate. This environmental factor seems to be influencing performance for this specific demographic.

Dynamic Authentication (Web Only)
For the 60+ age group on web authentication, the pass rate confidence intervals do not overlap with any of the other age groups, indicating a notable difference in performance. Since normalization by device manufacturer is not possible for web authentication, variations in device quality—if correlated with demographics—could affect performance. The slightly reduced performance for this age group may be linked to the diversity of device types and quality used within this group. This effect was not observed in previous reports, but it is important to note that this is the first report where performance by age has been further differentiated by platform.

Dynamic Authentication (Android Only):
Although the pass rate differences between ethnicities for Android devices are not large, the confidence intervals show relatively small or no overlap at all. This could be due to significant differences in the distribution of phone models used across different regions, even though the sampling was restricted to the most prevalent Android manufacturers. These regional variations in device models may be contributing to the observed performance differences.




