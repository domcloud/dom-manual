---
title: Pembatasan Resource
parent: Dasar Hosting
nav_order: 3
layout: default
permalink: id/pembatasan-resource.html
---

# Pembatasan Resource

Karena DOM Cloud menggunakan konsep shared hosting, resource (sumber daya) yang dapat digunakan ialah terbatas, dan ada 4 aspek yang dibatasi:

### Storage

Storage adalah penyimpanan yang tersimpan di disk. Ini termasuk code aplikasi, file upload dan database.

Level storage yang anda dapatkan bermacam-macam, sesuai jenis paket, mulai dari 256 MB lalu 1 GB hingga 40 GB.

Tips agar website anda hemat storage:

+ Hapus file cache yang tidak penting, seperti log aplikasi, bekas instalasi composer/npm/yarn dan sejenisnya.
+ Gunakan fasilitas embed sebisa mungkin, contoh anda dapat mengupload foto di Google Photo, dokumen di Google Docs dan video di YouTube.
+ Jika anda berencana untuk menyediakan file upload untuk kapasitas besar, anda mungkin lebih baik menggunakan integrasi pihak ketiga seperti S3, Dropbox, Cloudinary dan semacamnya.

### Bandwidth

Bandwidth adalah ukuran data yang keluar dari server ke pengguna anda. Ukuran bandwidth ini dihitung per bulan dan berlaku untuk semua orang, tidak hanya anda aja. Ini juga bisa disimpulkan bahwa kebutuhan bandwidth anda semakin tinggi apabila jumlah orang yang mengakses website anda juga ikut meningkat seiring waktu.

Bandwidth yang kami tawarkan mulai dari 18 GB lalu 60 GB hingga 3000 GB. Perlu diketahui bahwa ini adalah bandwidth yang anda dapatkan selama 1 tahun, namun pembatasan dilakukan per bulan, alhasil anda akan dibatasi sebanyak 1 / 12 dari bandwidth per tahun tersebut.

Tips agar website anda hemat bandwidth:
+ Menggunakan CSS, Javascript dan konten gambar melalui hotlink ke eksternal/CDN server.
+ Menggunakan fasilitas embed (seperti yang dijelaskan tadi).
+ Memasang *Content Delivery Network* (CDN). CDN menghemat penggunaan bandwidth dengan cara meng-cache konten statis anda melalui server lain sehingga trafik tidak selalu mengenai server dan mengkonsumsi bandwidth server utama. Contoh disini ialah WordPress Jetpack dan Cloudflare.

Jika anda kehabisan bandwidth, anda juga dapat menambah bandwidth melalui data add-ons yang dihargai Rp. 5000 per 10 GB. Data add-ons tidak akan hangus atau terbagi menjadi beberapa bulan seperti bandwidth utama dari paket.

### RAM

RAM (atau memori) adalah resource yang sangat terbatas. Meski demikian, tidak ada pembatasan otomatis yang diukur dari penggunaan RAM, karena penggunaan memori dikelola oleh **PHP-FPM** (untuk website berbasis PHP) dan **Phusion Passenger** (untuk website berbasis Python/Ruby/Node.JS).

Agar dapat menghemat RAM, proses aplikasi website hanya berjalan saat trafik pertama diterima (cold start). Cold start ini hanya menambah sekitar 0.1 detik (untuk PHP) memulai, sehingga viewer mungkin tidak menyadari proses ini.

Kemudian apabila proses tersebut idle / tidak mendapat trafik selama 5 menit, maka proses tersebut akan dimatikan untuk menghemat memori, hingga dinyalakan lagi apabila mendapatkan trafik kembali.

Untuk standar penggunaan memori, PHP membutuhkan sekitar 50 MB, namun beberapa aplikasi lain seperti Python/Ruby/Node.js mungkin membutuhkan memori lebih, sekitar 100 MB. Hal tersebut masih dapat ditoleransi, asalkan tidak menembus hingga 1 GB lebih.

### CPU

Seperti RAM, CPU memang terbatas, namun untuk penggunaan proses website, hal tersebut dapat dimaklumi. Apabila aplikasi website anda melibatkan proses background atau cron job, anda perlu memberi batasan / timeout berapa detik aplikasi tersebut berjalan, sehingga proses berlanjutnya tidak mengganggu proses lain.

Perlu diingat bahwa sesuai dengan ketentuan layanan kami, anda tidak diperbolehkan menggunakan server untuk melakukan proses berat, termasuk konversi / streaming video, training / komputasi data, Bitcoin / cryptocurrency mining dan sejenisnya. Mohon menggunakan resource secara bijak, atau jika harus, menggunakan layanan lain untuk melakukan pekerjaan berat.

## Penindakan Batasan

Prinsip shared hosting ialah saling berbagi resource secara adil sehingga tidak merugikan satu dengan yang lainnya. Maka dari itu, setiap provider shared hosting pasti mempunyai sistem pembatasan sendiri-sendiri. Untuk kami, diantaranya:

### Pembatasan Otomatis

Kelebihan storage ataupun bandwidth akan membuat hosting anda dimatikan oleh portal yang secara otomatis dipantau di tiap jam. Saat dimatikan, segala akses, termasuk HTTP, FTP, SSH, Database dimatikan.

Anda dapat mengatasi kelebihan storage dengan cara upgrade atau mengurangi konten file melalui portal, sedangkan apabila anda kekurangan sisa bandwidth, anda dapat upgrade, membeli tambahan add-on kuota, atau menunggu jatah bulan depan.

Segera setelah bandwidth dan storage tersedia kembali, hosting anda kembali diaktifkan secara otomatis di jam berikutnya.

### Pembatasan karena Masa Tenggang

Apabila anda masa tenggang hosting anda terlewati, hosting anda dimatikan secara otomatis. Anda masih mempunyai waktu **hingga 2 minggu** sebelum hosting **dihapus secara otomatis** oleh sistem.

### Pembatasan Manual

Segala sesuatu yang melanggar penggunaan sesuai ketentuan layanan atau batas kewajaran penggunaan RAM atau CPU akan dimatikan secara manual. Anda mungkin atau tidak menerima notifikasi tentang hal tersebut sebelum kami bertindak tegas.

## Keterbatasan Teknis

Apabila anda memprediksi bahwa website anda akan mendapatkan trafik yang banyak, sangat dianjurkan untuk menggunakan *PHP* atau *Node.js*, karena Python dan Ruby tidak mendukung multi-threading, sehingga rentan gagal apabila overload.

Karena desain server yang monolitik *(satu server untuk satu website)*, shared hosting hanya cocok digunakan untuk ukuran website yang tidak tembus jutaan users per hari. Jika ini adalah problem anda, anda dapat melihat halaman berikutnya untuk memahami metode host lainnya yang mungkin cocok untuk anda.