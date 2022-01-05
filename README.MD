<h1 align="center">
Langkah-Langkah Pembuatan Web
</h1>

<table align="center">
  <tr>
    <td>Framework</td>
    <td>Laravel 8</td>
  </tr>
  <tr>
    <td>Starter Kit</td>
    <td>Jetstream</td>
  </tr>
  <tr>
    <td>VDC</td>
    <td>Github</td>
  </tr>
  <tr>
    <td>Database</td>
    <td>Postgresql/MySQL</td>
  </tr>
  <tr>
    <td>IDE</td>
    <td>VS Code</td>
  </tr>
</table>

## Instalasi Laravel via Composer

- Laravel diinstal secara global
  ```bash
    laravel new <nama_proyek>
  ```
- Arahkan ke folder proyek
  ```bash
    cd <nama_proyek>
  ```

## Instalasi Laravel Valet (Cukup sekali di awal)

- Instalasi secara global untuk OS Windows 10
  ```bash
    composer global require cretueusebiu/valet-windows
    valet install
  ```
- Ubah DNS IP4 menjadi 127.0.0.1 dan Alternate DNS 8.8.8.8
- Ubah DNS IP6 menjadi ::1
- Masuk ke folder yang akan digunakan sebagai server lokal dan inisilisasi laravel valet
  ```bash
    valet park
  ```

## Koneksi VDC

- Buat repo baru pada github sesuai dengan `<nama_proyek>` tanpa file `README.md`
- Inisialisasi git pada repo lokal
  ```bash
    git init
  ```
- Jalankan IDE
  ```bash
    code .
  ```
- Pada IDE, tambahkan file `README.md` untuk deskripsi proyek
- Tambahkan semua file yang dimodifikasi pada repo lokal
  ```bash
    git add .
  ```
- Commit modifikasi data
  ```bash
    git commit -m "first commit"
  ```
- Jika tidak ada penambahan file baru
  ```bash
    git commit -am "modification file <filename_with_ext>"
  ```
- Ubah branch repo lokal serupa dengan repo github
  ```bash
    git branch -M main
  ```
- Buat remote baru agar repo lokal terhubung dengan repo github
  ```bash
    git remote add origin <alamat_https_repo_github>
  ```
- Upload penambahan atau modifikasi data pada repo lokal ke repo github
  ```bash
    git push -u origin main
  ```
- Untuk melihat status git untuk penambahan atau modifikasi data
  ```bash
    git status
  ```
- Setiap kali ada penambahan atau modifikasi file, jalankan perintah berikut
  ```bash
    git add <filename>
    git commit -m "description"
    git push -u origin main
  ```

## Instalasi Starter Kit

```bash
  composer require laravel/jetstream
  php artisan jetstream:install livewire --teams
  npm install
  npm run dev
```

## Konfigurasi Database

- Buat Database sesuai dengan proyek
- Konfigurasi Postgresql pada file `.env`

  ```bash
    DB_CONNECTION=pgsql
    DB_HOST=127.0.0.1
    DB_PORT=5432
    DB_DATABASE=<nama_database>
    DB_USERNAME=<username>
    DB_PASSWORD=<password>
  ```

  > Pastikan bahwa ext `pdo_pgsql` dan `pgsql` diaktifkan pada file `php.ini` pada folder php yang digunakan

- Konfigurasi MySQL pada file `.env`

  ```bash
    DB_CONNECTION=mysql
    DB_HOST=127.0.0.1
    DB_PORT=3306
    DB_DATABASE=<nama_database>
    DB_USERNAME=<username>
    DB_PASSWORD=<password>
  ```

  > Ubah `charset` & `collation` pada file `config/database.php` dari `utf8mb4` menjadi `utf8`

- Migrasi database
  ```bash
    php artisan migrate
  ```

## Konfigurasi Timezone

- Inisialisasi variabel baru pada file `.env`
  ```bash
    APP_TIMEZONE=Asia/Jakarta
  ```
- Ubah variabel `timezone` pada file `.env`
  ```bash
    'timezone' => env('APP_TIMEZONE', 'UTC'),
  ```
- Bersihkan cache config
  ```bash
    php artisan config:clear
  ```
