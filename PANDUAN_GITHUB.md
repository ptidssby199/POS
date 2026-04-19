# 📖 Panduan Upload POSku ke GitHub

Panduan lengkap cara upload POSku ke GitHub dan aktifkan GitHub Pages — **tanpa perlu install apapun**, cukup browser.

---

## ⚡ Ringkasan Cepat (5 menit)

```
1. Buat akun GitHub (gratis) di github.com
2. Buat repository baru → Public → Create
3. Upload semua file dari folder ini
4. Settings → Pages → main / root → Save
5. Selesai! Akses di https://USERNAME.github.io/NAMA-REPO/
```

---

## 📋 Langkah Detail

### Step 1 — Buat Akun GitHub
Jika belum punya akun, daftar gratis di **[github.com/signup](https://github.com/signup)**

### Step 2 — Buat Repository Baru
1. Login ke GitHub
2. Klik tombol **"+"** (pojok kanan atas) → **"New repository"**
3. Isi:
   - **Repository name**: `posku`
   - **Description**: `Aplikasi POS berbasis web - offline ready`
   - Pilih: ✅ **Public**
   - Centang: ✅ **Add a README file**
4. Klik **"Create repository"**

### Step 3 — Upload File
1. Di halaman repository → klik **"Add file"** → **"Upload files"**
2. **Drag & drop** semua file berikut ke area upload:
   - ✅ `index.html`
   - ✅ `README.md`
   - ✅ `LICENSE`
   - ✅ `.gitignore`
   - ✅ `_config.yml`
   - ✅ `PANDUAN_GITHUB.md`
3. Di bagian **"Commit changes"**:
   - Tulis pesan: `Upload POSku v2.0.0`
4. Klik **"Commit changes"**

> **Catatan folder `.github/`:** GitHub tidak bisa upload folder kosong lewat browser.
> Folder `.github/ISSUE_TEMPLATE/` bisa diabaikan — tidak mempengaruhi aplikasi.

### Step 4 — Aktifkan GitHub Pages
1. Klik tab **"Settings"** di repo Anda
2. Di sidebar kiri, klik **"Pages"**
3. Di bagian **"Build and deployment"**:
   - Source: **"Deploy from a branch"**
   - Branch: **"main"** | Folder: **"/ (root)"**
4. Klik **"Save"**

### Step 5 — Akses Aplikasi
Tunggu 1–3 menit, lalu refresh halaman Settings → Pages.
Akan muncul:
```
✅ Your site is live at https://USERNAME.github.io/posku/
```

**Selesai!** 🎉 POSku sekarang bisa diakses dari mana saja.

---

## 🔄 Update Aplikasi (Versi Baru)

Saat ada file `index.html` baru:

**Cara mudah (browser):**
1. Buka repo di GitHub
2. Klik file `index.html`
3. Klik ikon **pensil** (✏️ Edit this file) di kanan atas
4. Tekan **Ctrl+A** → hapus semua → paste isi file baru
5. Klik **"Commit changes"** → **"Commit directly to main"**
6. Tunggu 1–2 menit → GitHub Pages otomatis update

**Cara upload ulang:**
1. Hapus `index.html` lama (klik file → ikon tempat sampah)
2. Upload `index.html` baru
3. Commit

---

## 🔄 Cara Sync Dua Arah Antar Perangkat

POSku punya fitur **Sinkronisasi Server ↔ Client** via file JSON:

### Setup Awal
- **Perangkat Pusat/Admin** → buka Sinkronisasi → pilih **"Server / Pusat"**
- **Perangkat Kasir/Cabang** → buka Sinkronisasi → pilih **"Client / Cabang"**

### Server mengirim update ke Client (produk baru, harga baru)
```
Server → "Export Data Master" → download file JSON
         Kirim file ke kasir via WhatsApp / Drive / USB
Client → "Terima dari Server" → upload file → Preview → "Terapkan Update"
```

### Client mengirim transaksi ke Server
```
Client → "Kirim ke Server" → download file JSON
         Kirim file ke server via WhatsApp / Drive / USB
Server → "Terima dari Client" → upload file → Preview → "Gabungkan Data"
```

> ✅ Smart merge: transaksi duplikat otomatis dideteksi dan dilewati

---

## 📱 Tips Penggunaan di Tablet / HP

Setelah GitHub Pages aktif:
1. Buka link `https://USERNAME.github.io/posku/` di browser HP/tablet
2. Klik menu browser → **"Add to Home Screen"** / **"Tambahkan ke Layar Utama"**
3. POSku akan muncul seperti aplikasi di home screen!

---

## ❓ Troubleshooting

| Masalah | Solusi |
|---|---|
| GitHub Pages tidak muncul | Pastikan repo **Public**, tunggu 3–5 menit, cek tab **Actions** |
| Halaman 404 | Pastikan file bernama tepat `index.html` (huruf kecil) |
| Data hilang saat buka di browser lain | Data localStorage tidak dibagikan antar browser — gunakan fitur Sinkronisasi |
| Logo tidak muncul | Logo tersimpan di localStorage, tidak ikut ke GitHub — upload ulang logo di Pengaturan |

---

## 🔗 Link Berguna

- GitHub Signup: https://github.com/signup
- GitHub Pages Docs: https://docs.github.com/pages
- Git Download: https://git-scm.com/downloads

