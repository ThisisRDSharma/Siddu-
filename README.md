# Siddu-
iProov utilizes three core types of data—alerts, metadata, and imagery—to support the development, monitoring, and continuous improvement of its technology. These data types are critical for ensuring high-performance, security, and the ongoing enhancement of iProov’s systems throughout the lifecycle of each customer contract.
1. Alerts Data
Alerts data is essential for monitoring and evaluating the real-time performance of iProov’s technology. These alerts provide insights into the system’s health, including any downtime or issues affecting service availability. This data is crucial for ensuring the smooth operation of the system and is used to identify and resolve potential issues swiftly. Importantly, this data does not include any personal or PII (personally identifiable information) related to individual users but is focused solely on system performance.

2. Metadata
Metadata refers to non-personal, non-sensitive data collected during the transaction process. This data plays a key role in the performance monitoring and optimization of iProov’s technology. It provides critical insights into system performance metrics, such as transaction timing, device responsiveness, and performance across different handsets. This data enables iProov to continuously improve the technology, ensuring optimal performance without any association to personal data or identifiable users. The metadata is used purely for operational efficiency and technology enhancement.

3. Imagery
Imagery data is primarily accessed when a transaction is flagged as suspicious by iProov’s Security Operations Centre (SOC). While most transactions are processed without the need to access imagery or personal data, flagged transactions undergo detailed analysis. If the transaction is determined to be part of a potential biometric threat or attack, the imagery is escalated for further investigation.

If the imagery is deemed to be part of a novel attack or advanced biometric threat, it is marked as high-risk and reviewed by iProov’s Research Group for further analysis. This scenario is extremely rare, accounting for about 0.05% of all transactions.
All imagery access is strictly auditable and controlled to maintain privacy and security standards.
The system is designed to evolve with emerging threats, and any new attack patterns identified through imagery are stored and analyzed to enhance iProov’s defenses.
Data Flow and Sources for Model Development
The data leveraged for model development flows from multiple sources, which include:

Digital Banking Onboarding: Customer data obtained during the onboarding process is integrated into iProov’s system for initial account activation and transaction monitoring.
Real-time Alerts: These alerts are generated from iProov’s ongoing operations, providing insights into system performance and potential security threats.
Transaction Metadata: Continuously collected during transactions, this metadata is essential for optimizing system performance and technology development.
Imagery Data: Only accessed when a transaction is flagged as suspicious, enabling iProov to perform detailed analysis of potential threats.

