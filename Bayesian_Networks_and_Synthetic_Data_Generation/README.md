# Bayesian Networks and Synthetic Data Generation for Subsistence Retail Analytics

## 🎯 Project Goal

This project investigates the impact of different **synthetic data generation techniques** on class imbalance and evaluates how these techniques affect the performance of a **Bayesian Network (BN)** predicting Purchase Intention in the Soweto subsistence retail dataset.

---

## 🛠️ Methodology Overview

### **1. Class Imbalance Analysis**

* The raw dataset exhibited **severe class imbalance** across Purchase Intention categories.
* This imbalance impaired the model’s ability to learn and detect minority classes.

### **2. Data Exploration & Pre-processing**

* Data quality review
* Structural validation
* Preparation for synthetic data generation and BN modelling

---

## 🧪 Synthetic Data Generation Methods

### **SMOTE-Based Synthetic Data**

* Oversamples minority classes using feature-space interpolation.
* Generates balanced numeric samples based on nearest-neighbour distances.

📌 **Confusion Matrix**

<img width="631" height="659" alt="image" src="https://github.com/user-attachments/assets/880f2d68-4dac-4479-833a-6b0db38cb55f" />


📌 **Bayesian Network DAG**

<img width="631" height="659" alt="image" src="https://github.com/user-attachments/assets/9487592a-1026-4fa2-9611-a1261de2b582" />


---

### **ML-Based Synthetic Generators**

* Uses ML models (KNN, Random Forest, etc.) to impute new samples for minority classes.
* Generates synthetic values based on predicted patterns.

📌 **Confusion Matrix**

<img width="717" height="619" alt="image" src="https://github.com/user-attachments/assets/be2671f3-a54e-4901-9489-7bdff74bdb7f" />


📌 **Bayesian Network DAG**

<img width="633" height="697" alt="image" src="https://github.com/user-attachments/assets/24ce458b-0006-4a21-b484-74d345672abe" />


---

### **GAN-Based Synthetic Data**

* Uses a **Generative Adversarial Network** to learn underlying joint distributions.
* Generates synthetic tabular samples through adversarial training between Generator and Discriminator.

📌 **Confusion Matrix**

<img width="756" height="674" alt="image" src="https://github.com/user-attachments/assets/de790ece-3f94-412c-8ba8-f2cf27588ac1" />

📌 **Bayesian Network DAG Placeholder**

<img width="684" height="674" alt="image" src="https://github.com/user-attachments/assets/615f6661-3fb5-4adb-9004-595780355744" />

---

## 🧠 Bayesian Network Modelling

Four Bayesian Networks were trained and evaluated:

1. **Raw Imbalanced Baseline**
2. **SMOTE-Balanced BN**
3. **ML-Balanced BN**
4. **GAN-Balanced BN**

Evaluation metrics included:

* **Accuracy**
* **F1-score**
* **Recall**
* Minority class identification ability

---

## 📊 Key Findings (Table Format)

| Model Type                    | Performance Summary                                             | Interpretation                                                  |
| ----------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- |
| **Raw Imbalanced (Baseline)** | Extremely biased; fails to detect minority classes              | Not viable due to severe class imbalance                        |
| **ML-Balanced**               | Lowest Accuracy and F1-score                                    | ML-based synthesis did not generate meaningful minority samples |
| **SMOTE-Balanced**            | **Best Recall and F1-score**; strong minority class performance | Most effective balancing method; best BN model                  |
| **GAN-Balanced**              | Highest Accuracy but lower Recall/F1 than SMOTE                 | Some generated samples may be noisy or non-representative       |

---

## ✔️ Final Conclusion

Raw Imbalanced: Baseline suffers from extreme bias, effectively unable to find the minority class.
* ML-Balanced: Lowest accuracy and F1, the ML imputation method did not effectively synthesize or structure meaningful minority data.
* SMOTE-Balanced: Best performance. Achieved the highest F1-score and Recall, successfully identifying minority samples.
* GAN-Balanced: Highest Accuracy, but lower Recall/F1 than SMOTE, may have synthesized noise or non-representative data.
