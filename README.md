# Supermarket Sales Analytics & Enterprise Dashboard System

<p align="center">
  <img src="https://img.shields.io/badge/Version-1.0.0-emerald?style=for-the-badge" alt="Version">
  <img src="https://img.shields.io/badge/Environment-Client--Side-blue?style=for-the-badge" alt="Environment">
  <img src="https://img.shields.io/badge/UI--Framework-Tailwind%20CSS-38bdf8?style=for-the-badge" alt="Tailwind">
  <img src="https://img.shields.io/badge/Chart--Engine-Apache%20ECharts-red?style=for-the-badge" alt="ECharts">
</p>

---

## Deskripsi Proyek

**Supermarket Sales Analytics** adalah sebuah purwarupa *dashboard business intelligence* tingkat tinggi (*enterprise-grade*) yang dirancang khusus untuk memproses, menganalisis, dan memvisualisasikan data transaksi ritel dalam volume besar secara instan. Sistem ini mengintegrasikan pemrosesan data di sisi klien (*client-side data processing*) dengan mesin visualisasi berperforma tinggi untuk memantau indikator kinerja utama (KPI) bisnis, melacak profitabilitas, memahami segmentasi pasar, dan mengidentifikasi tren operasional secara mendalam. Aplikasi ini diciptakan sebagai solusi pemantauan satu pintu (*one-stop monitoring system*) yang adaptif untuk kebutuhan eksekutif, manajer wilayah, hingga analis data ritel dalam merumuskan strategi berbasis data (*data-driven decision making*).

---

## Pratinjau Antarmuka

### Mode Gelap (Dark Mode - Default)
<p align="center">
  <img src="Images/Mode gelap.png" alt="Dashboard Dark Mode" width="100%" style="border-radius: 8px; border: 1px solid #334155;">
  <br>
  <em>Gambar 2.1: Tampilan Utama Dashboard Pusat Kendali dalam Skema Mode Gelap.</em>
</p>

### Mode Terang (Light Mode)
<p align="center">
  <img src="Images/Mode terang.png" alt="Dashboard Light Mode" width="100%" style="border-radius: 8px; border: 1px solid #cbd5e1;">
  <br>
  <em>Gambar 2.2: Transisi Skema Warna ke Mode Terang untuk Kebutuhan Presentasi Formal.</em>
</p>

### Mode Display
<p align="center">
  <img src="Images/Display Mode.png" alt="Dashboard Light Mode" width="100%" style="border-radius: 8px; border: 1px solid #cbd5e1;">
  <br>
  <em>Gambar 2.2: Mode Display untukKebutuhan Presentasi Formal.</em>
</p>
---

## Arsitektur & Fitur Unggulan

Sistem ini dirancang tidak hanya sebagai pembuat grafik statis biasa, melainkan menggabungkan beberapa pilar optimasi web modern:

### Big Data Virtual Rendering Engine
Ketika menangani ribuan baris data, tabel HTML tradisional akan mengalami penurunan performa (*bottleneck layout rendering*). Proyek ini menerapkan konsep **Virtual Table Explorer** berbasis manipulasi DOM dinamis. Baris data hanya akan dibuat jika masuk ke dalam area pandang pengguna (*viewport*), menjamin penggunaan memori browser tetap stabil dan super ringan.

### Smart Analytics & Visualisasi Multi-Dimensi (Apache ECharts)
Mesin grafis ditenagai oleh Apache ECharts dengan konfigurasi responsif yang memetakan analisis:
* **Analisis Tren Temporal:** Grafik garis area (*smooth line*) untuk membandingkan fluktuasi kumulatif nilai Penjualan (*Sales*) dan Keuntungan (*Profit*) berdasarkan sumbu waktu.
* **Analisis Kontribusi Segmentasi:** Diagram donat (*donut chart*) interaktif untuk mengukur distribusi pangsa pasar antara kategori *Consumer, Corporate,* dan *Home Office*.
* **Analisis Kinerja Sub-Kategori:** Diagram batang horizontal terurut (*sorted bar chart*) untuk mendeteksi produk terlaris secara instan.
* **Analisis Radar Profil Wilayah:** Grafik komparatif jaring laba-laba untuk menilai keseimbangan performa antar-regional (Central, East, South, West).

### Realtime Sync & Automated Ticker
Dilengkapi dengan komponen mesin sinkronisasi data internal otomatis. Pengguna dapat memilih interval penyegaran data (*auto-refresh*) mulai dari 10 detik hingga 5 menit, didukung oleh visual *countdown ticker* yang berjalan di latar belakang secara akurat.

### Client-Side Fixed Export System (PNG & PDF)
Sistem ini memecahkan masalah umum kegagalan render dokumen dengan menyuntikkan bypass CORS melalui script manipulasi:
* **Export PNG:** Menangkap seluruh visual DOM dashboard secara presisi tinggi menggunakan `html2canvas` dengan kerapatan skala piksel ganda (scale: 2).
* **Export PDF:** Mengonversi visual kanvas menjadi dokumen cetak laporan resmi berorientasi lanskap (*A4 Landscape*) melalui pustaka `jsPDF`.

### National Command Center Monitor Mode
Menyediakan fitur *Display Mode* satu-klik yang memampukan dashboard meminimalkan komponen kontrol navigasi sekunder dan menyusutkan visualisasi agar sangat pas diproyeksikan pada layar monitor pusat kendali berukuran besar.

---

## Spesifikasi Teknologi Stack

Sistem ini murni berjalan di sisi klien (*standalone frontend build*) memanfaatkan CDN teknologi berikut:
* **UI Style & Framework:** Tailwind CSS v3.x (Dengan konfigurasi perluasan tema palet warna *Emerald Enterprise*).
* **Core Visualization Engine:** Apache ECharts v5.4.3.
* **Document Generator:** jsPDF v2.5.1 & html2canvas v1.4.1.
* **Spreadsheet Engine:** SheetJS / XLSX v0.18.5 (Menyediakan abstraksi manipulasi tabel data lokal).
* **Typography & Icons:** Plus Jakarta Sans Font & Font Awesome v6.4.0 Icons.

---
