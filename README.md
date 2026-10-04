# 🌤️ Dashboard Cuaca Jakarta

Dashboard cuaca interaktif untuk wilayah **Jakarta, Indonesia** yang menampilkan prakiraan cuaca real-time dari [Open-Meteo API](https://open-meteo.com/) — gratis dan tanpa API key.

![Preview](https://images.unsplash.com/photo-1555899434-94d1368aa7af?auto=format&fit=crop&w=1200&q=80)

---

## ✨ Fitur

- **Layout landscape** lebar (max 1440px) dengan split 2 kolom: grafik di kiri, insight di kanan
- **Header image** full-width (20% tinggi) — foto Jakarta dari Unsplash
- **Format waktu 24 jam + label WIB** (GMT+7) di seluruh tampilan
- **4 grafik interaktif** — semua bisa diklik untuk melihat detail:
  - 🌡️ Suhu udara per jam
  - 💧 Kelembaban relatif
  - 💨 Kecepatan angin
  - ☔ Peluang hujan per jam
- **5 KPI cards** clickable dengan detail modal (statistik + sparkline + tabel per jam)
- **7 insight otomatis** — puncak suhu, peringatan hujan lebat, angin kencang, indeks UV, tren 3 hari
- **Prakiraan 7 hari** — kartu per hari clickable (suhu maks/min, peluang hujan, UV, sunrise/sunset)
- **Footer** bertema komunitas

## 🚀 Cara Pakai

1. Unduh file `dashboard_cuaca_jakarta.html`
2. Buka langsung di browser (double-click) — tidak perlu install apa pun
3. Data cuaca diambil otomatis secara live dari Open-Meteo API

> Tidak ada build step, tidak ada dependency yang perlu di-install. Hanya butuh koneksi internet untuk mengambil data cuaca dan gambar header.

## 🛠️ Teknologi

| Komponen | Detail |
|----------|--------|
| **Framework** | [Vue 3](https://vuejs.org/) (global build via CDN) |
| **Grafik** | SVG native (tanpa library chart eksternal) |
| **Data** | [Open-Meteo API](https://open-meteo.com/) |
| **Gambar** | [Unsplash](https://unsplash.com/) |
| **Bahasa** | HTML + CSS + JavaScript (single file) |

## 📊 Sumber Data

Data diambil dari endpoint Open-Meteo:

```
https://api.open-meteo.com/v1/forecast
  ?latitude=-6.2&longitude=106.8
  &hourly=temperature_2m,relative_humidity_2m,windspeed_10m,precipitation_probability
  &daily=temperature_2m_max,temperature_2m_min,precipitation_probability_max,weathercode,sunrise,sunset,uv_index_max
  &timezone=Asia%2FJakarta&forecast_days=7
```

- **Koordinat:** -6.2°, 106.8° (Jakarta)
- **Zona waktu:** Asia/Jakarta (WIB, GMT+7)
- **Prakiraan:** 7 hari, resolusi per jam

## 📁 Struktur

```
.
├── dashboard_cuaca_jakarta.html   # Dashboard interaktif (single file)
└── README.md                      # Dokumentasi ini
```

---

**Creao AI Agent - NexusAI Community - 2026-X-IV**
