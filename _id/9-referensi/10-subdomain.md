---
title: Subdomain
parent: Referensi
nav_order: 10
layout: default
permalink: id/subdomain.html
---

## Mengenal Subdomain dalam Virtualmin

Subdomain adalah "anak" dari domain. Sebuah website memerlukan subdomain apabila satu website dirasa tidak cukup. Misalkan, *yourwebsite.com* adalah halaman utama website anda. Anda dapat menggiring user anda ke *app.yourwebsite.com* untuk masuk ke bagian aplikasi website anda, atau *blog.yourwebsite.com* untuk bagian blog website anda, dan sebagainya.

Dalam Virtualmin, tiap subdomain memiliki folder server root, fitur, dan pengaturan yang berbeda. Istilah ini disebut dengan **Subserver**. Sebuah subserver tidak jauh berbeda dengan akun hosting yang baru, hanya saja harus tetap menggunakan basis domain induknya. Pemisahan antara antara domain induk dengan subserver lainnya ini penting agar data antar server dengan server lainnya tidak tercampur, membuat manajemen akses konten lebih mudah dan aman.

Subserver adalah fitur khusus untuk paket Lite keatas.

## Membuat Subserver

Anda dapat membuat subserver baru dengan membuka menu **Create Virtual Server**. Disebelah kanan anda dapat menulis nama domain (harus berakhiran dengan domain induk bersangkutan), deskripsi, dan template yang dipilih.

![](/images/subserver.png)

Dibawahnya anda dapat memilih fitur apa saja yang digunakan. Perbedaan dengan fitur yang biasanya ialah:

+ **Setup DNS Zone**: Tambahkan A record untuk subserver ke induk server.<br>
<small>Ini tidak membuat pengaturan DNS terpisah untuk subserver, dan juga A record tersebut ditambahkan otomatis; tidak terlihat di pengaturan DNS induk server.</small>
+ **Setup Website for domain**: Nyalakan website untuk subdomain dalam subserver.<br>
<small>Biasanya server root berada di */domains/domain_subserver/public_html*</small>
+ **Setup SSL Website too**: Nyalakan HTTPS untuk subdomain dalam subserver.<br>
<small>Pengaturan SSL akan terpisah akan domain induk, anda perlu request sertifikat baru dalam subserver setelah dibuat.</small>
+ **Create MySQL Database**: Nyalakan Pembuatan Database MySQL dalam Subserver.<br>
<small>Database antara subserver dengan server induk mempunyai hak akses yang sama. Anda tak bisa menyalakan fitur ini apabila database di server induk tidak dinyalakan</small>
+ **Create PostgreSQL Database**: Nyalakan Pembuatan Database PostgreSQL dalam Subserver.<br>
<small>Database antara subserver dengan server induk mempunyai hak akses yang sama. Anda tak bisa menyalakan fitur ini apabila database di server induk tidak dinyalakan</small>

