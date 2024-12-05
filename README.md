# Siddu-
so play a role in ensuring accurate verification. These variables work together to assess the genuine presence of a live user and mitigate identity fraud by analyzing dynamic facial behavior and contextual data in real-time.
Explanatory variables, also known as independent variables or features, are the factors or inputs that a model uses to explain or predict an outcome. In the context of machine learning or biometric verification, explanatory variables are the data points or characteristics that help the system make decisions about whether an authentication attempt is genuine or fraudulent.These variables can be anything from biometric features (e.g., facial landmarks) to contextual data (e.g., device information or session history).In the case of iProov’s face biometric verification system, the explanatory variables include a variety of factors that contribute to determining whether the user is a genuine human or an attempt at spoofing

Facial Behavior: This includes key features like eye movement, blink patterns, and head pose, all of which help assess the liveliness of the user. These behaviors are natural and dynamic, allowing the system to distinguish a real person from static images or videos.

Color Reflection Data: During the authentication process, the system illuminates the face with a sequence of colors. The reflection of light from the skin during this process is an important explanatory variable. The way light reflects from the user's skin confirms liveliness and ensures the presence of a real human, not a spoofed attempt using a photo or video.

Contextual Information: This includes details like device metadata (e.g., device type, operating system) and session history, which provide additional layers of context around the authentication attempt, helping to verify the legitimacy of the session.
The response variable in iProov's model is the alert system that indicates the performance and outcome of the biometric verification process.
he response variable in iProov's model is the alert system that indicates the performance and outcome of the biometric verification process. 
the two main types of explanatory variables for your iProov model are metadata and imagery, 
Metadata refers to the contextual information surrounding the authentication attempt. This data helps assess the authenticity of the session and provides insights into the environment in which the verification is taking place.
Imagery refers to the visual data captured during the authentication process, primarily focusing on the face of the user. This visual data provides key biometric features that are essential for identifying and verifying the user.
For the months of April, May, and June 2024, data was collected for each relevant breakdown where possible. The goal was to ensure that the data was comprehensive and representative across demographic groups and devices. The following steps were undertaken as part of the reconciliation process:

Device Selection:

For each breakdown, the most common devices across the three months were selected. This ensured that the data was consistent and aligned with the devices most frequently used.
In cases where the available data was insufficient to limit sampling to only the most common devices, all devices were included, while still maintaining balanced representation across demographic groups.



While specific details on monitoring frequency are not available, continuous monitoring is recommended for the Iproov model. This ensures ongoing performance, accuracy, and security, detecting issues such as spoofing attempts or data quality concerns in real time.
Sampling Approach:

The sampling was conducted in such a way that the total number of samples for each demographic group was equal across each device and for each month. This helped mitigate any biases that might arise from over-representation of any particular device or demographic group.
Where the data was sparse and it was not feasible to sample exclusively from a few devices, equal samples from each demographic group were still ensured, even if the samples came from a broader range of devices.
This methodology was aimed at reconciling the data by ensuring that it was representative, balanced, and consistent across devices and demographic groups over the three-month period. The reconciliation process helped ensure that the samples used for analysis were aligned with the expected standards and that the resulting dataset was complete and reliable.
The approval process for Iproov’s biometric solution involves rigorous evaluations and certifications to ensure security, robustness, and compliance with industry standards. Iproov is the first organization to achieve comprehensive certification for remote verification from the FIDO Alliance, confirming the solution's robustness, inclusivity, and interoperability. This certification ensures Iproov’s technology provides unmatched defense against presentation attacks and deepfake threats throughout the entire identity lifecycle.

The dynamic liveliness solution was independently evaluated and confirmed as compliant with ISO 19795 and ISO 30107 standards, validating its excellence in face matching and liveliness detection.

Testing was conducted by the accredited laboratory Ingenium Biometrics, which confirmed the system's ability to thwart all types of presentation attacks, including photo masks, face morphs, videos, and presented deepfakes.

