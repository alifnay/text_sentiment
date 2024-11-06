<h1 align="center">Sentiment Analysis using Caikit and Hugging Face</h1>
<p align="center">Berisi tentang model sentiment analisis yang dibuat menggunakan Caikit dan Hugging Face</p>

<div align="center">
    <img src="https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54">
    <img src="https://img.shields.io/badge/SciPy-%230C55A5.svg?style=for-the-badge&logo=scipy&logoColor=%white">
    <img src="https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white">
</div>

## Overview

Proyek Analisis Sentimen Teks dirancang untuk menganalisis dan mengkategorikan sentimen dari teks menjadi positif, negatif, atau netral. Alat ini memanfaatkan pembelajaran mesin dan pemrosesan bahasa alami untuk memahami nilai emosional dalam data teks, sehingga berguna untuk aplikasi seperti analisis umpan balik pelanggan, pemantauan media sosial, dan lainnya.

Sebagai contoh, dengan input *"I don't love you, like I did yesterday."* analisis sentimen mendeteksi sentimen **negatif**. Sebaliknya, dengan masukan *"You are so beautiful today"* sentimen yang diidentifikasi adalah **positive**.

## Model Components

1. **Data Model**: Modul `data_model` menangani pemrosesan data dan mengubah teks mentah menjadi format yang sesuai untuk dimasukkan ke dalam model. Modul ini membersihkan, melakukan tokenisasi, dan menyiapkan data sehingga meningkatkan akurasi model dengan memastikan konsistensi dalam format input.
   
2. **Runtime Model**: Modul `runtime_model` terintegrasi dengan pustaka Hugging Face dan memanfaatkan model bahasa pra-latih yang telah di-tuning untuk analisis sentimen. Komponen ini bertanggung jawab memprediksi label sentimen berdasarkan teks input.
   
3. **Configuration Management**: Melalui file konfigurasi (`config.yml`), pengguna dapat menentukan parameter model, jalur data, dan berbagai pengaturan runtime. Fleksibilitas ini memudahkan penyesuaian model untuk tugas analisis sentimen atau dataset tertentu.

## Prerequisites

Untuk menjalankan proyek ini, pastikan persyaratan berikut telah terpasang:

- **Caikit (v0.9.2)** 
- **Python (v3.8+)** 
- **pip (v23.0+)** 

## Getting Started

**1. Clone Repository**

Pertama, clone repository ke komputer lokal dan masuk ke direktori proyek:
```bash
git clone https://github.com/alifnay/text_sentiment
cd text-sentiment
```

**2. Upgrade pip**

Pastikan pip diperbarui ke versi terbaru. Ini diperlukan untuk menginstal semua paket yang dibutuhkan:
```bash
python -m pip install --upgrade pip
```

**3. Install Dependencies**

Instal dependencies yang dibutuhkan seperti yang tercantum di requirements.txt:
```bash
pip install -r requirements.txt
```

**4. Start the Runtime**

Untuk menginisialisasi lingkungan runtime, jalankan skrip start_runtime.py. Skrip ini menyiapkan dan mempersiapkan lingkungan untuk analisis sentimen teks:
```bash
python start_runtime.py
```

**5. Run the Client**

Gunakan client.py untuk berinteraksi dengan model sentimen teks. Skrip ini memungkinkan pengguna memasukkan data teks dan mendapatkan prediksi sentimen:
```bash
python client.py
```

## Project Structure

Repository ini diorganisir sebagai berikut:

```plaintext
text-sentiment/
├── start_runtime.py               # Skrip untuk inisialisasi lingkungan runtime
├── client.py                      # Skrip client untuk berinteraksi dengan model sentimen
├── requirements.txt               # Daftar dependensi proyek
├── models/                        
│   └── text_sentiment/
│       └── config.yml             # File konfigurasi untuk pengaturan model
└── text_sentiment/                
    ├── config.yml                 # File konfigurasi utama
    ├── __init__.py                # Inisialisasi paket
    ├── data_model/                # Submodul data model
    │   ├── classification.py      # Logika klasifikasi
    │   └── __init__.py            
    └── runtime_model/             # Submodul model runtime
        ├── hf_module.py           # Integrasi model Hugging Face
        └── __init__.py
```
