<h1 align="center">
Langkah-Langkah Pembuatan Web
</h1>

<table align="center">
  <tr>
    <td>Framework</td>
    <td>Laravel 8</td>
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

- Buat repo baru sesuai dengan `<nama_proyek>` tanpa file `README.md`
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

  jika tidak ada penambahan file baru, gunakan perintah :

  ```bash
    git commit -m "modification file <filename_with_ext>"
  ```

- Commit modifikasi data
  ```bash
    git commit -m "first commit"
  ```
