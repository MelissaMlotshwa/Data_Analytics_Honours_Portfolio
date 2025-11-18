## **Demographic Profiling of Purchase Intent Using Probabilistic Models**

## 🎯 Project Goal: Conditional Probability Analysis for Customer Segmentation
This project applies **Bayesian inference** to perform **demographic profiling** of customer purchase intent.  
The goal is to determine which combinations of demographic variables are most likely to result in different purchase intention types by comparing **unbalanced** and **synthetically balanced** Bayesian Networks (developed in Assignment 2).  
The output provides actionable insights for segmentation and targeted marketing.

---

## 🛠️ Methodology & Scope of Work

### 1. Preparation and Model Utilization
- **Models Used:** Saved Bayesian Networks (`.pkl`) from Assignment 2 — Raw, SMOTE, ML-Balanced, and GAN-Balanced.  
- **Demographic Variables:** Gender, Marital Status, Age, Education Level, Employment Status.

### 2. Conditional Probability Calculation (Inference)
- **Core Task:** Compute  
  P(Purchase Intention | Demographic Combination)  
  across all demographic permutations for all four networks.  
- **Visualisation:** An *Inference Decision Tree* was used to show how demographic splits drive probability changes.

### 3. Comparative Analysis: Balanced vs Unbalanced Networks

| Model Type | What It Represents | Purpose of Balancing |
|-----------|--------------------|-----------------------|
| **Unbalanced** | True skewed market data | Provides a realistic baseline |
| **Balanced (ML, SMOTE, GAN)** | Re-weighted / re-sampled distributions | **Reduces bias** and uncovers minority-class uplift |

---

## 🔍 Key Results: High-Probability Demographic Profiles

The most probable purchase-intent profiles show clear segmentation differences between balanced and unbalanced networks:

| Bayesian Network | Highest-Probability Profile | Strategic Interpretation |
|------------------|-----------------------------|---------------------------|
| **Unbalanced / ML-Balanced** | Older (50–65), Male, Basic Education, Married, Unemployed | **Established & Unemployed Segment** — dominant baseline market |
| **SMOTE-Balanced** | Older (50–65), Female, Basic Education, Married, Unemployed | **Gender Shift** — balancing suggests older unemployed women become top uplift segment |
| **GAN-Balanced** | Younger (23–28), Female, Diploma, Single, Employed | **Young Aspirational Segment** — high-growth, upwardly mobile buyers |

---

## ⚠️ Critical Reflection on Bias & Reliability
- Balanced data can distort reality by exaggerating minority-class signals.  
- Small datasets cause **high sensitivity** to noise when computing conditional probabilities.  
- Insights derived from synthetic balancing should **always** be validated using domain knowledge and external data.

---

## 📈 Real-World Targeted Marketing Implications

**1. Established & Unemployed Segment**  
- Focus on **discounts, loyalty rewards, essential goods, and affordability-driven messaging**.

**2. Young & Employed Aspirational Segment**  
- Emphasise **quality, innovation, convenience, and lifestyle-aligned products**.

## Inference Decision Tree for Purchase Probability

<img width="1394" height="697" alt="image" src="https://github.com/user-attachments/assets/b690cfcc-ab21-46ad-b4a9-03b1eaaaeab5" />
