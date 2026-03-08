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
