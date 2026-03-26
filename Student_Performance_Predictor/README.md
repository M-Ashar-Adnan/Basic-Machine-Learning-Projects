# Student Performance Prediction: Analyzing Demographic Impacts

**Abstract**
This project explores the application of machine learning regression techniques to predict student academic outcomes. By deliberately excluding past academic records from the feature set, this work humbly attempts to quantify the impact of socio-demographic factors—specifically focusing on variables like internet access and study time—on final educational achievement.

**1. Introduction & Motivation**
Predicting student performance is a critical task for educational institutions aiming to provide proactive support. However, models that rely heavily on past grades often state the obvious. The motivation behind this specific implementation is to build a predictive model that relies entirely on environmental, social, and demographic inputs. This allows us to investigate how external factors influence a student's final grade.

**2. Dataset Characteristics**
This project utilizes the UCI Student Performance dataset, which records the achievements of students in secondary education at two Portuguese schools. To ensure the model learns from environmental factors rather than historical performance, the previous period grades (`G1` and `G2`), as well as unrelated behavioral metrics, were strictly removed from the feature space. The target variable is the final year grade (`G3`).

**3. Methodology & Preprocessing**
To prepare the dataset for regression analysis, several data engineering steps were executed:
* **Feature Selection:** Deliberate removal of highly correlated historical grades to force the model to evaluate demographic and lifestyle features.
* **Categorical Encoding:** The dataset contains numerous textual features (e.g., internet access 'yes'/'no', guardian type). These were algorithmically transformed into machine-readable numeric formats using standard Label Encoding.
* **Target Definition:** The final grade (`G3`), a continuous numerical value, was isolated as the target for our regression pipeline.

**4. Model Training & Evaluation**
A Random Forest Regressor was selected for this task due to its ability to handle complex interactions between multiple categorical and numerical variables without requiring extensive hyperparameter tuning. The model is evaluated using the R-squared metric, which provides insight into the proportion of the variance in the final grades that can be explained by the student's demographic and environmental profile.

**5. Replication & Usage**
To review the implementation and execute the code, clone the master repository and navigate to this specific project directory:

