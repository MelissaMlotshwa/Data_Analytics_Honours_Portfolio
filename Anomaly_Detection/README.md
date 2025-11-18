## Anomaly Detection in Time-Series

This project focuses on building a **high-performance anomaly-detection system** capable of identifying abnormal patterns in temporal datasets.
By leveraging ensemble anomaly detection techniques, the model achieved a strong final performance score of **94% accuracy** on unseen test data.

---

## 🧠 Theoretical Overview of Anomaly Detection Models

### **Isolation Forest — Isolation-Based Detection**

Isolation Forest isolates anomalies by randomly splitting features until a point is isolated.
Anomalies are easier to isolate → require fewer splits → shorter path length.

**Advantages:**

* Fast, scalable
* No distribution assumptions
* Great for sparse anomalies

---

### **One-Class SVM (OCSVM) — Boundary-Based Detection**

Learns a hypersphere/hyperplane enclosing most data.
Anything outside this learned boundary is flagged as an anomaly.

**Advantages:**

* Captures subtle distributional shifts
* Effective for smooth or continuous drifts in time-series

---

### **Ensemble Strategy — Hybrid Detection**

Combines the complementary strengths of Isolation Forest and OCSVM.
Produces:

* Higher recall for true anomalies
* Lower variance in predictions
* More stable detection across datasets

---

## 🛠️ Methodology & Pipeline

### **1. Data Preprocessing & Feature Engineering**

Built temporal features to capture patterns over time:

* Lag features
* Rolling-window features (mean, STD, min, max)
* Rate-of-change
* Time indexing (sequential order)

---

## 📊 Visualisation Outputs

### **Overview of the Dataset**

<img width="1489" height="990" alt="image" src="https://github.com/user-attachments/assets/c1387540-e17b-4a38-87e9-4a1966e4fbbb" />

---

### **Distribution Analysis**

Exploring value ranges, density, and skewness of the dataset.

<img width="1489" height="990" alt="image" src="https://github.com/user-attachments/assets/56b89c89-8f00-4488-a589-a25f70aeb66b" />


---

### **Multiple Series Grid**

Shows all time-series channels simultaneously.

<img width="1489" height="1790" alt="image" src="https://github.com/user-attachments/assets/45628947-09d6-45f4-ac4c-8f15914b0ae3" />



---

### **Detailed View of First Dataset**

Zoomed analysis of the first time-series segment.

<img width="1489" height="990" alt="image" src="https://github.com/user-attachments/assets/7a979a3a-127e-49bf-9828-d8e49994c3a9" />


---

### **Model Scores for First Dataset**

Performance comparison of each anomaly detection model.

<img width="1489" height="1189" alt="image" src="https://github.com/user-attachments/assets/78edc489-6d54-4411-b257-13d156fc3e09" />


---

### **Feature Analysis for First Dataset**

Importance or contribution of engineered features.

<img width="1490" height="1190" alt="image" src="https://github.com/user-attachments/assets/9d218eee-5738-4844-b455-02d12ff2de6d" />


---

## 🧮 Results & Performance

### **Final Model Performance Table**

| Metric       | Score                                               |
| ------------ | --------------------------------------------------- |
| **Accuracy** | **94%**                                             |


### **Interpretation of Results**

* **94% accuracy** indicates strong generalisation to unseen data.
* The ensemble successfully captured both structural and distributional anomalies.
* Temporal feature engineering contributed significantly to improving model sensitivity and robustness.

