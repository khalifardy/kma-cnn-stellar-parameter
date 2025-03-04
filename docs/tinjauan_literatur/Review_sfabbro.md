## An application of deep learning in the analysis of stellar spectra

### 1. Introduction 

#### a). Previous Spektroskopy Analysis Method

1. SDSS SEGUE Pipeline
- perhitungan indeks garis -> langkah awal mengubah skala panjang gelombang dari spektrums sdss asli ke skala panjang gelombang berbasis udara (bukan berbasis vakum) dan melakukan rebinning linear spektrum ke bin 1 A di bagian biru (3800-6000 A) dan bin 1.5 A dibagian merah (6000-9000 A). Kemudian berdasarkan kecepatan radia yang diadopsi seperti dijelaskan diatas, skala panjang gelombang digeser ke panjang gelombang istirahat nol

menggunakan dua mode dalam perhitungannya:
- fitting kontinumm global di seluruh rentang panjang gelombang (3850 A - 9000 A)
- Mendapatkan kontinumm lokal di sekitar pita garis yang menjadi perhatian 


indeks garis (lebar) dihitung dengan mengintegrasikan fluks yang dinormalisasi kontinumm diatas wilayah panjang gelombang yang ditentukan dari setiap pita garis.

2. Gaia Spectroscopic Analysis
