---
title: Hosting
nav_order: 2
---

# Seputar tentang Hosting

### Apa itu Hosting?

Hosting adalah sarana komputer yang dibuat untuk melayani internet, seperti website dan email. Dengan membeli hosting berarti anda menyewa komputer tersebut untuk keperluan layanan internet anda, seperti memasang website untuk blogging atau jual beli online.

### Bagaimana Cara Hosting Bekerja?

Saat anda menjelajahi website seperti `tokoku.co.id`, komputer akan menerjemahkannya menjadi sebuah alamat IP Address yang mempunyai format `xxx.xxx.xxx.xxx`; penerjemahan ini dibantu oleh [DNS](domain.md) yang didaftarkan oleh masing-masing domain. Setelah IP Address ditemukan komputer akan mengirim data request HTTP kepada server yang menempati alamat IP tersebut untuk diproses dan membalas request dalam bentuk HTML yang bisa ditampilkan oleh browser.

Pada umumnya, sebuah server yang mempunyai satu alamat IP bisa menghosting beberapa atau bahkan puluhan website dalam domain yang berbeda sekaligus. Hal ini disebut sebagai **Shared Hosting** dan banyak provider hosting berbasis pada konsep ini agar biaya hosting dapat murah dan terjangkau.  

### Bagaimana Cara Mendaftar Hosting?

Anda dapat memulai hosting secara gratis melalui DOM Cloud.

1. [Daftar Hosting Baru](https://portal.dom.my.id/user/hosting/create)
2. Masukkan username hosting, ini akan menjadi basis domain anda.<br>Misal dengan username `tokoku`, maka anda mendapatkan domain `tokoku.dom.my.id`.
3. Klik **Order Sekarang**
4. Hosting anda akan langsung aktif.

Setelah hosting anda aktif, anda bisa mengisi hosting tersebut sesuai kebutuhan.

### Hosting bisa di isi apa saja?

Banyak hal yang anda bisa isi dengan hosting aktif tersebut. Diantaranya:

1. Wordpress, untuk [blogging](wordpress.md) maupun [jual beli](woocommerce.md).
2. Website statis, untuk profil diri ataupun lembaga.
3. Website dinamis berbasis PHP, untuk merancang sistem online.

Didalam hosting website dikendalikan oleh [Apache Server](apache.md).

### Bagaimana Cara Mengisi Hosting?

Anda bisa mengisi hosting melalui portal, berikut caranya:

1. Pilih hosting aktif anda, lalu **Buka Portal Webmin**.
2. Setelah anda masuk ke portal webmin, buka tab **File Manager**
3. Navigasi ke folder `public_html`, di folder tersebut anda dapat mengisi hosting.

Dari sini anda dapat menggunggah file hosting dari melalui komputer anda menggunakan ZIP, lalu menggunggahnya melalui menu **File** > **Upload to current directory**.

Anda juga dapat menggunggah file hosting melalui [Aplikasi FTP](ftp.md).



## Kapasitas Hosting

 ### Berapa Kapasitas Hosting yang tersedia?

Dengan paket Free (gratis), anda dapat mengisi tempat dalam hosting hingga **150 MB**. Ada pula opsi yang berbayar yang menambah kapasitas storage menjadi **500 MB**, **1.5 GB** dan **5 GB**.

### Apa itu Kapasitas Bandwidth?

