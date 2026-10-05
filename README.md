# Credential Stuffing Attack Detection Using Gradient Boosting Machine and Isolation Forest

## Project Overview

This repository contains the Machine Learning project **Credential Stuffing Attack Detection Using Gradient Boosting Machine and Isolation Forest**.

Credential stuffing is a cybersecurity attack in which attackers use previously leaked username-password combinations to automate login attempts against other services. The objective of this project is to analyze login and network-related activity and classify suspicious sessions using machine learning.

The project combines two complementary approaches:

- **Gradient Boosting Machine (GBM)** / GradientBoostingClassifier for supervised attack classification.
- **Isolation Forest** for unsupervised anomaly detection.

The project was developed as part of the **Machine Learning** course for the Bachelor of Technology program, A.Y. 2026-27.

## Team

| Name | Roll Number |
|---|---|
| Hruday Deepak | 2520030138 |
| Surya | 2520030145 |
| Aasritha | 2520030178 |

Guide: **Dr. Ravinder, Associate Professor, CSE**

## Abstract

Cybersecurity is one of the most critical concerns for online platforms because user accounts and sensitive information are continuously exposed to automated attacks. Credential stuffing is a major threat in which attackers use stolen username-password pairs obtained from previous data breaches to attempt unauthorized access to multiple accounts. Detecting these attacks accurately can help organizations prevent account takeover, protect user privacy, reduce fraud, and maintain trust.

This project develops a machine learning-based credential stuffing detection system using login and network-related features. The data is inspected and prepared through preprocessing, including missing-value handling, categorical encoding, feature preparation, and train/test splitting. Relevant attributes include network packet size, protocol type, login attempts, session duration, encryption method, IP reputation score, failed login count, browser type, unusual-time access, and the attack label.

A Gradient Boosting classifier is used as the primary supervised learning model to classify malicious and legitimate sessions. Isolation Forest is additionally used to identify unusual observations without relying solely on labelled data. The models are evaluated using Accuracy, Precision, Recall, F1-Score, ROC-AUC, confusion matrix, and related visualizations. The overall goal is to demonstrate how machine learning can strengthen authentication security and support real-time detection of suspicious login activity.

## Dataset

The project notebook loads the dataset from:

`cybersecurity_intrusion_data.csv`

The observed dataset contains **9,537 records and 11 columns**.

Main attributes include:

- `session_id`
- `network_packet_size`
- `protocol_type`
- `login_attempts`
- `session_duration`
- `encryption_used`
- `ip_reputation_score`
- `failed_logins`
- `browser_type`
- `unusual_time_access`
- `attack_detected`

The target variable is `attack_detected`, where 0 represents a non-attack session and 1 represents a detected attack.

The dataset contains missing values in `encryption_used`; the notebook handles missing values as part of the preprocessing workflow.

## Machine Learning Workflow

The implemented workflow follows these stages:

1. Import Python and machine learning libraries.
2. Load the cybersecurity intrusion dataset.
3. Inspect the dataset shape, columns, data types, and sample records.
4. Analyze missing values.
5. Explore the target-class distribution.
6. Separate input features and target labels.
7. Prepare numerical and categorical features.
8. Apply imputation, encoding, and scaling where required.
9. Split the data into training and testing sets.
10. Train the Gradient Boosting classifier.
11. Train an Isolation Forest anomaly detector.
12. Generate predictions.
13. Calculate classification and anomaly-detection metrics.
14. Plot confusion matrices, ROC curves, and other relevant visualizations.
15. Compare model performance and identify practical use cases.

## Algorithms

### 1. Gradient Boosting Machine

Gradient Boosting builds an ensemble of decision trees sequentially. Each new tree attempts to correct errors made by the previous trees. For this project, it is used as a supervised binary classification model.

Advantages:

- Strong classification performance.
- Captures nonlinear relationships.
- Works well with mixed cybersecurity features after preprocessing.
- Provides a useful baseline for security-event classification.

### 2. Isolation Forest

Isolation Forest is an unsupervised anomaly detection algorithm. Instead of requiring every suspicious behavior to be labelled, it attempts to isolate unusual observations through randomized tree structures.

Advantages:

- Useful when labelled attack examples are incomplete.
- Can identify previously unseen abnormal behavior.
- Suitable for exploratory security monitoring.
- Complements supervised classification.

## Evaluation Metrics

The project uses several evaluation measures:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC
- Confusion Matrix
- Classification Report
- ROC Curve

For cybersecurity applications, Recall and F1-Score are especially important because failing to identify a malicious login can be more costly than incorrectly flagging a legitimate session.

## Software Requirements

- Python 3
- Jupyter Notebook or Google Colab
- Visual Studio Code (optional)
- Pandas
- NumPy
- Matplotlib
- Scikit-learn

## Installation

Create a Python environment and install the required packages:

```bash
pip install -r requirements.txt
```

## Running the Project

1. Place `cybersecurity_intrusion_data.csv` in the same directory as the notebook.
2. Open the notebook in Jupyter Notebook, JupyterLab, Google Colab, or VS Code.
3. Run the cells from top to bottom.
4. Review the preprocessing output and exploratory analysis.
5. Train the models.
6. Review the evaluation metrics and visualizations.

## Project Objectives

1. Prepare a suitable cybersecurity dataset for machine learning.
2. Perform systematic preprocessing and exploratory analysis.
3. Select relevant login and network features.
4. Train suitable supervised and unsupervised machine learning models.
5. Evaluate and compare model performance using appropriate metrics.
6. Demonstrate the practical application of ML for authentication security.

## Practical Applications

The proposed approach can be adapted for:

- Login security monitoring.
- Account takeover prevention.
- Suspicious authentication detection.
- Security operations dashboards.
- Automated risk scoring.
- Rate-limiting and access-control support.
- Fraud and bot detection.
- Real-time authentication monitoring.

## Future Enhancements

Future versions can extend the project with:

- Larger real-world security datasets.
- More advanced ensemble models.
- Hyperparameter optimization.
- Explainable AI using SHAP or similar techniques.
- Real-time streaming login analysis.
- Cloud deployment.
- Model-drift monitoring.
- External-dataset validation.
- REST API deployment.
- Security dashboard integration.
- Automated alerting for high-risk sessions.

## Project Structure

A recommended repository structure is:

```text
ML-Project/
├── README.md
├── requirements.txt
├── cybersecurity_intrusion_data.csv
├── Credential_Stuffing_Detection.ipynb
├── ML_Project_Report.docx
└── Credential_Stuffing_Detection.pptx
```

## Academic Information

**Course:** Machine Learning  
**Program:** Bachelor of Technology  
**Academic Year:** 2026-27  
**Department:** Computer Science and Engineering

## Keywords

Credential Stuffing, Cybersecurity, Machine Learning, Gradient Boosting, Isolation Forest, Anomaly Detection, Intrusion Detection, Authentication Security

## Disclaimer

This project is an academic machine-learning implementation intended for learning, experimentation, and demonstration. It should be validated with appropriate real-world security data and security controls before being used in production.
