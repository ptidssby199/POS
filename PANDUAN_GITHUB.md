# 📖 Panduan Upload ke GitHub

Panduan lengkap cara mengupload POSku ke GitHub dan mengaktifkan GitHub Pages.

---

## 📋 Prasyarat

- Akun GitHub (gratis di [github.com](https://github.com))
- Git terinstall di komputer ([download](https://git-scm.com/downloads)) **— ATAU —**
- Cukup pakai browser saja (tanpa install Git)

---

## 🌐 Cara A — Upload Lewat Browser (Termudah)

### Langkah 1: Buat Repository Baru
1. Login ke [github.com](https://github.com)
2. Klik tombol **"+"** di kanan atas → **"New repository"**
3. Isi form:
   - **Repository name**: `posku` (atau nama lain)
   - **Description**: `Aplikasi POS berbasis web - offline`
   - Pilih **Public** (supaya bisa pakai GitHub Pages gratis)
   - ✅ Centang **"Add a README file"**
4. Klik **"Create repository"**

### Langkah 2: Upload File
1. Di halaman repository baru, klik **"Add file" → "Upload files"**
2. **Drag & drop** semua file dari folder `posku-github` ke area upload:
   - `index.html`
   - `README.md`
   - `LICENSE`
   - `.gitignore`
3. Di bagian **"Commit changes"**:
   - Tulis pesan: `Upload POSku v2.0.0`
4. Klik **"Commit changes"**

### Langkah 3: Aktifkan GitHub Pages
1. Masuk ke **Settings** (tab di menu repo)
2. Scroll ke bagian **"Pages"** di sidebar kiri
3. Di **"Source"**: pilih **"Deploy from a branch"**
4. Branch: pilih **"main"** → Folder: **"/ (root)"**
5. Klik **"Save"**
6. Tunggu 1–3 menit
7. Refresh halaman — akan muncul link:
   ```
   ✅ Your site is live at https://USERNAME.github.io/posku/
   ```

---

## 💻 Cara B — Lewat Git (Command Line)

### Langkah 1: Inisialisasi Git di folder
```bash
# Masuk ke folder project
cd posku-github

# Inisialisasi git
git init

# Tambahkan semua file
git add .

# Commit pertama
git commit -m "Initial commit: POSku v2.0.0"
```

### Langkah 2: Buat repo di GitHub dan hubungkan
```bash
# Hubungkan ke repo GitHub (ganti USERNAME dan REPONAME)
git remote add origin https://github.com/USERNAME/REPONAME.git

# Rename branch ke main
git branch -M main

# Push ke GitHub
git push -u origin main
```

### Langkah 3: Aktifkan GitHub Pages
Sama seperti Cara A Langkah 3 di atas.

---

## 🔄 Cara Update Aplikasi

Setelah ada versi baru:

**Lewat browser:**
1. Buka repo di GitHub
2. Klik file `index.html`
3. Klik ikon pensil (Edit)
4. Hapus semua isi → paste isi file baru
5. Klik **"Commit changes"**

**Lewat Git:**
```bash
# Salin file baru ke folder
cp /path/ke/POSku_baru.html index.html

# Add & commit
git add index.html
git commit -m "Update POSku ke v2.1.0"
git push
```

---

## 🔗 Hasil Akhir

Setelah selesai, aplikasi POSku bisa diakses di:

```
https://USERNAME.github.io/NAMA-REPO/
```

Contoh: `https://tokosaya.github.io/posku/`

Link ini bisa:
- Dibuka di browser tablet/PC/HP
- Dibookmark di home screen
- Dibagikan ke kasir

---

## 💡 Tips

- **Bookmark** halaman GitHub Pages di semua perangkat kasir
- Di Android/iOS, buka di browser lalu **"Add to Home Screen"** agar terasa seperti aplikasi
- Data tersimpan di browser masing-masing — backup rutin via **Sinkronisasi → Export Data**
- Untuk multi-cabang, setiap cabang bisa pakai file yang sama, data terpisah per browser

---

## ❓ Troubleshooting

**GitHub Pages tidak muncul:**
- Pastikan repository bersifat **Public**
- Tunggu beberapa menit setelah save settings
- Cek tab **Actions** di repo — pastikan build berhasil (ikon ✅)

**File tidak ter-upload:**
- Pastikan nama file persis `index.html` (huruf kecil semua)
- Coba upload ulang jika gagal

**Aplikasi tidak terbuka:**
- Pastikan URL-nya benar: `https://USERNAME.github.io/REPONAME/`
- Coba buka di browser Chrome terlebih dahulu
