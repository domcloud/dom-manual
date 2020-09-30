---
title: Install SSL
parent: Referensi
nav_order: 3
layout: default
permalink: id/install-ssl.html
---

## Bagaimana HTTPS Berbeda dari HTTP

HTTPS adalah varian protokol yang aman (**S**ecure) daripada HTTP. HTTPS ada karena HTTP mempunyai masalah tersendiri, yakni data selama transmisi dari satu server ke server lain hingga sampai di browser dapat *dilihat* bahkan *dimodifikasi* oleh siapapun. Ini merupakan masalah privasi dan keamanan data yang serius bagi pengguna website anda.

Agar data selama transmisi aman, website anda dapat menggunakan protokol HTTPS. HTTPS mengenkripsi data selama transmisi, sehingga hanya anda dan server website yang dapat membukanya (dengan kata lain, selain kedua pihak, tidak ada yang dapat melihat data didalamnya). Agar memastikan bahwa data tersebut tidak dimodifikasi, HTTPS mensyaratkan bahwa komunikasi di validasi melalui *sertifikat digital* yang disebut sebagai **Sertifikat SSL**.

Adalah sebuah kewajiban untuk setiap website yang ingin menggunakan HTTPS, membuat Sertifikat SSL *melalui Agen SSL*, yang dinamakan sebagai **Certificate Authority** (CA). Agen CA ini tidak bisa sembarangan, hanya beberapa yang sudah diakui oleh browser umum, seperti COMODO, GeoTrust, RapidSSL, Symatec, dan lain sebagainya; Maka tidak heran jika anda menjumpai bahwa Sertifikat SSL itu tidak gratis, kecuali Let's Encrypt.

Jika anda tidak menggunakan Sertifikat SSL *melalui Agen SSL* tersebut, atau sertifikat sudah tidak valid, maka browser tidak akan mau mengakuinya, dan muncul peringatan *Koneksi anda tidak aman*. Saat memulai hosting HTTPS, anda menggunakan sertifikat yang dibuat oleh server sendiri, yang dinamakan *Self-signed Certificate*, sehingga muncul peringatan tersebut. Solusi dari permasalahan tersebut ialah dengan cara berikut:

## Mengaktifkan HTTPS

Dalam Portal Hosting anda dapat mengaktifkan HTTPS paling mudah dengan sertifikat SSL Let's Encrypt yang gratis dan otomatis:

1. Pertama, buka [pengaturan fitur hosting](/hosting/features.html) lalu nyalakan **Apache SSL Website**.
2. Kedua, [buka menu](/hosting/portal.html#apa-saja-menu-tersedia-di-virtualmin) Server Configuration > SSL Certificate, lalu pergi ke tab **Let's Encrypt** lalu klik **Request Certificate**
![](/images/letsencrypt.png)
3. Jika ada tulisan *Certificate successfully requested!* berarti operasi tersebut berhasil dan website HTTPS anda sudah aktif secara langsung.

Sertifikat dari Let's Encrypt hanya bertahan sampai 90 hari, namun Portal akan meminta ulang (renewal) sertifikat tersebut setiap 2 bulan secara otomatis sehingga anda tidak perlu request lagi kecuali anda melakukan perubahan signifikan pada website anda.

## HTTPS Redirect

Jika anda ingin mengalihkan semua akses HTTP menjadi HTTPS, anda dapat mengaktifkannya [melalui menu](/hosting/portal.html#apa-saja-menu-tersedia-di-virtualmin) Server Configuration > Website Options, lalu pilih opsi *Redirect all requests to SSL site?* ke **Yes**.

Peralihan ini dilakukan menggunakan modifikasi pada pengaturan Apache pada server.

## Custom SSL

Jika anda tidak ingin setifikat dari Let's Encrypt atau sudah membeli SSL dari provider lain, anda dapat mengupload sertifikat custom untuk digunakan pada website, yakni melalui menu Configuration > SSL Certificate lalu pada tab **Update Certificate and Key**. Jika CA anda meminta anda melakukan *Certificate Signing Request* (CSR), anda dapat melakukannya pada tab **Create Signing Request** di menu yang sama.

Menggunakan SSL yang berbayar mempunyai keuntungan tambahan, yakni anda menggunakan sertifikat EV, sehingga nama company anda dapat muncul disamping tanda SSL. Selain itu masa sertifikatnya lebih tahan lama, biasanya sekitar 1 tahun atau lebih.

![](https://www.tunetheweb.com/assets/images/security/DV_OV_EV_certificates.png)## Troubleshooting

### Request Certificate Let's Encrypt Gagal

1. Pastikan website anda aktif atau benar-benar bisa diakses melalui browser.
2. Pastikan ada folder `.well-known` di server root (biasanya */public_html/.well-known*), anda dapat mengeceknya di File Manager.
3. Pastikan `.htaccess` anda tidak memblokir akses file statis didalam folder `.well-known` atau file statis lainnya.

Jika anda sudah mengecek namun gagal, mungkin saat itu kami terbatas *rate-limit* request dari Let's Encrypt. Cobalah minimal 15 menit lagi.

### Muncul Error saat mengakses HTTPS

Jika anda mendapatkan error *Koneksi Anda tidak pribadi*, anda mungkin:

1. Belum mengaktifkan sertifikat SSL (dari Let's Encrypt atau Certificate Authority Lainnya)
2. Sertifikat SSL anda sudah kadarluarsa (atau pengaturan waktu di komputer anda salah)
3. Anda baru saja mengganti URL atau menambah subdomain baru namun belum merequest seritifkat SSL untuk domain baru tersebut.

Anda dapat memperbarui sertifikat SSL anda secara manual.

### Muncul Tulisan Not Secure / Tidak Aman meski SSL sudah valid

Beberapa elemen dari halaman tersebut mungkin memuat konten dari HTTP (bisa saja script, stylesheet, gambar atau media lain). Istilah masalah disini ialah *Mixed Content*. Anda harus memastikan semua URL tidak ada konten yang dimulai dengan kata `http://` (dengan cara melihat sumber HTML dari view-source: atau Ctrl+U).
