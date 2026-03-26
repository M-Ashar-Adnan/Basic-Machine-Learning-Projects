# Network Traffic Anomaly Detection: An Intrusion Detection Model

**Abstract**
This project presents a humble investigation into securing digital infrastructure through machine learning. By utilizing an ensemble classification model on network traffic logs, this work seeks to accurately distinguish between benign network activity and malicious intrusions, contributing to the foundational study of automated Intrusion Detection Systems (IDS).

**1. Introduction & Motivation**
As network architectures grow increasingly complex, traditional rule-based security measures often struggle to identify novel cyber threats. This project explores a data-driven alternative, leveraging historical network traffic patterns to train a machine learning model capable of recognizing the statistical anomalies that are highly indicative of a cyberattack. 

**2. Dataset Characteristics**
This implementation utilizes the NSL-KDD dataset, a widely respected benchmark in the field of network security. The dataset captures complex connection details, including basic features (like protocol type and packet duration), content features (like login failures), and broader traffic routing characteristics. The target variable encompasses a wide taxonomy of attacks (e.g., Denial of Service, Probing) which have been aggregated into a straightforward binary classification: 'normal' or 'anomaly'.

**3. Methodology & Preprocessing**
To prepare the raw connection logs for algorithmic processing, several rigorous data engineering transformations were applied:
* **Binary Mapping:** The diverse array of specific attack labels was consolidated into a single anomalous class (`1`), with standard traffic mapped as normal (`0`).
* **Categorical Encoding:** Non-numeric network features, such as `protocol_type`, `service`, and `flag`, were mathematically transformed using One-Hot Encoding to ensure compatibility with the classifier.
* **Standardization:** To prevent features with massive numerical ranges (such as byte transfer sizes) from disproportionately influencing the model, all inputs were normalized using standard z-score scaling.

**4. Model Training & Evaluation**
A Random Forest classifier was deployed to capture the highly non-linear relationships within the multidimensional network data. The evaluation methodology heavily weights the precision and recall metrics. In a practical IDS environment, minimizing false negatives (undetected attacks) is absolutely critical, while managing false positives is necessary to prevent alert fatigue for network administrators.

**5. Replication & Usage**
To review the implementation and execute the code, clone the master repository and navigate to this specific project directory:
