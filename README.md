# 📚 Pustaka Kampus - Sistem Informasi Perpustakaan Digital

Sistem Informasi Perpustakaan berbasis web yang dibangun menggunakan **Laravel** dan **Tailwind CSS**. Aplikasi ini memungkinkan mahasiswa untuk mencari dan meminjam buku, serta admin untuk mengelola katalog buku dan laporan peminjaman.

---

## 👥 Anggota Kelompok

**Tugas Kelompok Pemrograman Web Lanjut**

| No | Nama Lengkap | NIM | Peran (Jobdesk) |
|----|--------------|-----|-----------------|
| 1. | **Syaifus Sholihin Putra Aditama** | 2402510001 | Project Manager & Fullstack |
| 2. | **Riyan Subhan Akbar** | 2402510017 | Backend Developer |
| 3. | **Moh Ferdiansyah Brawijayanto** | 2402510021 | Frontend & UI/UX |
| 4. | **Sakinah Hidayati** | 2402510019 | Database & QA |

---

## 🚀 Fitur Unggulan

### 🌍 Halaman Publik (Guest)
* **Landing Page Modern:** Menampilkan katalog buku terbaru tanpa perlu login.
* **About Team:** Halaman profil tim pengembang dengan foto.
* **Navigasi:** Akses mudah ke Login dan Register.

### 👤 Dashboard User (Mahasiswa)
* **Katalog Buku:** Melihat daftar buku dengan tampilan cover yang rapi (Grid Layout).
* **Pencarian Canggih:** Mencari buku berdasarkan Judul, Penulis, atau Kategori.
* **Peminjaman:** Fitur *one-click* untuk meminjam buku (jika stok tersedia).
* **Status Peminjaman:** Tabel real-time untuk melihat buku yang sedang dipinjam, tanggal pinjam, dan batas waktu kembali.

### 🛡️ Dashboard Admin
* **Akses Admin Default:**
  * **Email:** `admin@perpus.com`
  * **Password:** `password`
* **Manajemen Buku (CRUD):** Tambah, Edit, Hapus buku beserta **Upload Gambar Cover**.
* **Laporan Peminjaman:** Memantau siapa yang meminjam buku.
* **Proses Pengembalian:** Tombol untuk memproses pengembalian buku (stok otomatis bertambah).
* **Hapus Riwayat:** Membersihkan data transaksi yang sudah selesai.

---

## 🛠️ Teknologi yang Digunakan

* **Framework:** Laravel 12
* **Language:** PHP 8.2
* **Frontend:** Blade Templating + Tailwind CSS
* **Database:** MySQL
* **Authentication:** Laravel Breeze
* **Assets Manager:** Vite

---

## 💻 Panduan Instalasi (Quick Start)

Jalankan perintah-perintah berikut di terminal Anda secara berurutan untuk menjalankan aplikasi:

```bash
# 1. Download Project
git clone [https://github.com/kelompok-satset/perpustakaan-mini.git](https://github.com/kelompok-satset/perpustakaan-mini.git)
cd perpustakaan-mini

# 2. Install Library Pendukung
composer install
npm install

# 3. Setup File Konfigurasi
cp .env.example .env
php artisan key:generate

# --- PENTING: SETTING DATABASE SEKARANG ---
# 1. Buat database kosong bernama 'perpustakaan_mini' di phpMyAdmin
# 2. Buka file .env dan pastikan: DB_DATABASE=perpustakaan_mini
# ------------------------------------------

# 4. Buat Tabel & Akun Admin
php artisan migrate --seed

# 5. Jalankan Aplikasi (Gunakan 2 Terminal Berbeda)
# Terminal A:
php artisan serve

# Terminal B:
npm run dev

