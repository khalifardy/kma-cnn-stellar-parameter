# Kerangka Detil Fase 1: Pengembangan Teoretis dan Pengumpulan Data

## 1. Pengembangan Teoretis dan Studi Literatur (Bulan 1-2)

### 1.1 Landasan Matematika KMA

#### 1.1.1 Formulasi Matematis Komprehensif
- Definisikan ruang pencarian hyperparameter $H = \{h_1, h_2, ..., h_n\}$ di mana setiap $h_i$ adalah hyperparameter dengan domain tertentu
- Formulasikan representasi matematis untuk tiga kelompok individu dalam KMA: jantan besar, betina, dan jantan kecil
- Kembangkan notasi formal untuk gerakan HILE, MIME, dan LIHE

#### 1.1.2 Model Konvergensi KMA
- Analisis konvergensi probabilistik KMA menggunakan rantai Markov
- Identifikasi kondisi yang menjamin konvergensi ke solusi optimal global
- Formulasikan teorema batas konvergensi untuk KMA berdasarkan jumlah iterasi

#### 1.1.3 Teorema Mlipir Rate
- Kembangkan teorema yang menghubungkan mlipir rate optimal dengan dimensionalitas ruang pencarian
- Formulasikan bukti matematis untuk pengaruh mlipir rate terhadap trade-off eksplorasi-eksploitasi
- Definisikan metrik kuantitatif untuk mengukur efektivitas mlipir rate pada berbagai lanskap fungsi

### 1.2 Integrasi Teori Spektroskopi dan Deep Learning

#### 1.2.1 Analisis Spektral-CNN
- Kembangkan model teoretis mengenai hubungan antara karakteristik garis absorpsi spektrum dan operasi konvolusi dalam CNN
- Formulasikan representasi matematis tentang bagaimana CNN mengekstrak informasi parameter stellar dari pola spektral
- Analisis teoretis tentang pengaruh resolusi spektral terhadap kebutuhan arsitektur CNN

#### 1.2.2 Model Relasi Hyperparameter-Parameter Stellar
- Kembangkan model matematika tentang hubungan antara hyperparameter CNN dengan akurasi prediksi untuk setiap parameter stellar
- Formulasikan relasi teoretis antara ukuran kernel dan kemampuan CNN mendeteksi fitur spektral pada berbagai skala
- Analisis teoretis tentang pengaruh fungsi aktivasi terhadap non-linearitas dalam prediksi parameter stellar

#### 1.2.3 Formulasi Bias Sistematis
- Kembangkan model teoretis untuk bias sistematis pada rentang ekstrem parameter stellar
- Formulasikan pendekatan matematis untuk mengurangi bias pada prediksi nilai ekstrem
- Analisis teoretis tentang hubungan antara distribusi data training dan bias prediksi

### 1.3 Analisis Kompleksitas dan Kajian Algoritma Pembanding

#### 1.3.1 Analisis Kompleksitas KMA
- Evaluasi kompleksitas waktu dan ruang KMA sebagai fungsi dari ukuran populasi, dimensi, dan jumlah iterasi
- Bandingkan kompleksitas teoretis KMA dengan algoritma optimasi lain
- Formulasikan batas kompleksitas asimtotik untuk KMA pada dimensi tinggi

#### 1.3.2 Kajian Algoritma Pembanding
- Analisis teoretis dari Bayesian Optimization untuk optimasi hyperparameter
- Kajian mendalam mengenai Population-based Training dan keunggulannya
- Evaluasi kritis tentang Neural Architecture Search dan aplikasinya untuk data spektral

#### 1.3.3 Pengembangan Framework Perbandingan Teoretis
- Kembangkan kerangka teoretis untuk membandingkan algoritma metaheuristik
- Formulasikan metrik kuantitatif untuk evaluasi algoritma optimasi pada ruang hyperparameter
- Desain taksonomi karakteristik lanskap fungsi hyperparameter

### 1.4 Studi Literatur Komprehensif

#### 1.4.1 Review Sistematis Analisis Spektral Bintang dengan Deep Learning
- Analisis sistematis dari 50+ paper terkait aplikasi CNN untuk spektroskopi bintang
- Klasifikasi metodologi yang digunakan berdasarkan parameter stellar yang diprediksi
- Identifikasi gap penelitian dalam pendekatan optimasi hyperparameter

#### 1.4.2 Review Metode Optimasi Hyperparameter untuk Deep Learning
- Analisis kritis dari 30+ paper terkait optimasi hyperparameter untuk CNN
- Evaluasi pendekatan optimasi untuk arsitektur deep learning lainnya
- Identifikasi tren dan arah penelitian terkini dalam optimasi hyperparameter

#### 1.4.3 Review Aplikasi Algoritma Metaheuristik dalam Astrofisika
- Kajian sistematis dari 20+ paper tentang aplikasi algoritma metaheuristik dalam astrofisika
- Analisis kritis peran algoritma inspirasi biologis dalam analisis data astronomi
- Identifikasi peluang aplikasi KMA untuk masalah astrofisika lainnya

