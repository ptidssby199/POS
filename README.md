# 🛒 POSku — Aplikasi Point of Sale Web

![Version](https://img.shields.io/badge/versi-2.0.0-blue)
![License](https://img.shields.io/badge/lisensi-MIT-green)
![Platform](https://img.shields.io/badge/platform-Web%20%7C%20Tablet%20%7C%20PC-lightgrey)
![Offline](https://img.shields.io/badge/mode-offline--ready-brightgreen)

**POSku** adalah aplikasi Point of Sale (POS) berbasis web yang berjalan sepenuhnya di browser — tidak memerlukan server, tidak perlu instalasi, dan bekerja **offline**. Semua data tersimpan di `localStorage` perangkat Anda.

🌐 **[Lihat Demo Live →](https://YOUR_USERNAME.github.io/posku/)**

---

## ✨ Fitur Lengkap

| Fitur | Keterangan |
|---|---|
| 🔐 Login PIN | Username + PIN 6 digit, keypad visual |
| 👥 Multi Role | Administrator, Manajer, Kasir — hak akses per menu |
| 🔑 Ganti PIN | Dari dalam aplikasi tanpa logout |
| 🛒 Kasir / POS | Grid produk, foto/emoji, filter, diskon, hold transaksi |
| 💳 Pembayaran | Tunai, Debit, QRIS, Transfer + metode kustom |
| 📊 Dashboard | Ringkasan harian, grafik 7 hari, alert stok |
| 📦 Produk | Upload foto, drag & drop, stok, barcode |
| 📈 Laporan | Filter periode, export CSV, grafik penjualan |
| ⏰ Shift | Buka/tutup shift, live total, rincian per metode bayar |
| 🏪 Multi Cabang | Banyak cabang, user per cabang |
| 🔄 Sync Dua Arah | Server ↔ Client via file JSON (smart merge) |
| 💾 Backup & Restore | Full backup semua data ke JSON |
| 🖨️ Struk Thermal | Cetak 80mm, logo, header/footer kustom |
| 🌐 Multi Bahasa | Indonesia & English |
| 🔁 Session Persist | Tetap login walau browser di-refresh |
| ⚙️ Pengaturan | Logo, pajak, timeout sesi, info versi & storage |

---

## 🚀 Cara Pakai

### Opsi 1 — Buka Langsung (Offline)
Download `index.html` → buka di browser → selesai.

### Opsi 2 — GitHub Pages (Online, Gratis)
1. Fork repo ini
2. **Settings → Pages → Source: main / root → Save**
3. Akses di `https://USERNAME.github.io/posku/`

📖 **[Panduan lengkap upload ke GitHub →](PANDUAN_GITHUB.md)**

---

## 🔑 Akun Default

| Username | PIN | Role |
|---|---|---|
| `admin` | `123456` | Administrator (semua akses) |
| `manajer` | `111111` | Manajer |
| `kasir1` | `222222` | Kasir |

> ⚠️ Ganti PIN setelah login pertama: **sidebar → nama user → Ganti PIN**

---

## 🔄 Sinkronisasi Dua Arah

```
🖥️ SERVER/PUSAT                    💻 CLIENT/CABANG
Export Master ──── file JSON ────► Terima & Terapkan
(produk, harga,                    (update otomatis)
 user, setting)

Terima & Gabung ◄── file JSON ──── Kirim Transaksi
(smart merge,                      (hanya data baru)
 deteksi duplikat)
```

File dikirim via WhatsApp, Google Drive, USB, email, dll.

---

## 💾 Backup & Restore

- **Backup** → download semua data ke 1 file JSON (untuk cadangan)
- **Restore** → upload file backup (menimpa semua data lokal)
- Berbeda dari Sync: Backup untuk cadangan, Sync untuk tukar data antar cabang

---

## 🔁 Session Tetap Login

Setelah login, sesi disimpan otomatis. Refresh browser / tutup tab tidak memerlukan login ulang. Bisa diatur timeout di **Pengaturan → Umum → Timeout Sesi Login** (default: tidak ada timeout).

---

## 📁 Struktur File

```
posku/
├── index.html           ← Seluruh aplikasi (single file, ~200KB)
├── README.md
├── LICENSE              ← MIT
├── .gitignore
├── _config.yml          ← GitHub Pages config
├── PANDUAN_GITHUB.md    ← Panduan step-by-step Bahasa Indonesia
└── .github/
    └── ISSUE_TEMPLATE/
        ├── bug_report.md
        └── feature_request.md
```

---

## 📋 Changelog

### v2.0.0 (2025)
- ✅ Session persist — tetap login setelah refresh browser
- ✅ Sinkronisasi dua arah Server ↔ Client (smart merge)
- ✅ Backup & Restore full data
- ✅ Hak akses granular per menu
- ✅ Shift kasir lengkap dengan rincian tutup
- ✅ Dashboard alert stok + komparasi hari kemarin
- ✅ Ganti PIN dari dalam app
- ✅ ID transaksi readable
- ✅ Multi bahasa ID/EN
- ✅ Info versi & storage usage

### v1.0.0 — Rilis pertama

---

## 📄 Lisensi

[MIT License](LICENSE) — bebas digunakan, dimodifikasi, dan didistribusikan.

<div align="center"><strong>POSku v2.0.0</strong> · Dibuat dengan ❤️</div>
