# 🔍 Loan Default Prediction

Proyek ini bertujuan untuk membangun model machine learning yang mampu memprediksi nasabah berisiko gagal bayar berdasarkan data pinjaman, dengan fokus pada akurasi dan ketepatan dalam mengenali kelas minoritas (nasabah default).

---

## 📁 Struktur Proyek


---

## 🎯 Tujuan Bisnis

- Mengurangi risiko kerugian akibat kredit macet
- Membantu tim keuangan dan analis risiko mengidentifikasi nasabah berisiko lebih awal
- Menyusun kebijakan kredit yang lebih tepat sasaran

---

## ⚙️ Teknik dan Pendekatan

- **Preprocessing:**
  - Imputasi nilai kosong
  - One-Hot Encoding untuk fitur kategorikal
  - StandardScaler untuk fitur numerik (khusus model sensitif skala)
  - Penanganan outlier dengan Z-Score

- **Modeling:**
  - Logistic Regression
  - K-Nearest Neighbors (KNN)
  - SMOTE untuk penyeimbangan kelas
  - Hyperparameter Tuning (RandomizedSearchCV)

- **Evaluasi:**
  - Metrik utama: **F1-Score**
  - Tambahan: Accuracy, Precision, Recall, ROC AUC, PR AUC

---

## 🏆 Hasil Utama

| Model               | Accuracy | Precision | Recall | F1-Score | PR AUC |
|--------------------|----------|-----------|--------|----------|--------|
| Logistic Regression | 0.8312   | 0.6689    | 0.6241 | 0.6457   | 0.7562 |
| KNN                | 0.8976   | 0.8382    | 0.7244 | 0.7772   | 0.8809 |
| **KNN + SMOTE**    | **0.8559** | 0.6630    | **0.8448** | **0.7429** | **0.8553** |

✅ **Model terbaik: KNN + SMOTE** – memberikan keseimbangan optimal antara mengenali nasabah gagal bayar dan menjaga presisi.

---

## 🧠 Insight Bisnis

- Nasabah dengan tujuan pinjaman seperti **refinancing** dan **renovasi** memiliki kecenderungan lebih tinggi untuk gagal bayar
- Jenis kredit (credit bureau) juga menjadi indikator penting risiko
- Model yang mampu menangkap nasabah default lebih efektif membantu pengambilan keputusan kredit

---

## 🚀 Cara Menjalankan

```bash
# Clone repo
git clone https://github.com/username/loan-default-prediction.git
cd loan-default-prediction

# Instal dependensi
pip install -r requirements.txt

# Jalankan skrip utama (jika ada)
python main.py
