# Lab7Web_

# README – Praktikum Web 2 (CodeIgniter 4)

## Deskripsi

Praktikum ini bertujuan untuk mempelajari penggunaan **Framework CodeIgniter 4** dalam pembuatan aplikasi web sederhana. Pada praktikum ini mahasiswa mempelajari konsep **MVC (Model, View, Controller)**, routing, serta pembuatan tampilan halaman web menggunakan template layout.

---

## Nama & Kelas

* Nama: Mochammad Hafilla Dasuki
* NIM: 312410375
* Kelas: I.24.1C Reguler


## Langkah Praktikum

### 1. Instalasi CodeIgniter

* Download CodeIgniter dari website resmi.
* Extract file ke folder **htdocs** pada XAMPP.
* Ubah nama folder menjadi **ci4**.
* Jalankan project melalui browser:

```
http://localhost/lab11_ci/ci4/public
```

---

### 2. Mengaktifkan Mode Debugging

Agar pesan error dapat terlihat jelas, ubah konfigurasi pada file `.env`.

```
CI_ENVIRONMENT = development
```

---

### 3. Membuat Routing

Routing digunakan untuk menentukan halaman yang akan diakses.
File routing berada di:

```
app/Config/Routes.php
```

Contoh routing yang dibuat:

```php
$routes->get('/about', 'Page::about');
$routes->get('/contact', 'Page::contact');
$routes->get('/faqs', 'Page::faqs');
```

---

### 4. Membuat Controller

Controller dibuat pada folder:

```
app/Controllers/Page.php
```

Contoh kode:

```php
<?php

namespace App\Controllers;

class Page extends BaseController
{
    public function about()
    {
        echo "Ini halaman About";
    }

    public function contact()
    {
        echo "Ini halaman Contact";
    }

    public function faqs()
    {
        echo "Ini halaman FAQ";
    }
}
```

---

### 5. Membuat View

View digunakan untuk menampilkan tampilan halaman web.

Lokasi file:

```
app/Views/about.php
```

Contoh kode:

```php
<h1><?= $title; ?></h1>
<p><?= $content; ?></p>
```

---

### 6. Membuat Layout

Layout dibuat menggunakan template **header** dan **footer** agar tampilan halaman lebih rapi dan konsisten.

File yang dibuat:

* `app/Views/template/header.php`
* `app/Views/template/footer.php`

---

## Hasil

Website berhasil menampilkan beberapa halaman seperti:

* Home
* About
* Contact
* FAQ

Semua halaman menggunakan konsep **MVC** dan memiliki layout yang sama.

---


<img width="1902" height="918" alt="image" src="https://github.com/user-attachments/assets/d6ac2c76-65e9-404a-95d4-e5b3c783b577" />


## Kesimpulan

Framework **CodeIgniter 4** membantu proses pengembangan aplikasi web menjadi lebih terstruktur dengan menggunakan konsep MVC yang memisahkan antara logika program, data, dan tampilan.



## PRATIKUM 2 ## 
# Aplikasi Artikel - CodeIgniter 4

## Deskripsi

Aplikasi ini merupakan sistem sederhana berbasis web yang digunakan untuk mengelola data artikel. Dibangun menggunakan framework CodeIgniter 4, aplikasi ini menerapkan konsep MVC (Model, View, Controller) sehingga struktur kode menjadi lebih terorganisir dan mudah dikembangkan.

## Tujuan

Tujuan pembuatan aplikasi ini adalah untuk memahami dasar pengembangan web menggunakan framework, khususnya dalam pengelolaan data (CRUD) serta implementasi koneksi database.

## Fitur Utama

* Menampilkan daftar artikel
* Melihat detail artikel
* Menambah data artikel
* Mengubah data artikel
* Menghapus data artikel
* Halaman admin untuk pengelolaan data

## Teknologi yang Digunakan

