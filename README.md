# Deep-Learning-Enhanced-Channel-Estimation-for-MIMO-Communication-Systems
# 📶 Wireless Channel Estimation using Machine Learning

This project explores the use of **machine learning models** to estimate and analyze **pathloss** in wireless MIMO systems. By examining key parameters such as **channel, distance, line of sight (LoS), and location**, the study predicts pathloss patterns and their influence on **channel estimation**, helping optimize wireless communication performance.

---

## 🚀 Objectives

- Estimate **pathloss** in wireless channels using ML.
- Analyze the **relationship between distance and pathloss**.
- Detect anomalies using **adaptive thresholding**.
- Evaluate model performance across **3 real-world-like scenarios**.

---

## 📁 Dataset Overview

Each entry in the dataset includes:

- `channel`: Identifier of the wireless channel
- `distance`: Distance between transmitter and receiver
- `line_of_sight`: 1 if LoS exists, 0 otherwise
- `pathloss`: Signal loss over distance

---

## 📊 Scenarios

### 📌 Scenario 1
- **Uniform increase** in pathloss with distance
- **LoS = 1** for all channels
- `distance` more important than `pathloss`

### 📌 Scenario 2
- **No consistent relation** between pathloss and distance
- **LoS = 0**
- `distance` again more important in predictions

### 📌 Scenario 3
- **Unpredictable changes** in pathloss
- **LoS = 1**
- `pathloss` becomes more important than `distance`

---

## 🤖 Machine Learning Models Used

| Model                | Accuracy | Precision | Recall | F1 Score |
|---------------------|----------|-----------|--------|----------|
| Logistic Regression | Low      | 0.1       | 0.1    | 0.1      |
| Decision Tree       | Low      | 0.1       | 0.1    | 0.1      |
| Naïve Bayes         | Low      | 0.1       | 0.1    | 0.1      |
| **ANN**             | **High** | 0.8       | 1.0    | 0.89     |

**Note:** Model performance varies by scenario. ANN showed the best results in Scenarios 1 & 3.

---

## 📈 Feature Importance (Decision Tree)

- Scenario 1 & 2: `distance` is the key feature.
- Scenario 3: `pathloss` is the dominant feature.

---

## 🧪 Anomaly Detection

- Used **adaptive thresholding** on the `pathloss` variable.
- Generated **class labels** to flag abnormal values.

---

## 🏁 Conclusion

This study demonstrates that:
- Pathloss can be **predicted effectively using ML**, especially with ANNs.
- **Distance and LoS impact prediction quality** significantly.
- Machine learning offers promising solutions for **real-time wireless channel estimation**.

---

## 🔧 Future Work

- Integrate additional parameters (e.g., Doppler shift, delay spread).
- Apply transfer learning to adapt across different environments.
- Deploy in real-time simulation for 5G or mmWave testing.
