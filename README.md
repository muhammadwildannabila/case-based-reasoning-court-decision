
# A. Case-Based Reasoning untuk Analisis Putusan Pengadilan

Proyek ini merupakan implementasi dari **Tugas UAS Mata Kuliah Penalaran Komputer** Semester Genap 2024/2025 di Fakultas Teknik Informatika UMM. Sistem ini dirancang untuk melakukan **analisis dan prediksi putusan pengadilan** menggunakan pendekatan **Case-Based Reasoning (CBR)**.

---

## B. Struktur Direktori

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

## C. Instalasi dan Dependensi

1. Jalankan di Google Colab **atau** lokal dengan Python ≥ 3.8
2. Instal library yang dibutuhkan:

```bash
pip install -r requirements.txt
```

---

## D. Panduan Menjalankan Pipeline

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

## E. Dataset

- Dokumen diperoleh dari: [Direktori Putusan MA RI](https://putusan3.mahkamahagung.go.id)
- Domain: **Pidana - Pemalsuan Dokumen**
- Format awal: PDF → Teks → Representasi CSV

---

## F. Contoh File

- `queries.json` berisi daftar query kasus baru
- `ground_truth.csv` berisi label manual untuk evaluasi akurasi prediksi
- `prediction_metrics.csv` berisi nilai evaluasi (accuracy, precision, etc.)

---

## G. Anggota Kelompok

- **Nama: Muhammad Wildan Nabila**
- **NIM: 202210370311252**
- **Kelas: Penalaran Komputer A**
- **Nama: Irawana Juwita** 
- **NIM: 202210370311446**
- **Kelas: Penalaran Komputer A**

---

## H. Lisensi

Proyek ini ditujukan untuk keperluan akademik dan evaluasi tugas UAS.

---

> Deadline pengumpulan: **Sabtu, 28 Juni 2025 - 23:59 WIB** melalui LMS
