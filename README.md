# Student Academic Performance Classification

## 📖 Deskripsi
Proyek ini membandingkan dua algoritma machine learning dalam mengklasifikasikan performa akademik siswa:
- **Multinomial Logistic Regression**
- **Support Vector Machine (SVM)**

Dataset: `xAPI-Edu-Data.csv` (480 observasi, 17 fitur)  
Target: `Class` → Low, Middle, High  

---

## 🛠️ Metodologi
1. **Preprocessing**: Label Encoding, Scaling (StandardScaler)  
2. **Cross-Validation**: 5-fold untuk evaluasi awal  
3. **Grid Search**: Tuning parameter Logistic Regression & SVM  
4. **Evaluasi**: Akurasi, Precision, Recall, F1-score, Confusion Matrix  
5. **Feature Importance**: Koefisien LR & Permutation Importance (SVM)  

---

## 📊 Hasil Utama
- Logistic Regression & SVM sama-sama mencapai akurasi **79%**.  
- Logistic Regression lebih **seimbang antar kelas**, SVM lebih baik untuk kelas dominan.  
- Fitur penting: **StudentAbsenceDays**, **raisedhands**, **VisITedResources**.  

---

## 📈 Review
- 🔍 **Akurasi 79%** pada kedua model, cukup baik untuk dataset pendidikan.  
- 🎯 Logistic Regression unggul dalam *interpretabilitas*, cocok untuk insight praktis bagi guru/sekolah.  
- ⚡ SVM lebih kuat dalam menangani data non-linear, cocok jika ingin model yang lebih tajam.  
- 📊 Confusion Matrix menunjukkan kesulitan terbesar ada pada prediksi **kelas rendah (Low)**.  

---

## 🧰 Tools yang Digunakan
- **Python (Colab/Jupyter)** → implementasi model machine learning  
- **Excel** → eksplorasi awal dataset, pengecekan missing value  
- **Word** → penyusunan laporan akhir  
