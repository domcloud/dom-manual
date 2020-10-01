---
title: Fitur Hosting
parent: Referensi
nav_order: 2
layout: default
permalink: id/manage-fitur-hosting.html
---

# Fitur Hosting

Dalam Portal Hosting anda dapat menyalakan dan mematikan fitur hosting sesuai kebutuhan anda. Anda dapat mengecek ini melalui [Portal Hosting](/hosting/portal.html#apa-saja-menu-tersedia-di-virtualmin) lalu memilih menu **Edit Virtual Server**.

![](/images/features.png){: width="80%"}

Penjelasan tiap fitur:

+ **DNS Domain**: Mengaktifkan DNS server untuk hosting (untuk paket Lite keatas).<br>
<small>Jangan mematikan fitur ini apabila domain anda menggunakan Nameserver yang mengarah ke IP address hosting.</small>
+ **Apache Website**: Mengatifkan HTTP server untuk hosting.<br>
<small>Anda sebaiknya jangan mematikan fitur ini kecuali anda ingin mematikan website untuk publik.</small>
+ **Apache SSL Website**: Mengatifkan HTTPS server untuk hosting.<br>
<small>Secara default fitur ini mati. Anda [perlu mengaturnya](ssl.html) agar website anda dapat diakses melalui HTTPS.</small>
+ **Log File Rotation**: Mengatifkan Rotasi Log File (untuk paket Lite keatas).<br>
<small>Secara default fitur ini nyala agar menjaga konsumsi disk untuk logging rendah.</small>
+ **MySQL Database**: Mengatifkan database MySQL.<br>
<small>Secara default fitur ini mati. Anda dapat menyalakannya saat dibutuhkan.</small>
+ **PostgreSQL Database**: Mengatifkan database PostgreSQL.<br>
<small>Secara default fitur ini mati. Anda dapat menyalakannya saat dibutuhkan.</small>
+ **Webmin Login**: Mengatifkan akses portal.<br>
<small>Jangan mematikan fitur ini.</small>
+ **AWStats Reporting**: Mengatifkan laporan traffic AWStats (untuk paket Pro keatas).<br>
<small>Secara default fitur ini mati. Anda dapat menyalakannya saat dibutuhkan.</small>

Perlu diingat bahwa mematikan salah satu fitur diatas **mengakibatkan penghapusan data yang relevan secara permanen**. Jadi anda perlu berhati-hati saat merubah fitur-fitur hosting.

