# 🛒 POSku — Aplikasi Point of Sale Web

![Version](https://img.shields.io/badge/versi-2.0.0-blue)
![License](https://img.shields.io/badge/lisensi-MIT-green)
![Platform](https://img.shields.io/badge/platform-Web%20%7C%20Tablet%20%7C%20PC-lightgrey)
![Storage](https://img.shields.io/badge/storage-localStorage-orange)
![Offline](https://img.shields.io/badge/mode-offline--ready-brightgreen)

**POSku** adalah aplikasi Point of Sale (POS) berbasis web yang berjalan sepenuhnya di browser — tidak memerlukan server backend, tidak perlu instalasi, dan bekerja secara **offline**. Semua data tersimpan di `localStorage` perangkat Anda.

🌐 **[Lihat Demo Live →](https://YOUR_USERNAME.github.io/posku/)**

---

## ✨ Fitur Lengkap

### 🔐 Autentikasi & Keamanan
- Login **username + PIN 6 digit** dengan keypad visual
- **3 role**: Administrator, Manajer, Kasir
- Hak akses per menu (granular permission)
- Ganti PIN dari dalam aplikasi

### 🛒 Kasir / POS
- Grid produk dengan **foto upload** atau ikon emoji (100+)
- Filter kategori & pencarian real-time
- Indikator **stok hampir habis** (≤5) dan **stok habis**
- Diskon nominal atau persentase
- **Tunda transaksi** (hold & restore)
- Metode bayar: Tunai, Debit, QRIS, Transfer + kustom
- Numpad + kalkulasi kembalian otomatis

### 📊 Dashboard & Laporan
- Sapaan + ringkasan hari ini vs kemarin
- Alert stok habis & hampir habis
- Grafik penjualan 7 hari
- Laporan filter: Hari ini / 7 hari / Bulan ini / Kustom
- Ekspor laporan ke CSV

### ⏰ Manajemen Shift
- Buka & tutup shift dengan modal awal kas
- Live total penjualan per shift
- Rincian per metode pembayaran saat tutup shift

### 🔄 Sinkronisasi Dua Arah (Server ↔ Client)
Sync manual via file JSON — tanpa internet, tanpa server cloud:

**Server / Pusat:** Export data master, terima & gabung transaksi dari cabang

**Client / Cabang:** Kirim transaksi ke server, terima update produk/harga

> File dikirim via WhatsApp, Google Drive, USB, dll.

### 🖨️ Struk Thermal 80mm
### 🏪 Multi Cabang & Multi User
### ⚙️ Pengaturan Lengkap (logo, pajak, metode bayar, bahasa)

---

## 🚀 Cara Pakai

### Opsi 1 — Offline (Tanpa Internet)
1. Download file `index.html`
2. Buka di browser mana saja
3. Login dan mulai pakai

### Opsi 2 — GitHub Pages (Online, Gratis)
1. Fork repo ini
2. **Settings → Pages → Source: main / root → Save**
3. Tunggu 1–3 menit → akses di `https://USERNAME.github.io/posku/`

📖 **[Baca panduan lengkap upload ke GitHub →](PANDUAN_GITHUB.md)**

---

## 🔑 Akun Default

| Username | PIN | Role | Akses |
|---|---|---|---|
| `admin` | `123456` | Administrator | Semua fitur |
| `manajer` | `111111` | Manajer | POS, Produk, Laporan, Shift |
| `kasir1` | `222222` | Kasir | POS & Transaksi |

> ⚠️ **Ganti PIN segera** setelah login via sidebar → nama user → Ganti PIN

---

## 🔄 Alur Sinkronisasi Dua Arah

```
┌──────────────────────────────────────────────────┐
│              SERVER / PUSAT                       │
│   Export Master ──────────► Kirim ke Cabang      │
│   Terima Transaksi ◄─────── Dari Cabang          │
└──────────────────────────────────────────────────┘
         File JSON via WA / Drive / USB
┌──────────────────────────────────────────────────┐
│           CLIENT / CABANG (A, B, C...)            │
│   Terima Master ◄────────── Dari Server          │
│   Kirim Transaksi ──────────► Ke Server          │
└──────────────────────────────────────────────────┘
```

---

## 📁 Struktur File

```
posku/
├── index.html           ← Seluruh aplikasi (single file)
├── README.md            ← Dokumentasi
├── LICENSE              ← MIT License
├── PANDUAN_GITHUB.md    ← Panduan upload step-by-step (Bahasa Indonesia)
├── .gitignore
├── _config.yml          ← GitHub Pages config
└── .github/
    └── ISSUE_TEMPLATE/
        ├── bug_report.md
        └── feature_request.md
```

---

## 📋 Changelog

### v2.0.0 (2025)
- ✅ Sinkronisasi **dua arah** Server ↔ Client
- ✅ Smart merge transaksi (deteksi duplikat otomatis)
- ✅ Preview sebelum apply/merge
- ✅ Hak akses granular per menu
- ✅ Dashboard alert stok + komparasi hari kemarin
- ✅ Shift kasir lengkap dengan rincian tutup
- ✅ Ganti PIN dari dalam app
- ✅ ID transaksi readable
- ✅ Login hint → info versi app

### v1.0.0 — Rilis pertama

---

## 📄 Lisensi

[MIT License](LICENSE) — bebas digunakan dan dimodifikasi.

<div align="center"><strong>POSku v2.0.0</strong> · Dibuat dengan ❤️</div>
