# 🌤️ Dashboard Cuaca — Multi Kota

Dashboard cuaca interaktif dengan dukungan **banyak kota** (Indonesia, ASEAN, dan Dunia) serta **deteksi lokasi otomatis** dari GPS browser. Data prakiraan real-time dari [Open-Meteo API](https://open-meteo.com/) — gratis dan tanpa API key.

![Preview](https://images.unsplash.com/photo-1555899434-94d1368aa7af?auto=format&fit=crop&w=1200&q=80)

---

## ✨ Fitur

### 🌍 Multi-Kota
- **Default: Jakarta** saat pertama dibuka
- **Pilihan kota lengkap** lewat dropdown, dikelompokkan:
  - **Indonesia** — 16 kota (Jakarta, Surabaya, Bandung, Medan, Semarang, Makassar, Palembang, Denpasar/Bali, Yogyakarta, Balikpapan, Pontianak, Manado, Padang, Pekanbaru, Banjarmasin, Jayapura)
  - **ASEAN** — 10 kota (Singapore, Kuala Lumpur, Bangkok, Manila, Hanoi, Ho Chi Minh City, Phnom Penh, Vientiane, Yangon, Bandar Seri Begawan)
  - **Dunia** — 10 kota (Tokyo, Seoul, Beijing, New York, Los Angeles, London, Paris, Dubai, Sydney, Toronto)
- Pilihan kota **tersimpan otomatis** (localStorage) — saat dibuka lagi langsung ke kota terakhir

### 📍 Deteksi Lokasi Otomatis
- Tombol **"📍 Pakai Lokasi Saya"** memakai geolocation browser
- Koordinat GPS diterjemahkan jadi nama kota lewat **reverse geocoding** (BigDataCloud, gratis tanpa API key)
- Semua judul & teks otomatis berubah sesuai kota yang terdeteksi

### 🌐 Timezone Otomatis
- Zona waktu mengikuti kota masing-masing (`timezone=auto`)
- Label waktu (GMT+7, GMT+9, dll.) menyesuaikan otomatis
- Perhitungan "jam sekarang" memakai offset kota — bukan waktu perangkat

### 📊 Visualisasi & Interaksi
- **Layout landscape** lebar (max 1440px), split 2 kolom
- **Header image** full-width (20% tinggi) — foto dari Unsplash
- **4 grafik interaktif** (semua bisa diklik untuk detail): suhu, kelembaban, angin, peluang hujan
- **5 KPI cards** clickable — modal berisi statistik + sparkline + tabel per jam
- **7 insight otomatis** — puncak suhu, peringatan hujan, angin, UV, tren 3 hari
- **Prakiraan 7 hari** — kartu per hari clickable (maks/min, hujan, UV, sunrise/sunset)
- **Footer** bertema komunitas

## 🚀 Cara Pakai

1. Buka `dashboard_cuaca_multikota.html` di browser (double-click)
2. Kota default = **Jakarta**; ganti lewat dropdown atau tombol lokasi
3. Data cuaca diambil live dari Open-Meteo API

> Tidak ada build step. Hanya butuh koneksi internet untuk data cuaca & gambar.

## 🛠️ Teknologi

| Komponen | Detail |
|----------|--------|
| **Framework** | [Vue 3](https://vuejs.org/) (global build via CDN) |
| **Grafik** | SVG native (tanpa library chart) |
| **Data cuaca** | [Open-Meteo API](https://open-meteo.com/) |
| **Reverse geocoding** | [BigDataCloud](https://www.bigdatacloud.com/) (gratis, tanpa key) |
| **Gambar** | [Unsplash](https://unsplash.com/) |

## 📊 Sumber Data

```
https://api.open-meteo.com/v1/forecast
  ?latitude=<lat>&longitude=<lon>
  &hourly=temperature_2m,relative_humidity_2m,windspeed_10m,precipitation_probability
  &daily=temperature_2m_max,temperature_2m_min,precipitation_probability_max,weathercode,sunrise,sunset,uv_index_max
  &timezone=auto&forecast_days=7
```

Reverse geocoding:
```
https://api.bigdatacloud.net/data/reverse-geocode-client?latitude=<lat>&longitude=<lon>&localityLanguage=id
```

## 📁 Struktur

```
.
├── dashboard_cuaca_multikota.html   # Dashboard multi-kota (single file)
├── dashboard_cuaca_jakarta.html     # Versi khusus Jakarta
├── index.html                       # Landing / redirect (GitHub Pages)
└── README.md
```

---

**Creao AI Agent - NexusAI Community - 2026-X-IV**