## 2. Pengumpulan dan Preprocessing Dataset (Bulan 3-4)

### 2.1 Identifikasi dan Akuisisi Dataset

#### 2.1.1 Pengumpulan Dataset APOGEE DR17
- Akses dan unduh data spektral APOGEE DR17 dari portal SDSS
- Seleksi subset data berdasarkan kualitas spektral (S/N > 100)
- Akuisisi parameter stellar referensi dari katalog ASPCAP

#### 2.1.2 Pengumpulan Dataset LAMOST
- Akses dan unduh data spektral LAMOST DR7 dari portal resmi
- Seleksi spektrum bintang dengan rentang parameter stellar yang luas
- Akuisisi parameter stellar referensi dari katalog LAMOST Stellar Parameter Pipeline

#### 2.1.3 Pengumpulan Dataset GALAH
- Akses dan unduh data spektral GALAH DR3 dari arsip digital
- Seleksi spektrum dengan kualitas tinggi dan parameter stellar yang valid
- Akuisisi parameter stellar referensi dan flag kualitas terkait

#### 2.1.4 Pengumpulan Dataset Ekstrem
- Identifikasi dataset dari survei spektroskopi khusus bintang ekstrem (mis. metal-poor stars)
- Unduh spektrum bintang dengan parameter ekstrem dari katalog khusus
- Akuisisi parameter stellar dari literatur untuk validasi silang

### 2.2 Preprocessing dan Standardisasi

#### 2.2.1 Standarisasi Resolusi Spektral
- Pengembangan algoritma rebinning spektrum ke resolusi yang seragam
- Implementasi interpolasi spektral untuk menyesuaikan sampling antar survei
- Validasi kualitas resampling dengan analisis residual

#### 2.2.2 Normalisasi Spektrum
- Implementasi teknik normalisasi spektrum berbasis segmentasi
- Pengembangan algoritma normalisasi kontinuum berbasis quantile
- Evaluasi metode normalisasi dengan analisis propagasi error

#### 2.2.3 Manajemen Missing Values dan Outliers
- Pengembangan algoritma deteksi dan penanganan piksel yang rusak (bad pixels)
- Implementasi teknik interpolasi untuk segmen spektrum yang hilang
- Analisis statistik untuk deteksi dan penanganan outliers

#### 2.2.4 Augmentasi Data
- Pengembangan teknik augmentasi data dengan menambahkan noise artifisial
- Implementasi augmentasi spektrum dengan variasi dalam normalisasi kontinuum
- Simulasi variasi dalam resolusi spektral untuk meningkatkan ketahanan model

### 2.3 Penyiapan Dataset untuk Eksperimen

#### 2.3.1 Stratifikasi Dataset
- Implementasi stratified sampling berdasarkan distribusi parameter stellar
- Pengembangan strategi pembagian data untuk area parameter stellar yang jarang
- Analisis representativitas dataset setelah stratifikasi

#### 2.3.2 Validasi Silang
- Perancangan K-fold cross-validation (K=10) dengan stratifikasi
- Implementasi nested cross-validation untuk optimasi hyperparameter
- Pengembangan strategi validasi untuk menghindari bias pada data ekstrem

#### 2.3.3 Standarisasi Parameter Stellar
- Pengembangan teknik normalisasi untuk setiap parameter stellar
- Implementasi transformasi khusus untuk parameter dengan distribusi non-Gaussian
- Validasi kualitas standarisasi dengan analisis statistik

### 2.4 Analisis Eksploratori Data

#### 2.4.1 Analisis Distribusi Parameter Stellar
- Analisis univariat untuk setiap parameter stellar pada setiap dataset
- Analisis bivariat untuk mengidentifikasi korelasi antar parameter
- Visualisasi distribusi multi-dimensi dengan teknik dimensionality reduction

#### 2.4.2 Analisis Karakteristik Spektral
- Analisis Principal Component untuk mengidentifikasi mode variasi utama spektrum
- Pengembangan metrik kuantitatif untuk mengukur kekayaan fitur spektral
- Investigasi hubungan antara karakteristik spektral dan parameter stellar

#### 2.4.3 Analisis Gap dan Bias
- Identifikasi rentang parameter stellar dengan representasi yang rendah
- Analisis kemungkinan bias sistematis dalam dataset referensi
- Pengembangan strategi mitigasi untuk gap dan bias yang teridentifikasi

## 3. Penulisan Tinjauan Teoritis dan Dokumentasi Dataset

### 3.1 Penulisan Draft Tinjauan Teoretis
- Sintesis pengembangan teoretis dalam dokumen komprehensif
- Pengembangan visualisasi konseptual untuk ilustrasi formulasi matematika
- Persiapan bagian metodologi paper untuk publikasi

### 3.2 Dokumentasi Dataset
- Pengembangan dokumentasi ekstensif untuk dataset yang telah dipreprocessing
- Pembuatan visualisasi distribusi dan karakteristik dataset
- Persiapan dataset dan metadata untuk repositori publik