# Machine Learning Portfolio: Foundational Models & Data Engineering

**Abstract**
This master repository contains three distinct machine learning projects developed to demonstrate practical competency in data engineering, algorithmic training, and model evaluation. The projects span classification, anomaly detection, and regression tasks, serving as a foundational exploration of predictive modeling for real-world datasets.

**1. Credit Card Fraud Detection (Classification & Over-sampling)**
* **Objective:** To accurately identify fraudulent financial transactions within a highly imbalanced dataset.
* **Methodology:** Applied the Synthetic Minority Over-sampling Technique (SMOTE) to synthetically balance the training data, preventing the normal transactions from overwhelming the model. A Random Forest classifier was utilized, prioritizing the recall of the minority (fraud) class.
* **Key Skills:** Data Standardization, Handling Imbalanced Datasets, SMOTE, Precision/Recall Optimization.

**2. Network Traffic Anomaly Detection (Intrusion Detection)**
* **Objective:** To distinguish between benign network traffic and malicious cyberattacks using historical connection logs.
* **Methodology:** Processed the NSL-KDD dataset by mapping various attack types into a single 'anomaly' class. Categorical network features were transformed using One-Hot Encoding before training an ensemble classifier to detect statistical irregularities.
* **Key Skills:** Categorical Feature Encoding, Binary Classification, Cybersecurity Data Processing, False-Negative Reduction.

**3. Student Performance Predictor (Regression Analysis)**
* **Objective:** To predict final academic grades based strictly on student demographics and environmental factors, such as internet access and study habits.
* **Methodology:** Deliberately excluded historical grade data to force the model to learn from external socio-demographic inputs. A Random Forest Regressor was trained on the encoded dataset, utilizing the R-squared metric to evaluate variance.
* **Key Skills:** Regression Modeling, Feature Selection, Label Encoding, R-squared Evaluation.

**Technical Stack**
* **Environment:** Jupyter Notebook / Google Colab
* **Libraries:** Python, Pandas, Scikit-Learn, Imbalanced-Learn, Matplotlib, Seaborn
