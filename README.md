# 🚦 Sistem Peringatan Dini Kualitas Udara Jakarta: Analisis Prediktif dan Kontekstual Menggunakan IBM Granite

## 📌 Project Overview  
Polusi udara adalah salah satu tantangan lingkungan dan kesehatan terbesar di Jakarta. Tingginya tingkat polutan seperti **PM10** berkorelasi langsung dengan meningkatnya kasus **ISPA**, yang berdampak pada jutaan warga.  

Meskipun data kualitas udara tersedia, sifatnya sering kali teknis dan reaktif sehingga masyarakat serta pemangku kepentingan sulit mengambil tindakan preventif.  

Proyek ini bertujuan membangun **prototipe sistem peringatan dini (early warning system)** yang:  
- ✅ Memprediksi **kapan** polusi udara akan tinggi.  
- ✅ Menjelaskan **mengapa** polusi meningkat dengan analisis berbasis AI.  

---

## 🔎 Pendekatan  
1. **Analisis Data Historis**  
   - Menganalisis data kualitas udara Jakarta (2010–2025).  
   - Identifikasi pola musiman polusi.  

2. **Pemodelan Prediktif**  
   - Menggunakan **XGBoost** untuk memprediksi konsentrasi PM10.  
   - Validasi performa dengan **Mean Absolute Error (MAE)**.  

3. **Analisis Kontekstual Berbasis AI**  
   - Memanfaatkan **LLM IBM Granite** untuk menganalisis artikel berita.  
   - Mengekstrak penyebab utama polusi dari teks tidak terstruktur.  

---

## 📂 Pengumpulan Data  
- **Data Kuantitatif** → Dataset ISPU (PM10, PM2.5, O3, dll.) [Kaggle].  
- **Data Kualitatif** → Artikel berita tentang polusi udara Jakarta (2–3 tahun terakhir).  

---

## 📊 Insight & Findings  

### 🔹 Temuan 1: Polusi Udara Bersifat Musiman  
- Polusi meningkat signifikan di **musim kemarau** (Juni–Oktober).  
- Faktor iklim berperan besar dalam fluktuasi polusi.  

### 🔹 Temuan 2: Model Prediktif Akurat  
- **XGBoost** mampu memprediksi PM10 harian dengan baik.  
- **MAE = 7.20**, prediksi mengikuti tren aktual dengan ketat.  

### 🔹 Temuan 3: Tren Jangka Pendek Jadi Prediktor Terkuat  
- Fitur paling penting: **pm10_rolling_mean7** (rata-rata 7 hari terakhir).  
- Menunjukkan sifat polusi yang **persisten**.  

### 🔹 Temuan 4: Emisi Kendaraan = Narasi Utama Media  
- Analisis AI (IBM Granite) → penyebab terbanyak:  
  1. 🚗 Emisi Kendaraan  
  2. 🏭 Aktivitas Industri  
  3. 🌦 Kondisi Meteorologi  

---

## 🤖 Peran IBM Granite (AI Support)  
LLM IBM Granite digunakan untuk memperkaya analisis:  
- **Ekstraksi Terstruktur** → Mengubah ratusan paragraf berita menjadi kategori penyebab polusi.  
- **Analisis Kontekstual Skala Besar** → Menyintesis narasi dari puluhan sumber secara objektif.  
- **Rekomendasi Berbasis Data** → Fokus pada **emisi kendaraan** sebagai penyebab dominan.  

---

## ✅ Kesimpulan  
Proyek ini menunjukkan bahwa sistem peringatan dini kualitas udara yang **cerdas & actionable** dapat dibangun dengan menggabungkan:  
- **XGBoost (Prediksi “Kapan”)**  
- **IBM Granite (Analisis “Mengapa”)**  

Hasilnya: sistem yang **akurat, kontekstual, dan dapat ditindaklanjuti**.  

---

## 💡 Rekomendasi  

### Untuk Pemerintah Daerah  
- Terapkan **dasbor peringatan dini**.  
- Saat prediksi menunjukkan risiko tinggi akibat **emisi kendaraan**, segera aktifkan kebijakan seperti:  
  - Perluasan aturan ganjil-genap.  
  - Himbauan **WFH**.  

### Untuk Publik  
- Kembangkan **aplikasi mobile / chatbot WhatsApp** terintegrasi.  
- Contoh notifikasi:  
  > ⚠️ *Peringatan*: Besok kualitas udara diperkirakan **TIDAK SEHAT** akibat emisi kendaraan. Gunakan masker & transportasi publik.  

---

✍️ **Developer**: Muhammad Farrel Caesarian
📅 **Tahun**: 2025  
