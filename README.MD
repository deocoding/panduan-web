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
    <td>Postgresql</td>
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
- Jika tidak ada penambahan file baru, gunakan perintah :
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
- Uplod penambahan atau modifikasi data pada repo lokal ke repo github
  ```bash
    git push -u origin main
  ```
