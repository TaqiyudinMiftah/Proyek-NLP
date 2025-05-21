# 📱 Google Play Review Scraper & Preprocessing

Proyek ini bertujuan untuk **mengambil ulasan aplikasi Android dari Google Play Store** dan melakukan **pra-pemrosesan** teks seperti normalisasi kata tidak baku (slang).

## 🚀 Fitur

- Scraping semua ulasan dari aplikasi Android berdasarkan App ID.
- Pemrosesan teks:
  - Tokenisasi
  - Konversi slangwords (kata tidak baku → kata baku)
- Siap untuk analisis sentimen, visualisasi, dan NLP lanjutan.

---

## 📦 Dependencies

Pastikan Python environment kamu memiliki pustaka berikut:

```bash
pip install google-play-scraper pandas
```