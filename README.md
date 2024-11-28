# Siddu-
The data sources used for model development in iProov’s system can be summarized as follows:
Digital Banking Onboarding Data
This data comes from customers who onboarded through the digital banking platform. As of March 31, 2024, there were 49,103 customers with active accounts who were digitally onboarded, specifically for consumer deposit accounts. This data serves as the foundation for the initial customer verification process and transaction monitoring.

Alerts Data
Alerts data is collected from the system to monitor the performance of the iProov technology and ensure reliable operation. This data helps identify any issues with the technology, such as downtime or service availability problems, and is critical for maintaining the overall functionality and security of the system. Importantly, this data does not include any personal or identifiable information (PII) about individual users.

Transaction Metadata
Metadata is captured during the processing of transactions. This data is non-personal and non-sensitive, and it is used solely to monitor and improve the performance of the iProov technology. Transaction metadata includes details like transaction timing, system responsiveness, and performance across different devices, without linking back to individual users.

Imagery Data
Imagery data is used primarily for active threat management. Facial images captured during user authentication (e.g., via biometric verification) are processed to identify potential security threats. In most cases, imagery data is not accessed unless a transaction is flagged as suspicious by the iProov Security Operations Centre (SOC). When flagged, the images are manually reviewed, and if deemed part of a novel or advanced attack, they are escalated for further analysis. This data is used to continuously improve the system’s ability to detect fraudulent or suspicious activity and respond to emerging biometric threats.