* PHP
* CodeIgniter 4
* MySQL
* HTML & CSS

  <p>SCREENSHOOT HASIL</p>
  <img width="1877" height="967" alt="Screenshot 2026-03-12 000044" src="https://github.com/user-attachments/assets/e3b91667-1af5-4a57-9bcf-f9b096c84f3a" />
  <img width="722" height="491" alt="Screenshot 2026-04-01 211732" src="https://github.com/user-attachments/assets/ee2d72ce-4357-4f32-9305-8e5e4aecf6d7" />
  <img width="1739" height="857" alt="Screenshot 2026-04-01 230242" src="https://github.com/user-attachments/assets/defec035-f2f1-4787-8a11-52336bc0ff81" />
  <img width="1740" height="865" alt="Screenshot 2026-04-01 230704" src="https://github.com/user-attachments/assets/c9d459bc-7b2d-4159-80ff-a085a60f483f" />





## Penutup

Aplikasi ini masih bersifat sederhana dan dapat dikembangkan lebih lanjut dengan menambahkan fitur seperti autentikasi pengguna, upload gambar, dan tampilan yang lebih interaktif.


## PRATIKUM 3 ##

# Aplikasi Artikel - CodeIgniter 4

## Deskripsi

Aplikasi ini merupakan sistem sederhana untuk mengelola data artikel berbasis web menggunakan CodeIgniter 4. Aplikasi ini menerapkan konsep MVC sehingga struktur program menjadi lebih rapi dan mudah dikembangkan.

## Tujuan

Praktikum ini bertujuan untuk memahami penggunaan View Layout dan View Cell dalam membangun tampilan yang terstruktur, konsisten, dan modular.

## Fitur

* Menampilkan daftar artikel
* Detail artikel
* Tambah, ubah, dan hapus artikel
* Halaman admin
* Sidebar artikel terkini

## Konsep Utama

* **View Layout** digunakan untuk menyatukan tampilan (header, navbar, footer) agar tidak berulang.
* **View Cell** digunakan untuk membuat komponen seperti sidebar yang bisa dipakai di berbagai halaman.

## Kesimpulan

Penggunaan View Layout dan View Cell membantu membuat tampilan aplikasi lebih rapi, efisien, dan mudah dikembangkan.

# JAWABAN SOAL #

## Jawaban Tugas

### 1. Manfaat View Layout

View Layout digunakan untuk membuat tampilan aplikasi lebih rapi dan konsisten. Dengan layout, bagian seperti header, navbar, dan footer tidak perlu ditulis berulang, sehingga lebih efisien dan mudah dikelola.

---

### 2. Perbedaan View Cell dan View Biasa

View biasa digunakan untuk menampilkan halaman utama yang datanya dikirim dari controller.

Sedangkan View Cell digunakan untuk membuat komponen kecil yang dapat digunakan kembali, seperti sidebar, dan dapat mengambil data sendiri tanpa melalui controller utama.

---

### 3. Fungsi View Cell dalam Aplikasi

View Cell berfungsi untuk menampilkan bagian tertentu dari halaman yang bersifat dinamis dan dapat digunakan di berbagai halaman. Contohnya adalah menampilkan daftar artikel terbaru pada sidebar.

---

### 4. Keuntungan Menggunakan Layout dan View Cell

Keuntungan utamanya adalah membuat kode lebih rapi, mengurangi pengulangan kode, serta mempermudah pengembangan dan pemeliharaan aplikasi. Selain itu, tampilan menjadi lebih konsisten di setiap halaman.

---

### 5. Modifikasi View Cell

View Cell dapat dimodifikasi dengan menambahkan kondisi pada query untuk menampilkan data tertentu sesuai kebutuhan.

Contoh:

```php id="dzrtdc"
$artikel = $model
    ->where('status', 1)
    ->orderBy('id', 'DESC')
    ->limit(5)
    ->findAll();
```

Dengan modifikasi ini, data yang ditampilkan menjadi lebih spesifik.

