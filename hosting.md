---
title: Hosting
nav_order: 2
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



## Kapasitas Hosting

### Berapa Kapasitas Hosting yang tersedia?

Dengan paket Free (gratis), anda dapat mengisi tempat dalam hosting hingga **150 MB**. Ada pula opsi yang berbayar yang menambah kapasitas storage menjadi **500 MB**, **1.5 GB** dan **5 GB**.

Kapasitas Hosting yang dihitung termasuk berkas / file, database dan data server lainnya.

### Apa itu Kapasitas Bandwidth?

Kapasitas Bandwidth adalah batas jumlah data masuk dan keluar, mirip seperti data di handphone. Meski server secara teori mempunyai kapasitas data cepat dan unlimited, faktor lain juga perlu dihitung, misal konsumsi listrik dan panas yang ditimbulkan. 

Menghitung kebutuhan kapasitas bandwidth bergantung pada seberapa konten website yang anda gunakan. Jika anda ingin kalkulasi cepat, anda bisa memperkirakan untuk satu view memakan bandwidth rata-rata sekitar 250 KB. Dengan 10.000 view per hari anda dapat memakan bandwidth hingga 75 GB untuk satu bulan.

Dengan paket Free, anda mendapat jatah bandwidth hingga **5 GB** per bulan (30 hari). Ada pula opsi berbayar yang meningkatkan kapasitas bandwidth menjadi **15 GB**, **60 GB** dan **300 GB**.

### Bagaimana Jika Kapasitas Hosting terlampaui?

Hosting anda akan dimatikan secara *soft-state*, atau dengan kata lain tidak akan langsung gagal. Hosting anda akan dimatikan antara 1 hingga 6 jam oleh software bersih-bersih kami setelah kapasitas hosting terlampaui. Jika itu terjadi anda harus mengurangi atau upgrade kapasitas hosting hingga tidak melampaui batas lagi. Jika software bersih-bersih kami melihat hosting anda sudah dibawah batas, hosting anda akan dinyalakan kembali.

### Bagaimana Jika Kapasitas Bandwidth terlampaui?

Hosting anda akan langsung dimatikan. Jika itu terjadi anda harus menunggu batas 30 hari selesai atau upgrade kapasitas bandwidth. Jika bandwidth tersedia kembali maka hosting anda akan segera dinyalakan.

### Apakah saya dapat mengakses File dan Database saya saat Hosting Dimatikan?

Ya, untuk kasus kapasitas bandwidth atau hosting terlampaui, anda masih dapat mengakses data tersebut melalui portal.

Untuk kasus hosting dimatikan karena melampaui batas tempo, anda masih dapat mengakses data tersebut melalui portal. Namun hosting akan **dihapus secara permanen** apabila anda tidak memperbarui masa tempo hosting selama 2 minggu atau lebih.

### Apakah saya dapat notifikasi ketika Hosting Dimatikan?

Ya, anda akan mendapatkan notifikasi email oleh software bersih-bersih kami.

