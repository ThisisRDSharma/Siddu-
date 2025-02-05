
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

