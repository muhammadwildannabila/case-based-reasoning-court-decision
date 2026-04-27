
# ⚖️ Case-Based Reasoning for Court Decision Analysis

<div align="center">

![Python](https://img.shields.io/badge/Python-3.10-blue?style=for-the-badge&logo=python)
![AI](https://img.shields.io/badge/AI-Case--Based%20Reasoning-orange?style=for-the-badge)
![NLP](https://img.shields.io/badge/NLP-Legal%20Text-green?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Academic%20Project-lightgrey?style=for-the-badge)

### 🔵 Academic Project – Computational Reasoning  
Universitas Muhammadiyah Malang

</div>

---

### 🔍 Project Type
Academic Project | Artificial Intelligence | Case-Based Reasoning | 2025

---

## 📌 Project Overview

Proyek ini mengimplementasikan pendekatan **Case-Based Reasoning (CBR)** untuk menganalisis dan memprediksi putusan pengadilan pada kasus pidana, khususnya **pemalsuan dokumen**.

Sistem bekerja dengan mencari kasus terdahulu yang paling mirip, kemudian menggunakan informasi tersebut untuk memprediksi keputusan pada kasus baru.

---

## ⚙️ System Pipeline

Data Collection → Text Processing → Case Representation → Retrieval → Prediction → Evaluation

### Tahapan:
1. Scraping & cleaning dokumen putusan  
2. Representasi kasus dalam bentuk terstruktur  
3. Retrieval menggunakan TF-IDF / BERT  
4. Prediksi berdasarkan kemiripan kasus  
5. Evaluasi performa model  

---

## 📂 Project Structure

```
CBR_Putusan_Pemalsuan/
├── data/
│   ├── raw/                  # Hasil ekstraksi & cleaning putusan (txt)
│   ├── processed/            # File structured hasil representasi (CSV)
│   └── eval/                 # queries.json, ground_truth.csv, metrik evaluasi
├── results/                  # Hasil prediksi sistem
├── notebooks/                # Jupyter notebook tiap tahap
│   ├── 01_scraping.ipynb
│   ├── 02_representation.ipynb
│   ├── 03_retrieval.ipynb
│   ├── 04_predict.ipynb
│   └── 05_evaluation.ipynb
├── README.md                 # Dokumentasi proyek
├── requirements.txt          # Library yang dibutuhkan
```


---

## 🧪 Methodology

### 🔹 Case Representation
- Ekstraksi metadata kasus  
- Identifikasi pasal hukum  
- Ringkasan fakta hukum  

### 🔹 Retrieval
- TF-IDF similarity  
- (Opsional) Semantic similarity dengan BERT  

### 🔹 Prediction
- Menggunakan Top-K kasus paling mirip  
- Reuse solusi dari kasus terdahulu  

---

## 📊 Dataset

- Sumber: https://putusan3.mahkamahagung.go.id  
- Domain: **Pidana – Pemalsuan Dokumen**  
- Format: PDF → Teks → CSV  

---

## 📈 Evaluation

Model dievaluasi menggunakan:
- Accuracy  
- Precision  
- Recall  
- F1-score  

## 📁 Hasil evaluasi:

data/eval/prediction_metrics.csv

---

## ▶️ Instalasi dan Dependensi

1. Jalankan di Google Colab **atau** lokal dengan Python ≥ 3.8
2. Instal library yang dibutuhkan:

```bash
pip install -r requirements.txt
```

---

## Panduan Menjalankan Pipeline

1. **Tahap 1 – Scraping dan Cleaning**
   - Jalankan `01_scraping.ipynb` untuk mengonversi PDF putusan ke teks dan membersihkannya.

2. **Tahap 2 – Case Representation**
   - Jalankan `02_representation.ipynb` untuk mengekstrak metadata, pasal, ringkasan fakta, dll, lalu simpan ke `cases.csv`.

3. **Tahap 3 – Retrieval**
   - Jalankan `03_retrieval.ipynb` untuk menghasilkan fungsi `retrieve()` dengan TF-IDF atau BERT.
   - Simpan query ke `eval/queries.json`

4. **Tahap 4 – Predict / Solution Reuse**
   - Jalankan `04_predict.ipynb` untuk memprediksi amar putusan dari top-k kasus serupa.
   - Hasil disimpan di `results/predictions.csv`

5. **Tahap 5 – Evaluasi Sistem**
   - Jalankan `05_evaluation.ipynb` untuk menghitung accuracy, precision, recall, f1-score dan simpan hasil ke `eval/`

---

## Dataset

- Dokumen diperoleh dari: [Direktori Putusan MA RI](https://putusan3.mahkamahagung.go.id)
- Domain: **Pidana - Pemalsuan Dokumen**
- Format awal: PDF → Teks → Representasi CSV

---

## Contoh File

- `queries.json` berisi daftar query kasus baru
- `ground_truth.csv` berisi label manual untuk evaluasi akurasi prediksi
- `prediction_metrics.csv` berisi nilai evaluasi (accuracy, precision, etc.)

---

## 📌 Key Insight

- Pendekatan **Case-Based Reasoning** efektif untuk domain hukum berbasis preseden  
- Similarity antar kasus menjadi faktor utama dalam prediksi  
- Representasi fitur sangat mempengaruhi performa sistem  

---

## 👤 Author & Contributors

| Name | Role |
|------|------|
| **Muhammad Wildan Nabila** | Lead Developer |
| Irawana Juwita | Contributor |

---

## 🎓 Academic Information

| Attribute | Detail |
|----------|--------|
| **Course** | Computational Reasoning |
| **Program** | Informatics |
| **Institution** | Universitas Muhammadiyah Malang |
| **Year** | 2024 / 2025 |

---

## Lisensi

Proyek ini ditujukan untuk keperluan akademik dan evaluasi tugas UAS.

---

> Deadline pengumpulan: **Sabtu, 28 Juni 2025 - 23:59 WIB** melalui LMS