Iproov’s solution has been tested through external evaluations by iBeta, accredited by NIST under the NVLAP program, and internal audits by the National Physical Laboratory, ensuring conformity to ISO 30107:3 standards.
Iproov’s model approval process involves comprehensive evaluations to ensure the highest levels of security, reliability, and compliance with international standards. Iproov is the first organization to achieve comprehensive certification for remote verification from the FIDO Alliance, which assesses the robustness, inclusivity, and interoperability of biometric solutions. This prestigious certification affirms Iproov’s solution’s usability in real-world applications and its unparalleled defense against threats like presentation attacks and presented deepfakes throughout the entire identity verification lifecycle.

The certification follows a rigorous independent evaluation of Iproov’s dynamic liveliness solution, confirming its excellence in face matching and liveliness detection, compliant with ISO 19795 and ISO 30107 standards. The solution has been validated through both external and internal testing. External testing was conducted by iBeta, an accredited laboratory certified by NIST under the NVLAP program. iBeta’s testing procedures for ISO 30107-3 presentation attack detection standards were audited by their accrediting body, and in April 2018, iBeta’s scope of accreditation was extended to include conformance testing to ISO 30107-3. Additionally, Iproov’s internal methodology has been audited by the National Physical Laboratory (NPL), confirming ongoing compliance with ISO 30107:3.

Moreover, Iproov’s solution has been accredited by Ingenium Biometrics, an independent laboratory, validating its resistance to all types of presentation attacks, including photo masks, face morphs, videos, and presented deepfakes. This combination of independent certifications and rigorous testing guarantees that Iproov’s biometric solution provides secure, accurate, and reliable verification, making it a trusted choice for real-world, high-security applications worldwide.
he GBG Scan Testing and Methodology reports discuss the sensitivity tests performed to evaluate how the model behaves under different conditions and assess its performance in varying scenarios.




Limited Data for Detection of Advanced or Novel Biometric Attacks
The data for detecting advanced or novel biometric attacks is extremely limited, as high-risk imagery accounts for just 0.05% of all processed transactions. This scarcity restricts the ability to train models and improve detection mechanisms for sophisticated threats.
 The scarcity of high-risk data makes it challenging to develop highly accurate detection models for advanced or novel biometric attacks



Due to the limited dataset of high-risk biometric incidents, continuous monitoring should focus on real-time detection, alerting for any anomalies or unusual patterns in the biometric data. 
While specific information regarding the frequency of monitoring activities is not available, continuous monitoring is highly recommended for biometric solutions like Iproov’s. Given the dynamic nature of biometric data and the ever-evolving threat landscape, it is crucial to ensure that the system is regularly monitored to maintain its accuracy, security, and reliability.



While specific details on monitoring frequency are not available, continuous monitoring is recommended for the Iproov model. This ensures ongoing performance, accuracy, and security, detecting issues such as spoofing attempts or data quality concerns in real time
There is insufficient information regarding the specific data quality treatments applied by iProov to address missing or erroneous values in the collected data. However, based on the available data types—alerts data, transaction metadata, and imagery data—it can be inferred that iProov likely uses automated validation and system checks to maintain data integrity. Given that the data is primarily used for performance monitoring and security purposes, issues with missing or erroneous values may be minimal, with poor-quality imagery or erroneous metadata likely excluded from analysis. The absence of detailed treatment protocols suggests that iProov’s focus is on ensuring the system’s evolution and security, where data errors may be handled dynamically during processing or excluded without significant impact on system performance.




It is assumed that the raw biometric data (facial images) will meet the required quality standards, including sufficient resolution, proper alignment, and proper lighting conditions. Images should be clear and unambiguous for accurate facial recognition.


The data provided will comply with relevant international standards, including ISO 30107-3 for presentation attack detection and ISO 19795 for biometric data interchange, ensuring the system operates in compliance with best practices and regulatory requirements.

The facial images must be provided in one of the following formats: PNG, JPEG, or JP2. All images should adhere to the ISO/IEC 19794 standard for biometric data interchange formats, ensuring compatibility and consistency in data representation.
Facial images must be provided in PNG, JPEG, or JP2 formats, in compliance with the ISO/IEC 19794 standard for biometric data interchange. This ensures compatibility and consistency in data representation, enabling seamless integration across different systems and devices. 

