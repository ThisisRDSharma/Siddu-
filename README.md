RAG Status	AUC Range	Action Plan	Escalation
🟢 Green	≥ 0.80	- Standard monitoring during each cycle
- Quarterly validation and drift tracking	No escalation
🟠 Amber	0.70 – 0.80	- Monthly review (or each cycle)
- Fine-tune parameters and reassess features
- Monitor performance over consecutive cycles (e.g., 2 cycles)	Notify Risk & Model Governance if Amber persists for 2 consecutive cycles
🔴 Red	< 0.70	- Immediate full model audit
- Deploy backup model and retrain with fresh data
- Perform root cause analysis	Escalate immediately to Senior Risk, Compliance & Regulatory Teams

RAG Status	KS Range	Action Plan	Escalation
🟢 Green	≥ 0.40	- Standard monitoring and quarterly validation
- Ongoing tracking for any drift	No escalation
🟠 Amber	0.25 – 0.40	- Monthly review (or each cycle)
- Reassess feature effectiveness and adjust decision thresholds
- Monitor performance over consecutive cycles	Notify Risk & Model Governance if Amber persists for 2 consecutive cycles
🔴 Red	< 0.25	- Immediate full audit and root cause analysis
- Retrain model with updated data
- Consider temporary model override	Escalate immediately to Senior Risk, Compliance & Regulatory Teams


RAG Status	PSI Range	Action Plan	Escalation
🟢 Green	< 0.10	- Standard monitoring during each cycle
- Regularly track population stability	No escalation
🟠 Amber	0.10 – 0.20	- Monthly review (or each cycle)
- Investigate potential data drift and feature distribution shifts
- Prepare for retraining if drift continues over cycles	Notify Risk & Model Governance if Amber persists for 2 consecutive cycles
🔴 Red	> 0.20	- Immediate root cause analysis of data distribution changes
- Urgent retraining of the model
- Assess business impact of data drift	Escalate immediately to Senior Risk, Compliance & Regulatory Teams
