# Mapping the Discourse and Sentiment in Social Media Data

## 📖 Introduction

The objective of this project is to extract and interpret the underlying structure of online discourse using **sentiment analysis** and **topic modelling** on a restricted social media dataset.
The analysis seeks to uncover:

* The **emotional tone** of public conversation
* The **dominant themes** discussed by users
* The **discursive dynamics** (how themes relate and interact)

### **Sentiment Analysis**

Sentiment analysis computationally identifies and categorises opinions expressed in text, detecting the writer’s **attitude**, **emotional tone**, and **subjective information**. It is used to classify text into categories such as **positive**, **negative**, or **neutral**, enabling large-scale understanding of public mood about events, products, or issues.

### **Topic Modelling**

Topic modelling uses **unsupervised machine learning** to uncover hidden structures and recurring patterns in large text corpora and is useful for identifying latent themes in unstructured social media data.
The process typically involves:

1. Determining the optimal number of topics using **coherence** and **perplexity** scores
2. Applying algorithms such as **Latent Dirichlet Allocation (LDA)** to automatically extract meaningful themes (Chen et al., 2020)

---

## 🧪 Methodology

### **1. Data Preprocessing and Cleaning**

Before performing sentiment analysis or topic modelling, the dataset underwent extensive preprocessing to ensure reliability and interpretability.

#### **Key Operations**

* **Text Cleaning:**
  Removed URLs, hashtags, mentions, emojis, and non-alphanumeric characters to standardise text and reduce noise.

* **Tokenisation:**
  Segmented sentences into individual tokens (words/terms) for computational processing.

* **Lemmatisation:**
  Reduced words to their base or dictionary form to group semantically similar terms (Loper et al., 2009).

* **Stop Word Removal:**
  Eliminated high-frequency but semantically irrelevant words (e.g., “the”, “and”, “is”) to emphasise meaningful linguistic content.

* **Column Selection:**
  Selected **Text** and **Timestamp** columns as the main analytical variables for both sentiment and topic modelling tasks.

This preprocessing pipeline enhances model performance and ensures that the text is normalised for downstream machine learning tasks (Liu, 2015; Camacho-Collados & Pilehvar, 2018).
Although computationally intensive, preprocessing is crucial for analytic reliability—particularly when working with noisy, unstructured, or uncertain data sources (Grimmer & Stewart, 2013).

---

## 📊 Dataset Summary

| Attribute             | Description          |
| --------------------- | -------------------- |
| **Source**            | Twitter (Microblogs) |
| **Timeframe**         | Feb 2023 – June 2023 |
| **Size**              | 10,000 microblogs    |
| **Unique Identifier** | Tweet ID             |

### 🔒 Ethical Compliance

* Removed all personally identifiable information
* Retained only **tweet_id**
* Analysis conducted at **aggregate level** to avoid doxxing or user targeting

---

## 🧠 Analytical Models

### **Sentiment Analysis — TextBlob**

Generated polarity scores and assigned each text a **Positive**, **Negative**, or **Neutral** label.

<img width="708" height="552" alt="image" src="https://github.com/user-attachments/assets/b947b8db-971a-447b-b931-c715253e6007" />

---

### **Topic Modelling — LDA**

* Implemented using **gensim**
* Optimal number of topics selected based on:

  * **Coherence Score**
  * **Perplexity Score**

<img width="1089" height="552" alt="image" src="https://github.com/user-attachments/assets/859aa96a-5390-4edd-8ee9-14787bc66a63" />

---

## 🧵 Discovered Themes

The topic model identified **four dominant themes**:

📌 **Customer Service**

<img width="790" height="428" alt="image" src="https://github.com/user-attachments/assets/aaf27736-87f3-4683-9183-a510ff7da7e9" />

📌 **Product Features**

<img width="790" height="428" alt="image" src="https://github.com/user-attachments/assets/ccd297c1-fbd0-40cc-92b1-3e1722aa5e78" />



📌 **Network Reliability**

<img width="790" height="428" alt="image" src="https://github.com/user-attachments/assets/b5a28d8c-050b-4710-be22-f66412566b08" />


📌 **Marketing & Hype**

<img width="790" height="428" alt="image" src="https://github.com/user-attachments/assets/80277a80-3e84-44cb-878b-a8c461a78693" />


---

## 🧠 Knowledge Mapping Insights

* **Product Features** and **Network Reliability** are the most central and highly connected components of the discourse.
* Strongest link: **Network Reliability ↔ Customer Service**
* **Marketing & Hype** is peripheral, generating isolated bursts of positive activity not strongly linked to central concerns.

📌 **Knowledge Network Graph:**

```
![Topic Network Graph](images/topic_network_graph.png)
```

---

## 📌 Conclusion

* The discourse is structurally coherent but marked by **emotionally strained interactions**, with many neutral statements and pockets of dissatisfaction.
* Four clear thematic pillars were identified, forming a comprehensive representation of public concerns.
* The intersection of **Network Reliability** and **Customer Service** emerged as the primary pain point driving negative sentiment.
* Combined sentiment, topic, and network analysis provides a scalable framework for interpreting large-scale social media discourse.
