# Vidio-App-Review-Scraping-Sentiment-Analysis
# Play Store Review Scraper & Sentiment Analysis: Vidio Streaming Application

Projek ini berfokus pada pengambilan data (*web scraping*) ulasan pengguna aplikasi streaming **Vidio** di Google Play Store dan dilanjutkan dengan implementasi pemrosesan bahasa alami (*Natural Language Processing*) untuk menganalisis sentimen pengguna. 

Tujuan utama projek ini adalah mengekstrak opini publik, mendeteksi masalah teknis utama dari ulasan negatif, serta melatih model Machine Learning/Deep Learning untuk mengklasifikasikan sentimen ulasan secara otomatis.

## 📁 Struktur Repositori

- `data/` : Berisi data hasil scraping ulasan aplikasi Vidio dalam format Excel.
- `notebooks/` : Berisi langkah-langkah eksperimen kode program dari scraping hingga pelatihan model.
  - `scraping_apk_vidio.ipynb` : Proses ekstraksi data menggunakan Play Store Scraper API.
  - `Pelatihan_Model_analisis_Sentimen_Elsa_...ipynb` : Proses preprocessing teks, ekstraksi fitur, pemodelan sentimen, dan evaluasi.
- `requirements.txt` : Daftar pustaka (library) Python beserta versi yang digunakan.

## 🛠️ Teknologi dan Pustaka (Tech Stack)

- **Bahasa Pemrograman:** Python
- **Environment:** Jupyter Notebook
- **Libraries & Tools:**
  - `google-play-scraper` (Pengambilan data ulasan)
  - `pandas` & `numpy` (Manipulasi dan analisis data)
  - `scikit-learn` / `Keras` / `TensorFlow` *(Sesuaikan dengan algoritma yang kamu gunakan)*
  - `nltk` / `Sastrawi` (Pembersihan teks & tokenisasi bahasa Indonesia)
  - `matplotlib` & `seaborn` (Visualisasi data)

## 🔄 Alur Kerja Projek (Workflow)

### 1. Data Scraping
Proses ekstraksi data ulasan langsung dari Google Play Store. Data yang berhasil dikumpulkan disimpan ke dalam berkas `vidio_reviews.xlsx`. Informasi yang diambil meliputi identitas pengguna, rating bintang, isi ulasan, serta waktu pemberian ulasan.

### 2. Text Preprocessing
Ulasan teks bahasa Indonesia bersifat sangat kasual dan tidak baku, sehingga perlu dibersihkan melalui tahap:
- **Case Folding:** Mengubah semua huruf menjadi huruf kecil.
- **Cleansing:** Menghapus angka, tanda baca, tautan, emoji, dan spasi berlebih.
- **Stopwords Removal:** Menghapus kata-kata konjungsi atau kata umum yang tidak membawa makna sentimen (seperti *yang, di, dan, itu*).
- **Stemming:** Mengembalikan kata berimbuhan menjadi kata dasar menggunakan library Sastrawi.

### 3. Ekstraksi Fitur & Pembagian Data
Teks diubah menjadi representasi angka menggunakan metode seperti **TF-IDF Vectorizer** atau **Word Embedding**. Selanjutnya, data dibagi menjadi *Training Set* dan *Testing Set*.

### 4. Pelatihan Model & Evaluasi
Model dilatih menggunakan algoritma klasifikasi untuk mengenali sentimen positif, netral, maupun negatif. Performa model dievaluasi menggunakan metrik seperti *Accuracy, Precision, Recall,* dan *F1-Score*.

## 🚀 Cara Menjalankan Projek

1. Kloning repositori ini:
```bash
   git clone [https://github.com/username-kamu/Vidio-App-Review-Scraping-Sentiment-Analysis.git](https://github.com/username-kamu/Vidio-App-Review-Scraping-Sentiment-Analysis.git)
