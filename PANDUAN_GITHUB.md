# 📖 Panduan Upload POSku ke GitHub

Cara upload POSku ke GitHub dan aktifkan GitHub Pages — **cukup pakai browser, tanpa install apapun**.

---

## ⚡ Ringkasan (5 Menit)

```
1. Daftar/login di github.com
2. Buat repository baru (Public)
3. Upload semua file dari ZIP ini
4. Settings → Pages → main/root → Save
5. Akses di https://USERNAME.github.io/posku/
```

---

## 📋 Langkah Detail

### Step 1 — Persiapan File
Extract file ZIP ini. Anda akan mendapatkan folder dengan isi:
```
posku-github/
├── index.html        ← Wajib diupload
├── README.md         ← Wajib diupload
├── LICENSE           ← Wajib diupload
├── .gitignore        ← Wajib diupload
├── _config.yml       ← Wajib diupload
└── PANDUAN_GITHUB.md ← Wajib diupload
```

### Step 2 — Buat Repository GitHub
1. Buka **[github.com](https://github.com)** → Login
2. Klik **"+"** (pojok kanan atas) → **"New repository"**
3. Isi form:
   - **Repository name**: `posku`
   - **Description**: `Aplikasi POS berbasis web`
   - Pilih: ✅ **Public**
   - Centang: ✅ **Add a README file**
4. Klik **"Create repository"**

### Step 3 — Upload Semua File
1. Di halaman repository → klik **"Add file"** → **"Upload files"**
2. **Drag & drop** semua file berikut ke area upload:
   - `index.html`
   - `README.md`
   - `LICENSE`
   - `.gitignore`
   - `_config.yml`
   - `PANDUAN_GITHUB.md`

   > **Catatan:** File yang diawali titik (`.gitignore`) mungkin tidak terlihat di Windows.
   > Aktifkan "Show hidden files" di File Explorer, atau upload satu per satu.

3. Di bagian **"Commit changes"**:
   - Pesan commit: `Upload POSku v2.0.0`
4. Klik **"Commit changes"**

### Step 4 — Aktifkan GitHub Pages
1. Klik tab **"Settings"** di repo
2. Sidebar kiri → klik **"Pages"**
3. Di **"Build and deployment"**:
   - Source: **"Deploy from a branch"**
   - Branch: **"main"** | Folder: **"/ (root)"**
4. Klik **"Save"**

### Step 5 — Akses Aplikasi
Tunggu **1–3 menit**, lalu refresh halaman Settings → Pages.
Akan muncul:
```
✅ Your site is live at https://USERNAME.github.io/posku/
```

**Selesai! 🎉** Bookmark link tersebut di semua perangkat kasir.

---

## 📱 Pasang di Home Screen (Tablet/HP)

1. Buka link GitHub Pages di browser HP/tablet
2. Menu browser → **"Add to Home Screen"** / **"Tambahkan ke Layar Utama"**
3. POSku muncul seperti aplikasi di home screen

---

## 🔄 Update ke Versi Baru

Saat ada file `index.html` baru:

**Cara mudah lewat browser:**
1. Buka repo di GitHub
2. Klik file `index.html` → klik ikon **✏️ Edit**
3. Tekan **Ctrl+A** → hapus semua → **paste** isi file baru
4. Klik **"Commit changes"** → GitHub Pages otomatis update

**Atau upload ulang:**
1. Hapus `index.html` lama (klik file → ikon 🗑️)
2. Upload `index.html` baru → Commit

---

## 🔄 Cara Sinkronisasi Dua Arah

POSku punya sistem sync **Server ↔ Client** tanpa internet:

### Setup Awal (sekali saja)
- Perangkat kantor/admin → buka **Sinkronisasi** → pilih **"🖥️ Server / Pusat"**
- Perangkat kasir/cabang → buka **Sinkronisasi** → pilih **"💻 Client / Cabang"**

### Server → Client (kirim update produk/harga/user)
```
1. Server  : Sinkronisasi → "Export Data Master" → file JSON terdownload
2. Kirim   : via WhatsApp / Google Drive / USB / email
3. Client  : Sinkronisasi → "Terima dari Server" → upload file → Preview → "Terapkan Update"
```

### Client → Server (kirim transaksi harian)
```
1. Client  : Sinkronisasi → "Kirim ke Server" → file JSON terdownload
2. Kirim   : via WhatsApp / Google Drive / USB / email
3. Server  : Sinkronisasi → "Terima dari Client" → upload file → Preview → "Gabungkan Data"
```

> ✅ **Smart merge**: transaksi duplikat otomatis dilewati, tidak ada data dobel

### Backup Penuh (cadangan rutin)
```
Sinkronisasi → bagian "Backup & Restore Penuh" → "Download Backup"
```
Simpan file backup di Google Drive / hard disk eksternal secara rutin.

---

## ❓ Troubleshooting

| Masalah | Solusi |
|---|---|
| GitHub Pages tidak aktif | Pastikan repo **Public**. Cek tab **Actions** — tunggu build selesai |
| Halaman 404 | Pastikan nama file tepat: `index.html` (huruf kecil semua) |
| Data hilang di browser lain | Data localStorage tidak dibagikan antar browser — gunakan fitur Sinkronisasi |
| Logo hilang setelah sync | Logo tersimpan lokal — upload ulang di **Pengaturan → Umum → Upload Logo** |
| Kembali ke login setelah refresh | Update ke versi terbaru — fitur session persist sudah diperbaiki di v2.0.0 |
| `.gitignore` tidak terlihat | Di Windows: File Explorer → View → centang "Hidden items" |

---

## 🔗 Link Berguna

| | |
|---|---|
| Daftar GitHub | https://github.com/signup |
| Dokumentasi GitHub Pages | https://docs.github.com/pages |
| Download Git (opsional) | https://git-scm.com/downloads |
