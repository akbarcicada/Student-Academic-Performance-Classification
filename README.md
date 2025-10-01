### README.md

# NHANES Health Clustering with K-Means & DBSCAN

## 📖 Deskripsi
Proyek ini membandingkan dua metode clustering:
- **K-Means** → berbasis centroid
- **DBSCAN** → berbasis kepadatan & deteksi outlier

Dataset: `NHANES.csv` (2.278 observasi, 10 fitur)  
Fokus: Segmentasi berdasarkan variabel metabolik (BMI, glukosa, insulin, usia).  

---

## 🛠️ Metodologi
1. **Preprocessing**: Normalisasi fitur numerik (z-score)  
2. **K-Means**: Eksperimen k=2–10 → Elbow & Silhouette untuk jumlah cluster optimal  
3. **DBSCAN**: Eksperimen parameter eps (k-distance graph) & min_samples  
4. **Evaluasi**: Silhouette Score, Davies-Bouldin Index, validasi eksternal `age_group`  
5. **Interpretasi**: Analisis profil tiap cluster  

---

## 📊 Hasil Utama
- **K-Means**: optimal di **k=5**, menghasilkan klaster mulai dari *muda sehat* hingga *lansia berisiko metabolik*.  
- **DBSCAN**: eps≈2, min_samples=5 → 8 cluster bermakna + outlier. Mendeteksi detail risiko seperti resistensi insulin & gangguan glukosa berat.  

---

## 📈 Review
- 📍 K-Means efektif menemukan **5 segmen besar**: muda sehat, usia menengah, obesitas, hingga lansia dengan risiko metabolik.  
- 🚨 DBSCAN lebih detail: menghasilkan **8 klaster + noise**, mampu mengidentifikasi *outlier* dengan risiko diabetes tinggi.  
- 🧬 Pola menarik: **BMI tinggi + insulin tinggi** → cluster dengan risiko resistensi insulin serius.  
- 👥 Validasi eksternal menunjukkan klaster selaras dengan kategori **usia (age_group)**.  

---

## 🧰 Tools yang Digunakan
- **Python (Colab/Jupyter)** → implementasi K-Means & DBSCAN  
- **Excel** → eksplorasi awal dataset, distribusi variabel  
- **Word** → dokumentasi hasil & interpretasi  
