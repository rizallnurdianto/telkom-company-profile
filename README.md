# Telkom University Company Profile - Praktikum
Project simulasi HTML, CSS, PHP native, MySQL/MariaDB, dan Git.

Project ini adalah simulasi website company profile sederhana yang dibangun untuk memenuhi tugas praktikum Pemrograman Web. Website ini menggunakan PHP native, MySQL/MariaDB, dan dikelola versinya menggunakan Git.

## Fitur Utama
* **Beranda:** Halaman utama yang dapat diakses tanpa error PHP.
* **Program Studi:** Menampilkan data program studi yang diambil langsung dari database.
* **Berita:** Fitur list berita dan halaman detail berita yang berfungsi penuh.
* **Kontak:** Form kontak yang dapat menyimpan pesan pengguna ke dalam database.
* **Admin Lokal:** Fitur simulasi untuk menambah berita baru.

## Persyaratan Sistem
* XAMPP
* PHP 7.4 atau lebih baru
* MySQL/MariaDB
* Git
* Browser web

## Penjelasan Merge Conflict
Simulasi merge conflict dilakukan dengan mengubah baris teks yang sama persis pada file `includes/header.php` di dua branch berbeda, yaitu `main` dan `conflict-navbar`. Karena kedua branch mengubah titik yang sama, Git menolak penggabungan otomatis dan menandai file sebagai konflik dengan marker `<<<<<<<`, `=======`, dan `>>>>>>>`. 

Penyelesaiannya dilakukan dengan:
1. Memilih teks final secara manual di file yang konflik
2. Menghapus semua marker konflik
3. Menjalankan `git add includes/header.php`
4. Menjalankan `git commit -m "merge: selesaikan conflict navbar"`

Setelah merge selesai, branch `conflict-navbar` dihapus karena sudah tidak diperlukan lagi.

## Riwayat Praktikum Git
* 57d9830 (HEAD -> main, origin/main) docs: memperbarui dokumentasi README
* f96a9f2 (tag: v1.0.0) Revert "docs: perubahan untuk simulasi revert"
* 6b68780 docs: perubahan untuk simulasi revert
*   ff80dc2 merge: selesaikan conflict README
|\
| * 5093849 docs: perubahan dari Laptop B
* | 6e5648c docs: perubahan dari Laptop A
|/
* 50faac0 docs: perbarui README dari Laptop B
*   d350797 merge: selesaikan conflict navbar
|\
| * f3d0e4b (conflict-navbar) feat: ubah label profil pada branch conflict
* | d7cc0f2 style: ubah label profil pada main
|/
* a3c2e71 feat: tambahkan informasi fokus pembelajaran
* 7b81ced feat: tambahkan form admin lokal untuk berita
* 236a220 feat: simpan pesan kontak ke database
* 2b81436 feat: simpan pesan kontak ke database
* 8e5c3ab feat: tambahkan daftar dan detail berita
* 3ff1c11 feat: hubungkan database dan tampilkan program studi
* 61d2e05 feat: tambahkan layout dasar dan stylesheet
* 6f1c156 chore: inisialisasi project dan dokumentasi awal

## Cara Menjalankan Project

1. **Clone Repository**
   Buka terminal dan menggunakan perintah berikut:
   ```bash
   git clone https://github.com/rizallnurdianto/telkom-company-profile-109062500140.git
   ```

2. **Pindahkan Folder**
   Letakkan folder project di direktori
    `C:\xampp\htdocs\`.

3. **Jalankan Apache dan MySQL**
   Buka XAMPP Control Panel, lalu klik Start pada Apache dan MySQL untuk menjalankan server lokal.

4. **Impor Database**
   Buka phpMyAdmin melalui `http://localhost/phpmyadmin`, lalu buat database telkom_profile dan impor file SQL yang tersedia di folder `database/`

5. **Konfigurasi Koneksi Database**
   Sesuaikan konfigurasi koneksi database pada file `config/database.php`.

6. **Akses Website**
   Buka website melalui browser dengan alamat lokal kamu, misalnya:
   `http://localhost/telkom-company-profile/109062500140/`