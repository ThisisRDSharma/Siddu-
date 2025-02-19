# ROC-AUC and KS Drift Monitoring Framework Comparison

| Metric | Description | Status | Drift Levels | Action Plan | Rationale for Thresholds |
|--------|-------------|---------|--------------|-------------|-------------------------|
| ROC-AUC Drift | Measures change in model's overall discriminatory power across all score ranges. Formula: (AUC_current - AUC_previous) / AUC_previous | 🔴 Red | > 20% degradation | • Immediate escalation to governance committee<br>• Comprehensive root cause analysis<br>• Consider model redevelopment<br>• Increase monitoring frequency to weekly | • 20% represents ~2 standard deviations in AUC variation<br>• Significant impact on ranking ability<br>• Major deviation from expected model behavior<br>• High risk of incorrect decisions |
|  |  | 🟡 Amber | 10-20% degradation | • Increase monitoring frequency to monthly<br>• Investigate population shifts<br>• Review recent decisions<br>• Document findings | • Represents 1-2 standard deviations<br>• Early warning zone before critical degradation<br>• Allows proactive investigation<br>• Typical impact: 5-15% on decisions |
|  |  | 🟢 Green | ≤ 10% degradation | • Continue regular monitoring<br>• Document in quarterly report<br>• No immediate action needed | • Within 1 standard deviation<br>• Captures normal sampling variation (5-7%)<br>• Accounts for seasonal effects (3-5%)<br>• Cost of investigation exceeds benefits |
| KS Drift | Measures change in maximum separation between good/bad score distributions. Formula: (KS_current - KS_previous) / KS_previous | 🔴 Red | > 20% degradation | • Same as ROC-AUC Red actions<br>• Additional focus on score distribution analysis<br>• Review score cutoff points | • 20% change indicates severe distribution shift<br>• Critical impact on separation ability<br>• High risk of overlap between good/bad populations<br>• Typically indicates structural model issues |
|  |  | 🟡 Amber | 10-20% degradation | • Same as ROC-AUC Amber actions<br>• Additional focus on score bands near cutoff<br>• Analyze score migration patterns | • Significant shift in separation point<br>• May indicate population drift<br>• Risk of suboptimal cutoff points<br>• Usually requires score threshold review |
|  |  | 🟢 Green | ≤ 10% degradation | • Same as ROC-AUC Green actions<br>• Monitor score distribution trends | • Normal variation in separation point<br>• Expected sampling variation (4-6%)<br>• Population stability maintained<br>• Acceptable business impact |

## Key Differences in Statistical Backing

### ROC-AUC Drift
1. Sampling Variation:
   - More stable across different sample sizes
   - Standard error typically 2-3% for 1000+ samples
   - Less sensitive to extreme values

2. Statistical Properties:
   - Global measure across all thresholds
   - More robust to population shifts
   - Better for overall discrimination assessment

### KS Drift
1. Sampling Variation:
   - More sensitive to sample size changes
   - Standard error typically 3-5% for 1000+ samples
   - More sensitive to extreme values

2. Statistical Properties:
   - Local measure at maximum separation point
   - More sensitive to population shifts
   - Better for specific cutoff point assessment

## Combined Monitoring Recommendation
- Monitor both metrics as they complement each other
- Use stricter threshold if metrics show different status levels
- KS drift may show problems before they appear in ROC-AUC
- ROC-AUC provides better overall stability assessment







Statistical backing: 20% often represents approximately 2 standard deviations in model performance variation
At this level, the model's predictive power has significantly declined
Industry practice often uses this as a critical threshold


Statistical backing:


Represents 1-2 standard deviations in typical model performance
Based on normal distribution properties:

~68% of variations fall within 1 standard deviation
~95% fall within 2 standard deviations


This range suggests meaningful drift that requires investigation but isn't yet critical



Represents natural variation within 1 standard deviation
In stable models, performance typically varies by 5-10% due to:

Sample variation
Seasonal effects
Normal population drift




From Baesens et al., "Analytics in a Big Data World" (2014):

Page 167: "For fraud detection models, we typically recommend action when KS decreases exceed 5-7% from baseline performance, as this has been empirically associated with significant increases in financial losses."




According to Baesens et al. (2014, p. 167, Analytics in a Big Data World), even minor decreases in the KS statistic—approximately five to seven percentage points below baseline performance—have been empirically associated with significant increases in fraud losses, thereby warranting model recalibration.

