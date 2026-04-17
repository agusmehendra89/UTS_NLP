Proyek NLP - Analisis Sentimen Ulasan Instagram

Proyek ini berisi implementasi sederhana Natural Language Processing (NLP) untuk klasifikasi sentimen teks berbahasa Indonesia menjadi Positif**, Negatif, dan Netral.

**Fitur Utama**
- Preprocessing teks: cleaning, lowercase, stopword removal, dan stemming
- Representasi teks:
  - Bag-of-Words (BoW)
  - TF-IDF
- Model klasifikasi:
  - Logistic Regression
- Visualisasi:
  - Distribusi label
  - Word Cloud
- Dibuat dalam format Jupyter Notebook (`.ipynb`) dan bisa dijalankan ulang

**Struktur File**
```text
project/
├── Untitled0.ipynb
├── Review Instagram.csv
└── README.md
```

**Persiapan**
Sebelum menjalankan notebook, pastikan sudah menyiapkan:

1. Python 3.8+
2. Jupyter Notebook atau Google Colab
3. File dataset `Review Instagram.csv`

---

** Cara Menjalankan di Google Colab**
Notebook ini paling mudah dijalankan di Google Colab karena sudah memakai fitur upload file.

#Langkah-langkah:
1. Buka file notebook `Untitled0.ipynb` di Google Colab.
2. Jalankan cell instalasi library:
   - `Sastrawi`
   - library pendukung lain seperti `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`, dan `wordcloud`
3. Saat muncul perintah upload file, unggah dataset `Review Instagram.csv`.
4. Pastikan dataset berhasil terbaca dan jumlah data tampil di output.
5. Jalankan seluruh cell secara berurutan dari atas ke bawah.
6. Tunggu proses preprocessing selesai, karena stemming biasanya memerlukan waktu cukup lama.
7. Setelah selesai, lihat hasil:
   - visualisasi distribusi sentimen
   - word cloud
   - perbandingan akurasi BoW dan TF-IDF

---

** Cara Menjalankan di Lokal**
Kalau ingin dijalankan di laptop/PC sendiri:

 1. Install library
Jalankan perintah berikut di terminal / command prompt:
```bash
pip install pandas numpy matplotlib seaborn wordcloud nltk scikit-learn Sastrawi notebook
```

 2. Siapkan dataset
Letakkan file `Review Instagram.csv` di folder yang sama dengan notebook.

 3. Buka notebook
Jalankan:
```bash
jupyter notebook
```

Lalu buka file `Untitled0.ipynb`.

4. Ubah bagian upload file
Di notebook, bagian ini:
```python
from google.colab import files
uploaded = files.upload()
```

digunakan untuk Google Colab.  
Kalau dijalankan secara lokal, bagian tersebut bisa diganti menjadi:

```python
import pandas as pd

df = pd.read_csv("Review Instagram.csv")
```

 5. Jalankan semua cell
Jalankan notebook dari atas ke bawah sampai selesai.

**Catatan Penting**
- Dataset minimal sebaiknya berisi 500 data agar hasil lebih representatif.
- Pastikan nama kolom dataset sesuai. Pada notebook ini kolom disesuaikan otomatis menjadi:
  - `user_name`
  - `text`
  - `sentiment_label`
- Jika struktur CSV berbeda, sesuaikan bagian berikut:
```python
df.columns = ['user_name', 'text', 'sentiment_label']
```

**Output yang Dihasilkan**
Setelah notebook selesai dijalankan, proyek ini akan menghasilkan:
- data yang sudah dibersihkan (`text_clean`)
- visualisasi sentimen
- word cloud
- model klasifikasi sentimen
- perbandingan performa:
  - Bag-of-Words
  - TF-IDF

---

**Hasil Perbandingan**
Notebook ini membandingkan dua metode representasi teks:
- Bag-of-Words
- TF-IDF

Hasil evaluasi ditampilkan dalam bentuk:
- akurasi
- classification report


**Troubleshooting**
 1. Error saat import Sastrawi
Pastikan library sudah terpasang:
```bash
pip install Sastrawi
```

 2. Error file CSV tidak ditemukan
Pastikan file dataset ada di folder yang sama dengan notebook atau unggah ulang di Colab.

3. Error nama kolom tidak cocok
Cek isi dataset dan ubah bagian:
```python
kolom_teks = 'text'
kolom_label = 'sentiment_label'
```
sesuai nama kolom asli di CSV.

 4. Proses terlalu lama
Proses stemming dan preprocessing dapat memakan waktu, terutama jika dataset cukup besar.

---

**Referensi Library**
- pandas
- numpy
- matplotlib
- seaborn
- wordcloud
- nltk
- scikit-learn
- Sastrawi

**Lisensi**
Proyek ini dibuat untuk keperluan pembelajaran dan tugas kuliah.
