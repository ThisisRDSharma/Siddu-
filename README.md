
Escalation Measures by PSI (Population Stability Index) RAG Status
RAG Status	PSI Range	Review Frequency	Actions	Escalation Level
=�â� Green	< 0.10	Quarterly	Standard monitoring, track for data drift	No escalation
=�à� Amber	0.10 – 0.20	Monthly	Investigate data drift, assess feature shifts, retrain if needed	Notify Risk & Model Governance if persists >2 cycles
=�4� Red	> 0.20	Bi-Weekly	Immediate root cause analysis, retrain model, assess business impact	Escalate to Senior Risk, Compliance & Regulatory


Escalation Measures by RAG Status
RAG Status	Review Frequency	Actions	Escalation Level
=�â� Green (AUC ≥ 0.80, KS ≥ 0.40)	Quarterly	Standard monitoring, track for data drift	No escalation
=�à� Amber (AUC 0.70–0.80, KS 0.25–0.40)	Monthly	Fine-tune model, check data quality, retrain if needed	Notify Risk & Model Governance if persists >2 cycles
=�4� Red (AUC < 0.70, KS < 0.25)	Bi-Weekly	Immediate audit, temporary override, deploy backup model, retrain	Escalate to Senior Risk, Compliance & Regulatory


ܽ�翢� Green (AUC ≥ 0.80)	Standard quarterly validation, monitor for data drift	No escalation
༽�࿠� Amber (AUC 0.70 – 0.80)	Monthly review, check for model degradation, fine-tune parameters, reassess features	Notify Risk & Model Governance if persists for 2+ cycles
༽�༴� Red (AUC < 0.70)	Immediate model audit, deploy backup model, retrain with fresh data	Escalate to Senior Risk, Compliance & Regulatory Teams
KS Action Plan:
KS Status	Action Plan	Escalation
༽�࿢� Green (KS ≥ 0.40)	Standard monitoring, quarterly validation, track for model drift	No escalation
ွ�რ� Amber (KS 0.25 – 0.40)	Monthly review, reassess features, tune model thresholds, improve data quality	Notify Risk & Model Governance if persists for 2+ cycles
༽�༴� Red (KS < 0.25)	Immediate full audit, root cause analysis, retrain model	Escalate to Senior Risk, Compliance & Regu****

