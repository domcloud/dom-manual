---
title: Akses Remote
nav_order: 3
layout: default
parent: Hosting
---

# Akses Remote

### Adakah cara mengelola website selain melalui portal?

Melalui aplikasi lain, Anda dapat mengelola hosting tanpa harus melalui portal:

+ **Aplikasi FTP**, contoh [FileZilla Client](https://filezilla-project.org/download.php?show_all=1) digunakan untuk upload, download, dan mengelola file jarak jauh.
+ **Aplikasi Database**, contoh [HeidiSQL](https://www.heidisql.com/download.php) digunakan untuk mengelola database MySQL atau Postgres jarak jauh.
+ **Aplikasi SSH**, contoh [PuTTY](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html) digunakan untuk mengakses interaktif terminal jarak jauh.

Anda dapat melihat kredensial login tiap aplikasi tersebut dengan cara [memilih hosting aktif](https://portal.dom.my.id/user/hosting) anda, lalu **Atur Server Login**.

Semua tutorial dibawah menggunakan asumsi bahwa anda menggunakan Windows. Jika anda menggunakan Linux atau MacOS, anda dapat memilih software alternatif lain, karena tentu konsepnya tidak jauh berbeda antara software.

### Bagaimana cara menggunakan FileZilla Client?

Setelah anda install dan membuka aplikasi FileZilla, anda bisa mengakses FTP melalui cara berikut:

![](/images/filezilla.png){: width="80%"}

1. Klik ikon *Site Manager*
2. Klik *New Site*
3. Namai sesi tersebut, lalu dipilih
4. Isi host berdasarkan *Hostname* yang tertera di server login.
5. Isi port menjadi **21** (karena port FTP selalu 21).
6. Isi *Username* dan *Password* sesuai dengan yang tertera di server login.
7. Klik **Connect**.

Untuk akses berikutnya anda cukup mengulang step 1, 3 dan 7.

Jika anda ingin tidak menyimpan password FTP (karena bukan komputer pribadi, misalnya) anda dapat merubah *Logon Type* menjadi **Ask for Password** sebelum melakukan step 6.

Jika koneksi berhasil anda akan melihat panel kanan terisi, itu adalah file dalam server, sedangkan panel kiri adalah file komputer anda. Anda dapat menarik (drag) file atau folder dari kiri ke kanan untuk upload file, begitu juga sebaliknya untuk download file.

### Bagaimana cara menggunakan HeidiSQL?

Sebelum anda bisa mengatur Database jarak jauh, anda harus mengatur database agar dapat diakses secara jarak jauh melalui Portal Hosting. Caranya ialah:

1. Buka [Portal Hosting](/hosting/portal.html#bagaimana-cara-mengakses-portal-hosting-virtualmin)
2. Buka menu **Edit Databases**
3. Buka tab **Remote Hosts**
4. Tambahkan `%.%.%.%` pada baris dibawahnya `localhost`
5. Klik **Save**

Setelah anda install dan membuka aplikasi HeidiSQL, anda diminta untuk menambahkan sesi, sesuai dengan cara berikut:

![](/images/heidisql.png){: width="80%"}

1. Klik ikon *New*
2. Namai sesi tersebut, lalu dipilih
3. Pastikan *Network Type* sesuai. Apabila anda menggunakan PostgreSQL, ganti menjadi *PostgreSQL (TCP/IP)*.
4. Isi host berdasarkan *Hostname* yang tertera di server login.
5. Isi *Username* dan *Password* sesuai dengan yang tertera di server login.
6. Isi port menjadi **3306** untuk MySQL atau **5432** untuk PostgreSQL.
7. Klik **Open**. Apabila anda ditanya untuk menyimpan sesi, tekan *Yes*.

Untuk akses berikutnya anda cukup mengulang step 2 dan 7.

Jika anda ingin tidak menyimpan password Database, anda dapat mencentang *Prompt For Credentials* sebelum melakukan step 5.

Jika koneksi berhasil anda akan melihat daftar database anda di panel kiri. Anda dapat menambah tabel atau ekspor database melalui menu klik kanan. Saat anda memilih tabel dalam database. Anda dapat mengelola datanya melalui tab *Data*, atau tab *Table* untuk mengganti struktur tabelnya. 

Anda pun bisa mengeksekusi operasi SQL melalui Tab Query, atau mengimpor database melalui menu File > Load SQL File. HeidiSQL adalah software manajemen database yang cukup lengkap. Anda bisa melihat banyak tutorial di internet. Namun, perlu diingat bahwa membuat atau menghapus database, tetap harus dilalukan melalui portal hosting.

### Bagaimana cara menggunakan PuTTY untuk SSH?

PuTTY adalah software SSH dan telnet untuk Windows. Setelah anda menginstall PuTTY, anda dapat mengaksesnya melalui CMD. Caranya sebagai berikut.

1. Buka Command Prompt. Anda bisa lakukan ini melalui tombol Windows + R lalu *cmd*, enter. Atau anda bisa cari *cmd* di start menu.
2. Ketik perintah `ssh` diikuti dengan *username* yang tertera pada server login, contoh:
```
ssh mywebsite@sv01.dom.my.id
```
3. Jika anda pertama kali mengakses SSH, anda akan menjumpai pertanyaan ini. 
```
The authenticity of host 'sv01.dom.my.id (x.x.x.x)' can't be established.
ECDSA key fingerprint is SHA256:___________________________________________.
Are you sure you want to continue connecting (yes/no)?
```
Cukup ketik *yes* dan Enter.
4. Selanjutnya anda diminta password seperti berikut. 
```
mywebsite@sv01.dom.my.id's password: 
```
Ketik password yang tertera pada server login lalu tekan Enter.

Untuk akses berikutnya anda cukup mengulang step 1, 2 dan 7.

Jika koneksi berhasil anda akan dapat mengakses terminal dalam konteks kredensial server yang anda sedang gunakan. Anda dapat lakukan perintah terminal seperti biasa seperti `git`, `wget`, `composer`, dsb. Ingat bahwa akun SSH yang anda gunakan adalah akun terbatas. Anda tak bisa melalukan perintah yang menggunakan `sudo` atau apapun yang membutuhkan perubahan pada sistem secara global.
