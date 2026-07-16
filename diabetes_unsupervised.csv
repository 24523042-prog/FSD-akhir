# Klasifikasi & Segmentasi Diabetes — Tugas Akhir Fundamental Sains Data

Repository ini berisi dua studi kasus analisis data machine learning terkait diabetes:

1. **Supervised Learning (Klasifikasi)** — `supervised_learning.ipynb`
   Memprediksi apakah seorang pasien menderita diabetes berdasarkan data pemeriksaan medis.
2. **Unsupervised Learning (Clustering)** — `unsupervised_learning.ipynb`
   Mengelompokkan pasien ke dalam beberapa segmen berdasarkan profil kesehatan (kolesterol, gula
   darah, tekanan darah, dan ukuran tubuh), tanpa menggunakan label.

## Deskripsi Singkat

| | Studi Kasus 1 (Supervised) | Studi Kasus 2 (Unsupervised) |
|---|---|---|
| Tipe masalah | Klasifikasi biner | Clustering |
| Dataset | Pima Indians Diabetes Dataset | Diabetes Clinical Dataset (Vanderbilt Univ.) |
| Jumlah data | 768 baris, 9 kolom | 403 baris, 19 kolom |
| Target | `Outcome` (1 = diabetes, 0 = tidak) | Tidak ada (unsupervised) |
| Algoritma | Logistic Regression, Decision Tree, Random Forest, SVM, Naive Bayes | K-Means, Hierarchical Clustering, DBSCAN, PCA |
| Model terbaik | Random Forest | K-Means |

## Sumber Dataset

- **Supervised Learning:** [Pima Indians Diabetes Database — Kaggle](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database)
  (bersumber dari National Institute of Diabetes and Digestive and Kidney Diseases / UCI ML Repository).
- **Unsupervised Learning:** Diabetes Dataset dari Dr. John Schorling, Universitas Virginia, yang
  dipublikasikan melalui Vanderbilt University Department of Biostatistics dan juga tersedia sebagai
  open dataset di berbagai platform (mis. Kaggle).

File dataset mentah disertakan pada folder `data/`:
- `data/diabetes_supervised.csv`
- `data/diabetes_unsupervised.csv`

## Struktur Repository

```
.
├── README.md
├── requirements.txt
├── supervised_learning.ipynb        # Notebook studi kasus 1 (klasifikasi)
├── unsupervised_learning.ipynb      # Notebook studi kasus 2 (clustering)
├── app.py                           # Antarmuka Gradio untuk model supervised
├── data/
│   ├── diabetes_supervised.csv
│   └── diabetes_unsupervised.csv
└── model/                           # Dibuat otomatis setelah menjalankan notebook 1
    ├── diabetes_model.pkl
    ├── diabetes_scaler.pkl
    └── diabetes_features.pkl
```

## Cara Menjalankan

### 1. Persiapan environment

```bash
python -m venv venv
source venv/bin/activate      # Windows: venv\Scripts\activate
pip install -r requirements.txt
```

### 2. Menjalankan notebook

Buka dan jalankan notebook secara berurutan menggunakan Jupyter Notebook / JupyterLab / Google Colab:

```bash
jupyter notebook supervised_learning.ipynb
jupyter notebook unsupervised_learning.ipynb
```

> **Penting:** Jalankan `supervised_learning.ipynb` terlebih dahulu secara lengkap (Run All), karena
> notebook ini akan menyimpan model terlatih (`model/diabetes_model.pkl`, `diabetes_scaler.pkl`,
> `diabetes_features.pkl`) yang dibutuhkan oleh `app.py`.

### 3. Menjalankan aplikasi Gradio

Setelah `supervised_learning.ipynb` dijalankan dan folder `model/` terisi, jalankan:

```bash
python app.py
```

Aplikasi akan berjalan secara lokal (biasanya pada `http://127.0.0.1:7860`) dan menampilkan form input
untuk memasukkan data pemeriksaan pasien, lalu menghasilkan prediksi risiko diabetes beserta
probabilitasnya.

## Ringkasan Hasil

- **Studi Kasus 1 (Supervised):** Model **Random Forest** terpilih sebagai model terbaik dengan
  akurasi sekitar 86% dan F1-score sekitar 0.80 pada kelas diabetes. Fitur `Glucose`, `BMI`, dan `Age`
  merupakan fitur paling berpengaruh terhadap prediksi.
- **Studi Kasus 2 (Unsupervised):** K-Means berhasil mengelompokkan pasien menjadi beberapa cluster
  berdasarkan profil gula darah, kolesterol, dan ukuran tubuh, mengungkap kelompok pasien dengan
  profil risiko metabolik yang berbeda-beda.

Detail lengkap proses analisis, visualisasi, dan interpretasi dapat dilihat pada masing-masing
notebook.

## Referensi

- Pima Indians Diabetes Dataset, UCI Machine Learning Repository / Kaggle.
- Diabetes Dataset, Vanderbilt University Department of Biostatistics.
- Dokumentasi scikit-learn: https://scikit-learn.org/
- Dokumentasi Gradio: https://www.gradio.app/
