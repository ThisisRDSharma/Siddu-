# Siddu-
 imagery flagged as high-risk represents an extremely small proportion of the total transactions, estimated to be 0.05% of the imagery processed through the platform. This limitation means that the data available for detecting and analyzing advanced or novel biometric attacks is significantly limited. Given the rarity of these high-risk incidents, there is a restricted dataset for training models and improving detection mechanisms for these sophisticated threats.
The development data used by iProov is highly relevant to its core modeling objectives of ensuring accurate biometric authentication and robust security threat detection. The metadata, which includes data like biometric test results, device information, and anti-spoofing test results, is vital for training and optimizing biometric models. This data enables the system to perform well across different devices and environmental conditions, ensuring the technology's accuracy and reliability. Imagery data, particularly high-risk imagery flagged during suspicious transactions, plays a crucial role in improving the model’s ability to detect novel biometric attack patterns and adapt to advanced spoofing attempts. These images are essential for training models to handle emerging security threats effectively. Additionally, alerts, which provide real-time data on system performance and security, are used to identify operational issues and potential vulnerabilities, ensuring that the models remain accurate and resilient. By continuously leveraging this development data, iProov can refine its authentication models, improving both security and user experience while adapting to evolving biometric threats.

To ensure the accuracy and security of the iProov authentication process, only the following formats are supported for image uploads:

PNG
JPEG
JP2 (JPEG 2000)
All other formats will be excluded from processing.

Additionally, images must meet the following requirements to be considered valid:

Maximum file size: 2 MB
Image Conformance: The image must comply with the ISO/IEC 19794 standard for information technology, which ensures proper alignment, quality, and compliance with biometric guidelines.
Eye Distance: The minimum distance between the subject's eyes must be 85 pixels in the image. This is essential for ensuring proper facial recognition accuracy.
Any data or images that do not meet these specifications will be automatically excluded from processing by the iProov model.
The iProov model uses a combination of facial behavior (including eye movement, blink patterns, and head pose), color reflection data (response to the time-limited session code’s color sequence, intensity, and facial depth analysis), and contextual information (such as device metadata and session history) to verify a user's authenticity. The reflection of light from the skin during the color sequence is analyzed to confirm liveliness, ensuring that the biometric data is coming from a genuine human and not a spoof (e.g., photo or video). Environmental factors such as lighting conditions and background noise also play a role in ensuring accurate verification. These variables work together to assess the genuine presence of a live user and mitigate identity fraud by analyzing dynamic facial behavior and contextual data in real-time.
Explanatory variables, also known as independent variables or features, are the factors or inputs that a model uses to explain or predict an outcome. In the context of machine learning or biometric verification, explanatory variables are the data points or characteristics that help the system make decisions about whether an authentication attempt is genuine or fraudulent.These variables can be anything from biometric features (e.g., facial landmarks) to contextual data (e.g., device information or session history).In the case of iProov’s face biometric verification system, the explanatory variables include a variety of factors that contribute to determining whether the user is a genuine human or an attempt at spoofing

Facial Behavior: This includes key features like eye movement, blink patterns, and head pose, all of which help assess the liveliness of the user. These behaviors are natural and dynamic, allowing the system to distinguish a real person from static images or videos.

Color Reflection Data: During the authentication process, the system illuminates the face with a sequence of colors. The reflection of light from the skin during this process is an important explanatory variable. The way light reflects from the user's skin confirms liveliness and ensures the presence of a real human, not a spoofed attempt using a photo or video.

Contextual Information: This includes details like device metadata (e.g., device type, operating system) and session history, which provide additional layers of context around the authentication attempt, helping to verify the legitimacy of the session.
The response variable in iProov's model is the alert system that indicates the performance and outcome of the biometric verification process.
he response variable in iProov's model is the alert system that indicates the performance and outcome of the biometric verification process. 
the two main types of explanatory variables for your iProov model are metadata and imagery, 
Metadata refers to the contextual information surrounding the authentication attempt. This data helps assess the authenticity of the session and provides insights into the environment in which the verification is taking place.
