# 🛒 POSku — Aplikasi Point of Sale (POS) Web

![Version](https://img.shields.io/badge/versi-2.0.0-blue)
![License](https://img.shields.io/badge/lisensi-MIT-green)
![Platform](https://img.shields.io/badge/platform-Web%20%7C%20Tablet%20%7C%20PC-lightgrey)
![Storage](https://img.shields.io/badge/storage-localStorage-orange)

**POSku** adalah aplikasi Point of Sale (POS) berbasis web yang berjalan sepenuhnya di browser — tidak memerlukan server, tidak perlu instalasi, dan bekerja secara offline. Semua data tersimpan di `localStorage` perangkat Anda.

---

## 🌐 Demo Live

Buka langsung di browser setelah clone:
```
index.html → buka di browser
```
Atau deploy gratis via **GitHub Pages** (lihat panduan di bawah).

---

## ✨ Fitur Utama

### 🔐 Autentikasi & Hak Akses
- Login dengan **username + PIN 6 digit** (keypad visual)
- **3 role pengguna**: Administrator, Manajer, Kasir
- Hak akses per menu yang bisa dikustomisasi
- Ganti PIN langsung dari dalam aplikasi

### 🛒 Kasir / POS
- Grid produk dengan foto atau ikon emoji
- Filter kategori & pencarian real-time
- Indikator **stok hampir habis** (≤5) dan **stok habis**
- Diskon nominal atau persentase
- **Tunda transaksi** (hold & restore)
- Metode bayar: Tunai, Debit, QRIS, Transfer, + kustom
- Numpad pembayaran + kalkulasi kembalian otomatis
- Scan barcode (via input manual)

### 📦 Manajemen Produk
- Upload foto produk atau pilih ikon emoji (100+)
- Drag & drop gambar
- Harga jual, harga modal, stok, satuan, barcode, kategori
- Manajemen kategori dengan ikon & warna

### 📊 Dashboard & Laporan
- Sapaan & ringkasan hari ini
- Perbandingan penjualan vs kemarin
- Alert stok habis & hampir habis
- Grafik penjualan 7 hari
- Produk terlaris dengan progress bar
- Laporan filter: Hari ini, 7 hari, Bulan ini, Kustom
- Rincian per transaksi, ekspor ke CSV

### ⏰ Shift Kasir
- Buka & tutup shift dengan modal awal kas
- Live total penjualan per shift
- Rincian pembayaran per metode saat tutup shift
- Riwayat shift dengan durasi
- Kasir hanya melihat shift miliknya sendiri

### 👥 Multi User & Multi Cabang
- Manajemen pengguna dengan hak akses granular
- Dukung banyak cabang
- User bisa dikunci ke cabang tertentu

### 🖨️ Struk Thermal
- Cetak struk ke printer thermal via dialog print browser
- Format 80mm, header & footer kustom
- Logo toko di struk (opsional)
- Info rekening transfer

### 🔄 Backup & Restore
- **Export** semua data ke file JSON
- **Import** / restore dari file backup
- Sinkronisasi manual antar cabang via download & upload

### ⚙️ Pengaturan Lengkap
- Upload logo aplikasi
- Nama toko, alamat, telepon, email, website
- Pengaturan pajak (PPN, GST, dll)
- Manajemen metode pembayaran
- Multi bahasa: **Indonesia & English**
- Info versi & penggunaan storage
- Reset semua data (admin only)

---

## 🚀 Cara Menggunakan

### Opsi 1 — Buka Langsung (Offline)
1. Download file `index.html`
2. Buka di browser (Chrome, Firefox, Edge, Safari)
3. Login dengan akun default

### Opsi 2 — GitHub Pages (Akses Online)
1. Fork repo ini
2. Masuk ke **Settings → Pages**
3. Source: pilih **Deploy from a branch → main → / (root)**
4. Klik **Save**
5. Tunggu beberapa menit, lalu akses di:
   ```
   https://<username>.github.io/<nama-repo>/
   ```

---

## 🔑 Akun Default

| Username | PIN    | Role          | Akses |
|----------|--------|---------------|-------|
| `admin`  | `123456` | Administrator | Semua fitur |
| `manajer`| `111111` | Manajer       | POS, Produk, Laporan, Shift |
| `kasir1` | `222222` | Kasir         | POS & Transaksi |

> ⚠️ **Segera ganti PIN** setelah login pertama melalui menu **Akun Saya → Ganti PIN**

---

## 📁 Struktur File

```
posku/
├── index.html        ← Aplikasi utama (single file, semua fitur)
├── README.md         ← Dokumentasi ini
├── LICENSE           ← Lisensi MIT
└── .github/
    └── ISSUE_TEMPLATE.md   ← Template laporan bug
```

> Seluruh aplikasi ada dalam **satu file `index.html`** — tidak ada dependensi eksternal yang wajib, tidak perlu npm, tidak perlu build.

---

## 💾 Penyimpanan Data

Semua data disimpan di **localStorage** browser pada perangkat yang digunakan:

| Key | Isi |
|-----|-----|
| `posku_settings` | Pengaturan aplikasi & toko |
| `posku_users` | Data pengguna & hak akses |
| `posku_branches` | Data cabang |
| `posku_products` | Produk & stok |
| `posku_categories` | Kategori produk |
| `posku_transactions` | Riwayat transaksi |
| `posku_shifts` | Riwayat shift |
| `posku_held` | Transaksi yang ditunda |

> **Penting:** Data tersimpan di browser/perangkat masing-masing. Gunakan fitur **Backup & Restore** untuk pindah data antar perangkat atau antar cabang.

---

## 🔄 Sinkronisasi Antar Perangkat / Cabang

Karena menggunakan localStorage, sinkronisasi dilakukan secara **manual**:

1. Di perangkat sumber → **Sinkronisasi → Export / Backup Data** → file `.json` ter-download
2. Di perangkat tujuan → **Sinkronisasi → Import / Restore Data** → upload file `.json`

---

## 🖥️ Kompatibilitas

| Browser | Status |
|---------|--------|
| Chrome / Edge 90+ | ✅ Didukung penuh |
| Firefox 88+ | ✅ Didukung penuh |
| Safari 14+ | ✅ Didukung |
| Mobile Chrome (Android) | ✅ Didukung |
| Mobile Safari (iOS) | ✅ Didukung |

**Resolusi minimum yang direkomendasikan:** 768px (tablet landscape)

---

## 🖨️ Cetak Struk Thermal

1. Pastikan printer thermal terhubung ke komputer
2. Install driver printer thermal (80mm)
3. Setelah transaksi selesai → klik **Cetak**
4. Di dialog print browser:
   - Pilih printer thermal Anda
   - Paper size: **80mm** atau **Roll paper**
   - Margin: **None / Minimum**
5. Klik Print

---

## 📋 Changelog

### v2.0.0 (2025)
- ✅ Hak akses per menu (granular permission)
- ✅ Dashboard dengan alert stok & perbandingan vs kemarin
- ✅ Shift kasir dengan live total & rincian tutup shift
- ✅ ID transaksi readable (`CBG001-20250418-0001`)
- ✅ Ganti PIN dari dalam aplikasi
- ✅ Menu akun user di sidebar
- ✅ Tambah metode pembayaran kustom (tanpa `prompt()`)
- ✅ Info rekening transfer dari pengaturan
- ✅ Reset semua data (admin only)
- ✅ Indikator stok hampir habis di POS
- ✅ Info versi & storage usage di pengaturan
- ✅ Login hint diganti tampilan versi aplikasi
- ✅ Fix bug `event.target` di icon picker

### v1.0.0
- 🎉 Rilis pertama

---

## 🤝 Kontribusi

Pull request sangat disambut! Untuk perubahan besar, buka **Issue** terlebih dahulu untuk diskusi.

1. Fork repo ini
2. Buat branch baru: `git checkout -b fitur/nama-fitur`
3. Commit perubahan: `git commit -m 'Tambah fitur X'`
4. Push ke branch: `git push origin fitur/nama-fitur`
5. Buat Pull Request

---

## 📄 Lisensi

[MIT License](LICENSE) — bebas digunakan, dimodifikasi, dan didistribusikan.

---

<div align="center">
  <strong>POSku v2.0.0</strong> · Dibuat dengan ❤️
</div>
