# Bank Marketing Campaign Prediction- Capstone Project

> Machine Learning project untuk memprediksi apakah seorang nasabah akan melakukan **deposit** dalam sebuah kampanye pemasaran bank. Model ini bertujuan untuk membantu bank dalam menargetkan nasabah secara lebih efektif sekaligus mengoptimalkan biaya promosi.

---

## 🔍 Project Overview

Dalam proyek ini, dilakukan analisis dan pembangunan model klasifikasi untuk memprediksi keputusan pelanggan berdasarkan data kampanye pemasaran bank. Model dikembangkan untuk membantu pengambilan keputusan marketing yang lebih akurat dan efisien, serta mengurangi kerugian finansial dari kesalahan prediksi yang dilakukan.

---

## 🧾 Problem Statement

Bank perlu mengetahui **siapa saja pelanggan yang berpotensi melakukan deposit** dalam suatu kampanye pemasaran. Salah sasaran dalam promosi menyebabkan kerugian biaya (False Positive), sedangkan gagal mengidentifikasi pelanggan potensial menyebabkan hilangnya peluang (False Negative).

---

## 📦 Libraries & Tools

* Python (pandas, numpy, seaborn, matplotlib)
* Scikit-learn (Logistic Regression, Random Forest, XGBoost, Metrics)
* Jupyter Notebook
* Seaborn & Matplotlib (visualisasi)

---

## 🧪 Modeling Approach

### ✅ Evaluasi Model

- **ROC AUC Score**:
  -  Model A: 0.8031
  
- **Precision-Recall Curve**:
  - Menunjukkan trade-off antara **presisi vs jangkauan (recall)**

- **Confusion Matrix**:
  - Dihitung estimasi **kerugian finansial dari FP dan FN**

### 🔁 Algoritma yang Digunakan
- Random Forest Classifier


## 📉 Kerugian Finansial (Asumsi)

| Jenis Error    | Penjelasan           | Biaya per kasus | Total              |
| -------------- | -------------------- | --------------- | ------------------ |
| False Positive | Salah target promosi | Rp 500.000      | Rp 89.000.000      |
| False Negative | Kehilangan nasabah   | Rp 5.000.000    | Rp 735.000.000     |
| **Total Loss** |                      |                 | **Rp 824.000.000** |

---

## 📌 Business Recommendation

* Fokus pada **minimasi False Negative** karena berdampak lebih besar secara finansial.
* Gunakan **threshold optimal** berdasarkan trade-off dari ROC/PR curve.
* Terapkan model pada data baru secara berkala dan update model dengan data terkini.
* Segmentasikan nasabah berdasarkan prediksi untuk strategi kampanye yang lebih personal.

---

## 📈 Feature Correlation Insight

Dari korelasi numerik:

* `pdays` dan `deposit`: korelasi positif (0.16)
* `campaign` dan `deposit`: korelasi negatif (-0.13)

  * Terlalu banyak kontak justru menurunkan peluang sukses.
* `balance` dan `deposit`: korelasi rendah namun positif (0.09)

---

## 🚀 Future Improvement

* Feature Engineering untuk meningkatkan hasil score prediksi
* Hyperparameter tuning pada model Random Forest dan XGBoost.
* Cross-validation lebih mendalam (Stratified KFold).

---

> Project ini merupakan bagian dari Capstone 3 dari Program JCDS Purwadhika Digital School
