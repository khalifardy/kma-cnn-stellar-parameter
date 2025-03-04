# Kerangka Penelitian untuk Optimasi Hyperparameter CNN dengan KMA untuk Analisis Spektral Bintang

## 1. Pendahuluan dan Landasan Teoretis

### 1.1 Pengembangan Formulasi Teoretis KMA
- Formulasikan secara matematis mekanisme KMA secara komprehensif
- Kembangkan model teoretis tentang konvergensi KMA dalam ruang hyperparameter
- Formulasikan teorema tentang hubungan mlipir rate dengan dimensionalitas ruang pencarian

### 1.2 Integrasi Teori Astrofisika dan CNN
- Analisis hubungan antara karakteristik spektrum bintang dan arsitektur CNN yang optimal
- Formulasikan bagaimana kompleksitas garis absorpsi dan emisi spektral berkorelasi dengan kebutuhan kedalaman dan lebar jaringan
- Kembangkan model teoretis tentang bagaimana parameter stellar terwakili dalam fitur CNN

### 1.3 Analisis Teoretis Kompleksitas dan Konvergensi
- Lakukan analisis kompleksitas waktu dan ruang KMA dibandingkan algoritma optimasi lain
- Kembangkan bukti matematis tentang konvergensi KMA untuk berbagai ukuran populasi
- Formulasikan jaminan teoretis tentang jarak maksimum dari solusi optimal untuk KMA

## 2. Perluasan Dataset dan Eksperimen

### 2.1 Pengumpulan dan Integrasi Dataset
- Kumpulkan data spektral dari minimal 3 sumber berbeda: APOGEE DR17, LAMOST, GALAH
- Lakukan standarisasi dan validasi silang untuk memastikan kompatibilitas antar dataset
- Buat subset yang berfokus pada rentang parameter stellar yang ekstrem

### 2.2 Perluasan Algoritma Pembanding
- Implementasikan minimal 5 algoritma optimasi state-of-the-art:
  - Bayesian Optimization
  - Population-based Training
  - Particle Swarm Optimization
  - SHADE dan LSHADE-cnEpSin
  - Neural Architecture Search

### 2.3 Desain Eksperimen Komprehensif
- Rancang validasi silang k-fold (k=10) untuk semua eksperimen
- Implementasikan uji statistik formal (Wilcoxon signed-rank test, Friedman test dengan post-hoc Nemenyi)
- Rancang eksperimen untuk mengevaluasi pengaruh setiap hyperparameter secara independen dan interaksinya

## 3. Modifikasi dan Peningkatan KMA

### 3.1 Pengembangan KMA Adaptif
- Kembangkan varian KMA dengan mlipir rate yang adaptif berdasarkan kualitas solusi
- Implementasikan mekanisme memori untuk menghindari re-evaluasi area yang sudah dieksplorasi
- Desain mekanisme paralel untuk populasi multiple islands

### 3.2 Pengembangan Fungsi Fitness Multi-objektif
- Desain fungsi fitness yang memperhitungkan akurasi, kompleksitas model, dan stabilitas prediksi
- Implementasikan regularisasi untuk mencegah overfitting dalam proses optimasi
- Kembangkan metrik fitness yang memprioritaskan performa pada rentang parameter ekstrem

### 3.3 Integrasi Transfer Learning dalam Optimasi
- Kembangkan metode untuk mentransfer pengetahuan hyperparameter dari satu parameter stellar ke parameter lainnya
- Implementasikan warm-start KMA berdasarkan optimasi sebelumnya
- Desain model meta-learning untuk mempercepat optimasi pada data baru

## 4. Analisis Mendalam

### 4.1 Analisis Sensitivitas Hyperparameter
- Lakukan analisis sensitivitas global dengan metode Sobol untuk mengidentifikasi hyperparameter paling berpengaruh
- Buat pemetaan hubungan antar hyperparameter dengan performa model
- Analisis dampak hyperparameter spesifik terhadap performa prediksi masing-masing parameter stellar

### 4.2 Analisis Performa pada Kasus Ekstrem
- Fokuskan analisis pada performa model pada nilai parameter stellar ekstrem
- Identifikasi pola kesalahan sistematis dan hubungannya dengan hyperparameter
- Kembangkan model teoretis untuk menjelaskan tantangan pada nilai ekstrem

### 4.3 Analisis Komputasional dan Skalabilitas
- Evaluasi skalabilitas KMA untuk dimensi hyperparameter yang sangat tinggi (hingga 100+ dimensi)
- Bandingkan efisiensi komputasional KMA dengan metode lain untuk ukuran dataset yang bervariasi
- Analisis dampak paralelisasi terhadap kualitas solusi dan waktu komputasi

## 5. Validasi dan Penerapan

### 5.1 Validasi Astrofisika
- Validasi prediksi parameter stellar dengan pengukuran independen (misalnya pengukuran optik)
- Analisis konsistensi fisik parameter stellar yang diprediksi
- Evaluasi dampak peningkatan akurasi terhadap pemahaman evolusi bintang

### 5.2 Aplikasi pada Masalah Astrofisika Terkait
- Terapkan model teroptimisasi untuk klasifikasi variabilitas bintang
- Gunakan model untuk mendeteksi bintang dengan abnormalitas komposisi kimiawi
- Evaluasi model untuk deteksi bintang kembar atau sistem multi-bintang

### 5.3 Generalisasi ke Domain Lain
- Terapkan KMA untuk optimasi hyperparameter pada domain lain (misalnya spektroskopi molekuler)
- Evaluasi performa KMA untuk masalah klasifikasi dan segmentasi citra astronomi
- Analisis kemampuan transfer KMA ke arsitektur DL lain seperti RNN, Transformer

## 6. Penulisan dan Diseminasi

### 6.1 Penulisan Ilmiah
- Struktur artikel dengan penekanan pada kontribusi teoretis dan metodologis
- Fokuskan pada analisis mendalam dibanding laporan hasil yang deskriptif
- Kembangkan visualisasi yang efektif untuk menunjukkan perbandingan performa

### 6.2 Repositori Kode dan Dataset
- Buat repositori publik dengan implementasi KMA dan algoritma pembanding
- Sediakan dataset yang digunakan dan notebook untuk reproduksi hasil
- Dokumentasikan dengan baik API untuk implementasi KMA

### 6.3 Identifikasi Jurnal Target
- Identifikasi jurnal Scopus Q1 yang cocok seperti:
  - Monthly Notices of the Royal Astronomical Society
  - Astronomy & Astrophysics
  - IEEE Transactions on Neural Networks and Learning Systems
  - Pattern Recognition
  - Knowledge-Based Systems

## Timeline Penelitian

1. **Bulan 1-2**: Pengembangan teoretis dan studi literatur
2. **Bulan 3-4**: Pengumpulan dan preprocessing dataset
3. **Bulan 5-6**: Implementasi algoritma dan rancangan eksperimen
4. **Bulan 7-8**: Pelaksanaan eksperimen dan analisis awal
5. **Bulan 9-10**: Analisis mendalam dan penyempurnaan metode
6. **Bulan 11-12**: Penulisan artikel dan persiapan diseminasi