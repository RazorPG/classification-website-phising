# Klasifikasi Website Phishing Menggunakan IBM Granite

## Overview
Proyek ini bertujuan mengklasifikasikan website phishing vs legitimate berdasarkan fitur teknikal menggunakan model IBM Granite LLM melalui Replicate API.

## Dataset
- Sumber: Kaggle (https://www.kaggle.com/datasets/eswarchandt/phishing-website-detector)
- Format: CSV
- Jumlah fitur: 30+
- Label: `1` (Phishing), `-1` (Legit)

## Langkah Analisis
1. Load dan preprocessing dataset
2. Konversi fitur menjadi prompt deskriptif
3. Kirim prompt ke Granite via Replicate API
4. Evaluasi prediksi Granite
5. Visualisasi dan insight

## Insight & Findings
- Granite memprediksi dengan akurasi awal 40%
- Beberapa fitur yang sensitif adalah: HTTPS, penggunaan IP, panjang URL
- Model cenderung overgeneralize ke kategori “legitimate”

## AI Support Explanation
Granite (ibm-granite/granite-3.3-8b-instruct) digunakan untuk memahami pola dari fitur website phishing melalui prompt berbasis teks. Model dipanggil via API dari Replicate langsung di Google Colab.
