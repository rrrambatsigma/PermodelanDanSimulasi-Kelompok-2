
---

# Analisis Regresi Determinan Sosial Ekonomi terhadap Indeks Pembangunan Manusia (IPM) di Indonesia

Repository ini berisi proyek tugas akhir mata kuliah **Permodelan dan Simulasi** yang bertujuan untuk menganalisis pengaruh faktor sosial ekonomi terhadap **Indeks Pembangunan Manusia (IPM)** kabupaten/kota di Indonesia menggunakan pendekatan **regresi linier berganda**. Penelitian ini juga membandingkan kinerja model antara data mentah dan data yang telah melalui proses transformasi logaritma serta standarisasi.

---

## Latar Belakang

IPM merupakan indikator utama kualitas pembangunan manusia yang mencakup dimensi kesehatan, pendidikan, dan standar hidup layak. Namun, capaian IPM di tingkat daerah tidak hanya dipengaruhi oleh komponen penyusunnya, melainkan juga oleh faktor struktural seperti tingkat kemahalan konstruksi, pertumbuhan ekonomi, kemiskinan, ketahanan pangan, serta kondisi sosial demografis. Oleh karena itu, penelitian ini berfokus untuk mengkaji pengaruh beberapa variabel sosial ekonomi terhadap IPM secara simultan dan menguji keandalan model regresi yang digunakan.

---

## Tujuan Penelitian

1. Membandingkan performa model regresi antara data mentah dan data hasil preprocessing.
2. Menganalisis pengaruh Indeks Kemahalan Konstruksi (IKK) terhadap IPM.
3. Menganalisis pengaruh Produk Domestik Regional Bruto (PDRB) terhadap IPM.
4. Menganalisis pengaruh persentase penduduk miskin terhadap IPM.
5. Menganalisis pengaruh prevalensi ketidakcukupan konsumsi pangan terhadap IPM.
6. Menganalisis pengaruh proporsi perempuan melahirkan anak pertama di bawah usia 20 tahun terhadap IPM.
7. Menganalisis pengaruh seluruh variabel independen secara simultan terhadap IPM.

---

## Variabel Penelitian

| Variabel                  | Keterangan                                              |
| ------------------------- | ------------------------------------------------------- |
| IPM                       | Indeks Pembangunan Manusia                              |
| IKK                       | Indeks Kemahalan Konstruksi                             |
| PDRB                      | Produk Domestik Regional Bruto                          |
| P0                        | Persentase Penduduk Miskin                              |
| PoU                       | Prevalensi Ketidakcukupan Konsumsi Pangan               |
| Proporsi Kelahiran Remaja | Persentase perempuan melahirkan anak pertama < 20 tahun |

---

## Metodologi

Penelitian ini menggunakan pendekatan **regresi linier berganda** dengan beberapa tahapan utama:

1. **Exploratory Data Analysis (EDA)**
   Melakukan analisis distribusi data, boxplot, dan scatter plot untuk mengidentifikasi skewness, outlier, serta pola hubungan antar variabel.

2. **Preprocessing Data**

   * Transformasi logaritma untuk variabel yang memiliki distribusi sangat menceng.
   * Standarisasi menggunakan z-score untuk menyeragamkan skala variabel.

3. **Pemodelan Regresi OLS**
   Regresi linier berganda dilakukan dengan robust standard error tipe HC3 untuk mengatasi heteroskedastisitas.

4. **Uji Asumsi Klasik**

   * Multikolinearitas: Variance Inflation Factor (VIF)
   * Normalitas residual: QQ-Plot dan Jarque-Bera
   * Heteroskedastisitas: Breusch–Pagan
   * Autokorelasi: Durbin–Watson dan ACF
   * Linearitas: Ramsey RESET

5. **Feature Pruning**
   Variabel yang tidak signifikan secara statistik dieliminasi untuk meningkatkan stabilitas model.

6. **Inferensi dan Evaluasi Model**
   Model diuji pada data tahun 2022 dengan metrik evaluasi MAE, RMSE, dan R².

---

## Hasil Singkat

* Model awal menunjukkan R² sekitar 0.72 namun melanggar beberapa asumsi klasik.
* Setelah preprocessing dan feature pruning, model menjadi lebih stabil dan valid secara statistik.
* Variabel yang berpengaruh signifikan terhadap IPM adalah IKK, PDRB, persentase penduduk miskin, dan proporsi kelahiran remaja.
* Hasil simulasi pada data 2022 menunjukkan MAE sekitar 2.7 dan RMSE sekitar 3.5, menandakan performa prediksi yang cukup baik.

---

## Cara Menjalankan Proyek

1. Clone repository:

   ```bash
   git clone https://github.com/rrrambatsigma/PermodelanDanSimulasi-Kelompok-2
   ```

2. Install dependensi:

   ```bash
   pip install -r requirements.txt
   ```

3. Jalankan Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

4. Buka notebook pada folder `notebooks/` secara berurutan.

---

## Anggota Kelompok

* Dhea Meidiyana Windawati (L0224004)
* Jonnathan Azarel Gunawan (L0224005)
* Prayuda Afifan Handoyo (L0224008)
* Rambat Ungu Aryati (L0224010)
* Farrel Naufal Maghribi (L0224031)

Program Studi Sains Data
Universitas Sebelas Maret – 2025
