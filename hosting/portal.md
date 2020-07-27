---
title: Akses Portal
nav_order: 2
layout: default
parent: Hosting
---


# Akses Portal Hosting

### Apa itu Portal Hosting?

Portal Hosting adalah website khusus untuk mengatur konten website anda. Portal hosting tidak peruntukkan untuk publik dan anda sendiri harus menjaga kerahasiaan akses portal anda sendiri agar tidak disalah gunakan.

### DOM Cloud memakai Portal Hosting apa?

![](https://www.virtualmin.com/images/carousel-screenshots/virtual-server-options.png)

DOM Cloud menggunakan Virtualmin sebagai basis portal hosting. Virtualmin mempunyai fitur yang cukup lengkap dan tampilan yang lebih mudah untuk dipahami.

### Bagaimana Cara Mengakses Portal Hosting (Virtualmin)?

Anda bisa mengaksesnya dengan cara [memilih hosting aktif](https://portal.dom.my.id/user/hosting) di portal akun anda, lalu **Buka Portal Webmin**.

Jika anda mengalami kendala **Error - No cookies**, anda bisa [membuka portal ini](https://sv01.dom.my.id:8443/session_login.cgi) dulu lalu klik *Buka Portal Webmin* lagi.

Perlu diingat bahwa Portal Hosting (Virtualmin) berbeda dengan Portal Akun (portal.dom.my.id). Jika anda menemukan kata *portal hosting*, berarti portal yang kami maksud ialah portal Virtualmin, begitu pula sebaliknya.

### Apa saja menu tersedia di Virtualmin?

<div style="float:left;margin-right:2em;margin-top:1em"><img src="/images/virtualmin-menus.png" alt="Bagan menu"></div>

#### **Pengaturan Umum**
+ **Create Virtual Server**: Menambah server untuk subdomain
+ **Edit Virtual Server**: Mengatur fitur server yang dinyalakan
+ **Edit Users**: Mengatur akun tambahan untuk akses FTP dan Database[^1]
+ **Edit Databases**: Mengelola Database MySQL dan Postgres dalam server[^3]
+ **File Manager**: Mengelola file dalam server
#### **Administration Options**
+ **Disk Usage**: Cek penggunaan kapasitas disk storage
+ **Excluded Directories and DBs**: Mengatur folder database yang di skip dalam Backup
+ **Manage Extra Admins**: Mengatur akun tambahan untuk manajemen website dari portal[^1]

#### **Server Configuration**
+ **Change Password**: Mengganti password portal
+ **DNS Records**: Mengelola aturan DNS dalam server[^2]
+ **PHP Versions**: Mengatur versi PHP yang ingin digunakan
+ **SSL Certificates**: Mengelola sertifikat SSL yang sedang digunakan[^4]
+ **Website Options**: Mengatur konfigurasi website yang dasar
+ **Website Redirects**: Mengelola endpoint yang digunakan untuk redirect

#### **Logs and Reports**
+ **AWStats Configuration**: Mengatur Konfigurasi Laporan AWStats[^5]
+ **AWStats Reports**: Melihat laporan traffic dari AWStats[^5]
+ **Apache Access Logs**: Melihat log traffic dalam server
+ **Apache Error Logs**: Melihat log error dalam server
+ **Bandwidth Graph**: Melihat laporan penggunaan bandwidth

[^1]: Hanya terbuka untuk hosting paket Business keatas
[^2]: Hanya terbuka untuk hosting paket Lite keatas, dan fitur DNS dinyalakan
[^3]: Hanya terbuka apabila fitur database MySQL atau Postgres dinyalakan
[^4]: Hanya terbuka apabila fitur Apache SSL Website/HTTPS dinyalakan
[^5]: Hanya terbuka untuk hosting paket Pro keatas, dan fitur AWStats dinyalakan


<div style="clear:both"></div>
