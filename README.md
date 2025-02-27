# KMA-CNN untuk Estimasi Parameter Stellar

[![Lisensi: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Kerangka kerja komprehensif untuk mengoptimalkan hyperparameter CNN menggunakan Algoritma Komodo Mlipir (KMA) untuk estimasi parameter stellar dari data spektral.

## Gambaran Umum

Repositori ini mengimplementasikan pendekatan baru untuk estimasi parameter stellar menggunakan deep learning dengan arsitektur yang dioptimalkan. Kami menerapkan Algoritma Komodo Mlipir (KMA), teknik optimasi metaheuristik terinspirasi alam, untuk menemukan hyperparameter optimal pada Convolutional Neural Networks (CNN) yang memprediksi parameter stellar dari data spektroskopi.

Pendekatan kami menyediakan:

1. **Landasan teoretis** untuk KMA dalam konteks optimasi hyperparameter
2. **Pipeline pemrosesan efisien** untuk data spektral dari berbagai survei
3. **Teknik optimasi canggih** dengan kemampuan adaptif dan multi-objektif
4. **Pembandingan komprehensif** dengan metode optimasi state-of-the-art
5. **Alat analisis dan visualisasi** untuk memahami performa model dan trajektori optimasi

## Fitur Utama

- **Kerangka Teoretis**: Formulasi matematis KMA dengan analisis konvergensi
- **Dukungan Multi-Survei**: Memproses data spektral dari APOGEE, LAMOST, dan GALAH
- **Varian KMA Canggih**: Implementasi dengan tingkat mlipir adaptif dan kemampuan multi-objektif
- **Suite Perbandingan**: Benchmark terhadap Optimasi Bayesian, PSO, SHADE, dan Neural Architecture Search
- **Prediksi Parameter Stellar**: Memperkirakan T<sub>eff</sub>, log g, [M/H], dan v<sub>e</sub> sin i dengan akurasi tinggi

## Instalasi

```bash
# Klon repositori
git clone https://github.com/usernamemu/kma-cnn-stellar-parameters.git
cd kma-cnn-stellar-parameters

# Siapkan lingkungan dengan conda
conda env create -f environment.yml
conda activate kma-cnn

# Atau dengan pip
pip install -r requirements.txt

# Instal paket dalam mode pengembangan
pip install -e .