The assumption is critical because adhering to this standard guarantees that the biometric data is captured in a uniform format, reducing the risk of data misinterpretation and ensuring accurate facial recognition.
By following the standard, the system maintains interoperability, data integrity, and accuracy, all of which are essential for reliable and secure biometric verification.
Model execution monitoring ensures robust performance and reliability throughout deployment. Security tests, including computer vision (CV) and machine learning (ML) techniques, are continuously evaluated and added based on their accuracy and relevance. New models are first deployed in beta mode, where they are tested on larger, unseen datasets for 2–4 weeks. During this phase, the models are monitored weekly, and only those achieving a false rejection rate (FRR) of 2% or less and a false acceptance rate (FAR) of 5% or less are promoted to production. Models that fail these benchmarks are refined or removed. Over time, newer models may replace older ones, with deprecated models clearly identified for transparency. Each model undergoes rigorous certification by the ML team, and its performance is continuously evaluated in production to meet target goals, ensuring accuracy and reliability in tampering detection.

The handoff process involves the following steps:

Generate User Token:

Accuant generates a unique token for each user. This token serves as a secure identifier for the user and is used throughout the verification process.
Enroll ID Document Image:

Accuant captures and processes the image from the user's ID document. This image is associated with the token, ensuring it is linked to the correct user profile. The image is then prepared for comparison in the next steps.
Initiate iProov SDK:

Accuant passes the token to iProov to initiate the identity verification process. This token acts as the key that links the user's identity and the enrolled image for subsequent selfie capture and verification.
Selfie Capture via iProov SDK:

The user is prompted to take a selfie using the iProov SDK. The SDK guides the user to capture their selfie, which is essential for validating the user's presence (liveness detection) and matching the face with the enrolled image.
Face Match and Liveness Validation:

iProov performs the validation by comparing the captured selfie to the enrolled ID image. It checks for liveness to ensure the selfie is from a live user and compares the face match to verify that the user in the selfie is the same person as the one in the ID image.
Return Results to iProov:

The results of the liveness detection and face match are processed within iProov but do not return to Accuant. iProov only processes the selfie and enrolled image and provides feedback, such as whether the selfie is a valid liveness image and whether the faces match.
Completion of Process:

The process ends when iProov has validated the identity based on the selfie and enrolled image, but no results or data are sent back to Accuant. The identity verification is complete on iProov’s side.




Generate User Token:

Accuant generates a unique token for each user. This token serves as a secure identifier throughout the process, ensuring the identity is consistently tied to the right user.
Enroll Image from ID Document:

Accuant captures the image from the user's ID document and enrolls it into the system. The enrolled image is then associated with the generated token, creating a reference image for later comparison during the verification process.
Initiate iProov SDK:

Accuant passes the generated token and enrolled image to iProov, which uses this data to initiate the identity verification process. The token ensures that iProov knows which user's data to work with.
Guide User to Take Selfie:

The user is prompted through the iProov SDK to take a selfie. This is an essential step for liveness detection (confirming the selfie is a live image) and face matching (comparing the selfie to the enrolled image from the ID document).
Face Match and Liveness Validation:

iProov processes the selfie and compares it to the enrolled image from Accuant. The SDK checks whether the selfie is a live image and whether the face matches the enrolled ID image.




Methodology Reports

Explain the model’s workflow, deployment process, and sensitivity tests.
Metrics Reports

Track model performance using metrics like ROC-AUC, FAR, FRR, and precision/recall.
Web Integration Reports

Cover input data requirements, REST APIs, Web SDKs, and tools like GBG Scan for seamless Assure ID integration.
Testing Reports

Document sensitivity, functional, and performance tests for system and model reliability.
Business Continuity Reports

Outline recovery plans, risk assessments, and strategies to maintain critical operations during disruptions.

The GBG Scan Testing and Methodology reports discuss the sensitivity tests performed to evaluate how the model behaves under different conditions and assess its performance in varying scenarios.








