# Siddu-
The document authentication model verifies the authenticity of ID cards, passports, driver’s licenses, and digital identity tokens by analyzing images that include key elements such as barcodes, MRZs, and contactless chips. Input images must meet recommended specifications, including a resolution of at least 600 dpi, a glare score of 50 or greater, and a sharpness grade of 50 or higher. Supported file formats include BMP, PNG, TIFF, JPEG, JPEG XR, JPEG 2000, and HEIC. The model uses a database of over 3,400 document types for verification. Input documents must meet quality standards, with all essential elements clearly visible. Cropping should be minimized, and compression must adhere to established guidelines.

Sensitivity settings—high, normal, or low—control the strictness of authentication. High sensitivity reduces the risk of fraud but may reject more genuine documents, while low sensitivity improves acceptance rates but increases fraud risk. 
Direct Correlation Between Image Quality and Verification Accuracy: The accuracy of iProov’s results is highly dependent on the quality of the ID image provided by Acuant. If Acuant provides a low-quality image—whether due to poor resolution, misalignment, environmental factors, or damage—the resulting image will be unsuitable for iProov’s facial comparison, potentially leading to failed verifications or false rejections.

Failure or Compromise in the Verification Process: Without a clear, well-lit, and properly aligned ID image, the verification process cannot be completed successfully, compromising both the user experience and security. A reasonable image quality from Acuant is essential for iProov to function properly and accurately verify the applicant's identity through the selfie comparison.

Impact on Customer Experience: If Acuant’s ID scanning process results in low-quality images, legitimate users may be unable to complete the onboarding process or may face unnecessary rejections, leading to customer frustration and potential drop-offs from the onboarding flow.
Impact of Acuant Limitations on iProov's Performance
Data Privacy Regulations Compliance:

General Data Protection Regulation (GDPR): iProov complies with EU Regulation 2016/679 on data protection and privacy, ensuring that personal data is processed securely and in compliance with user consent and rights to access, rectification, and deletion.
UK Data Protection Act 2018: iProov adheres to the UK’s Data Protection Act, ensuring personal data is handled in accordance with UK-specific privacy laws, including data retention and security requirements.
Bank Secrecy Act (BSA): iProov is designed to comply with the Bank Secrecy Act (BSA) for anti-money laundering (AML) and know-your-customer (KYC) regulations, which is crucial for financial institutions to maintain accurate records and prevent money laundering.
Industry Standards and Certifications:

National Security Standards: iProov has been tested to meet national security standards by UK Home Office, Singapore Government, Australian Government, and the U.S. Department of Homeland Security, ensuring the model adheres to stringent government-level security and identity verification protocols.
eIDAS (EU Regulation): iProov complies with the eIDAS Regulation (EN 319 401), which governs electronic identification and trust services across the EU. The model also holds Modular Certifications for eSignature to the qualified level and eID Assurance High. Due to annual eIDAS audits, iProov also conforms to AMLD5 Article 24(1)(d) for identity verification in financial services.
ISO/IEC 30107-3: iProov conforms to ISO/IEC 30107-3, which defines standards for biometric liveness detection, ensuring the system is robust against presentation attacks. It has been tested by iBeta to Level 1 and Level 2 to validate its resistance to spoofing attempts.
ISO/IEC 19794-5:2006: iProov complies with ISO/IEC 19794-5:2006, which specifies performance testing for biometric verification systems. The model has undergone audits by the UK National Physical Laboratory to ensure compliance with international biometric standards.
WCAG 2.1 AA and Section 508: iProov meets WCAG 2.1 AA accessibility standards, ensuring the model is accessible to users with disabilities. It also complies with Section 508 of the U.S. Rehabilitation Act, which mandates that electronic and information technology is accessible to people with disabilities.
IRAP and IP3 (Australia): iProov is certified to comply with IRAP (Information Security Registered Assessors Program) and meets IP3 (Identity Proofing Level 3) requirements for identity verification in Australia.
ISO/IEC 27001:2013: iProov is certified to ISO/IEC 27001:2013, demonstrating its commitment to Information Security Management Systems (ISMS). This certification ensures that iProov follows best practices for managing and securing sensitive data, critical to maintaining user privacy and security.
Data Privacy Regulations Compliance:

General Data Protection Regulation (GDPR): iProov complies with EU Regulation 2016/679 on data protection and privacy, ensuring that personal data is processed securely and in compliance with user consent and rights to access, rectification, and deletion.
UK Data Protection Act 2018: iProov adheres to the UK’s Data Protection Act, ensuring personal data is handled in accordance with UK-specific privacy laws, including data retention and security requirements.
Bank Secrecy Act (BSA): iProov is designed to comply with the Bank Secrecy Act (BSA) for anti-money laundering (AML) and know-your-customer (KYC) regulations, which is crucial for financial institutions to maintain accurate records and prevent money laundering.
Industry Standards and Certifications:

National Security Standards: iProov has been tested to meet national security standards by UK Home Office, Singapore Government, Australian Government, and the U.S. Department of Homeland Security, ensuring the model adheres to stringent government-level security and identity verification protocols.
eIDAS (EU Regulation): iProov complies with the eIDAS Regulation (EN 319 401), which governs electronic identification and trust services across the EU. The model also holds Modular Certifications for eSignature to the qualified level and eID Assurance High. Due to annual eIDAS audits, iProov also conforms to AMLD5 Article 24(1)(d) for identity verification in financial services.
ISO/IEC 30107-3: iProov conforms to ISO/IEC 30107-3, which defines standards for biometric liveness detection, ensuring the system is robust against presentation attacks. It has been tested by iBeta to Level 1 and Level 2 to validate its resistance to spoofing attempts.
ISO/IEC 19794-5:2006: iProov complies with ISO/IEC 19794-5:2006, which specifies performance testing for biometric verification systems. The model has undergone audits by the UK National Physical Laboratory to ensure compliance with international biometric standards.
WCAG 2.1 AA and Section 508: iProov meets WCAG 2.1 AA accessibility standards, ensuring the model is accessible to users with disabilities. It also complies with Section 508 of the U.S. Rehabilitation Act, which mandates that electronic and information technology is accessible to people with disabilities.
IRAP and IP3 (Australia): iProov is certified to comply with IRAP (Information Security Registered Assessors Program) and meets IP3 (Identity Proofing Level 3) requirements for identity verification in Australia.
ISO/IEC 27001:2013: iProov is certified to ISO/IEC 27001:2013, demonstrating its commitment to Information Security Management Systems (ISMS). This certification ensures that iProov follows best practices for managing and securing sensitive data, critical to maintaining user privacy and security.
Scanned ID Photos: The core data source for iProov is the scanned ID photo that Acuant processes. This is the ID photo from government-issued documents (e.g., driver’s license, passport, etc.) that will be compared to the user's selfie during the verification process.
Face Detection and Features: The Acuant scan may also include metadata, such as face coordinates and key biometric features (e.g., facial landmarks), which can be used for comparison during the matching process.
Selfie Images (For Comparison with ID Photos)

Selfie Photos: User-generated selfies are the primary input for iProov’s photo matching and liveness detection. The selfie is compared to the scanned ID photo to verify that the person submitting the identity matches the person on the ID.
Liveness Detection: In addition to the selfie itself, iProov analyzes the liveness of the image to ensure it is not a photo, video, or static image. Liveness detection can involve ensuring the face captured in the selfie is real-time, with features such as eye movement, blinking, and head movements verified to confirm the user is present and interacting with the device (as opposed to a spoofed image)

