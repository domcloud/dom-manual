---
title: Dasar Hosting
nav_order: 1
layout: default
parent: Hosting
---


# Seputar tentang Hosting

### Apa itu Hosting?

Hosting adalah sarana komputer yang dibuat untuk melayani internet. Dengan membeli hosting berarti anda menyewa komputer tersebut untuk keperluan layanan internet anda (berikutnya kita sebut sebagai **server**). Server digunakan untuk memasang konten dan berbisnis di internet.

![](https://themezee.com/wp-content/uploads/2011/05/all-themes-900x600.png)

### Bagaimana Cara Hosting Bekerja?

Tidak sembarang komputer dapat dipakai server. Agar server dapat mengatasi banyaknya pengguna di internet, spesifikasi hardware dan koneksi internetnya harus cukup cepat.

 Oleh karena itu, agar biaya operasionalnya tetap terjangkau, digunakan konsep **Shared Hosting**, yakni menggunakan satu komputer untuk tempat beberapa website sekaligus.

### Bagaimana Cara Mendaftar Hosting?

Anda dapat memulai hosting secara gratis melalui DOM Cloud.

1. [Daftar Hosting Baru](https://portal.dom.my.id/user/hosting/create)
2. Masukkan username hosting, ini akan menjadi dasar alamat domain anda.<br>Misal dengan username `tokoku`, maka anda mendapatkan domain `tokoku.dom.my.id`.
3. Klik **Order Sekarang**
4. Hosting anda akan langsung aktif.

Setelah hosting anda aktif, anda bisa mengisi hosting tersebut dengan konten sesuai kebutuhan.

### Apa saja konten hosting

Banyak hal yang anda bisa isi dengan hosting aktif tersebut. Diantaranya:

1. Wordpress, untuk [blogging](wordpress.md) maupun [jual beli](woocommerce.md).
2. Website statis, untuk profil diri ataupun lembaga.
3. Website dinamis berbasis aplikasi, untuk merancang sistem online.

Didalam hosting website dikendalikan oleh [Apache Server](apache.md). Apache server dapat menjalankan program PHP secara default, namun anda juga dapat menambahkan program lain seperti Python, Ruby, dan Node.JS melalui [Phusion Passenger](apache.md#phusion-passenger).

## Portal Hosting

![](https://www.virtualmin.com/images/carousel-screenshots/virtual-server-options.png)

DOM Cloud menggunakan Virtualmin sebagai basis portal hosting.

### Bagaimana Cara Mengakses Portal Hosting?

Anda bisa mengaksesnya dengan cara [memilih hosting aktif](https://portal.dom.my.id/user/hosting) anda, lalu **Buka Portal Webmin**.

### Bagaimana Cara Mengisi Hosting?

Anda bisa mengisi hosting melalui portal, berikut caranya:

1. Buka Portal Webmin.
2. Setelah anda masuk ke portal webmin, buka tab **File Manager**
3. Navigasi ke folder `public_html`, di folder tersebut anda dapat mengisi hosting.

Dari sini anda dapat menggunggah file hosting dari melalui komputer anda menggunakan ZIP, lalu menggunggahnya melalui menu **File** > **Upload to current directory**.

Anda juga dapat menggunggah file hosting melalui [Aplikasi FTP](ftp.md).


