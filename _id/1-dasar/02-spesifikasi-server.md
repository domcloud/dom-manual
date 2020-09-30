---
title: Spesifikasi Server
parent: Dasar Hosting
nav_order: 2
layout: default
permalink: id/spesifikasi-hosting.html
---

# Spesifikasi Server

Untuk menjadi sebuah server, komputer tersebut harus menyala 24 jam dan memiliki alamat IP statis (tidak berubah-ubah), juga harus mempunyai spesifikasi yang tinggi agar kuat menerima trafik pengguna website yang tinggi.

DOM Cloud menerapkan konsep **Shared Hosting** yang berarti satu komputer (server) dipakai untuk menjalankan banyak website. Konsep ini mempunyai banyak keunggulan seperti menjadikan biaya hosting yang terjangkau dan resource server menjadi dapat digunakan lebih efektif. Selain itu, agar konektifitas website tetap optimal, kami menempatkan insfrastruktur kami pada **Digital Ocean**.

![](https://nixpoin.com/img/digitalocean-logo.jpg)

Digital Ocean (DO) adalah cloud provider yang melayani insfrastruktur server. Istilah mudahnya, server yang kami gunakan untuk melayani DOM Cloud merupakan milik DO, kami pun "menyewa" server dari DO, karena dilihat dari perspektif biaya dan performa, jauh lebih murah dan fleksibel, daripada harus membangun insfrastruktur server sendiri.

Selain itu, biaya host server di Digital Ocean sangat terjangkau, belum lagi claim uptime mereka hingga 99.99%.

Dari sini mungkin anda bertanya, bukannya lebih murah kalau anda hosting di DO saja? Jawabannya, tidak bisa sesederhana itu.

![](https://blogs.bmc.com/wp-content/uploads/2017/09/iaas-paas-saas-comparison-1024x759.jpg)

Dilihat dari sini, bisa diibaratkan Digital Ocean merupakan **IaaS (Infrastucture-as-a-Service)**, mereka memberikan basis infrastruktur server yakni akses **Virtual Machine** (VM) yang serasa seperti komputer sendiri. Namun komputer sendiri bukan seluruh ceritanya, anda masih butuh pengetahuan tentang bagaimana merubah komputer tersebut menjadi sebuah server dengan bermacam-macam software diinstall. Inilah dimana DOM Cloud berperan sebagai **Paas (Platform-as-a-Service)**, kami yang menyiapkan segala kebutuhan software yang dibutuhkan, seperti *Apache, PHP, MySQL* dan semacammnya; sehingga anda cukup memikirkan bagian
websitenya. Dengan kata lain, anda yang berperan sebagai **SaaS (Software-as-a-Service)**, pembuatan website untuk customer website anda sendiri.

## Kapan Anda Harus menangani server sendiri



## Lokasi Server DOM Cloud

Digital Ocean mempunyai banyak titik lokasi server, namun untuk DOM Cloud sendiri, hanya memiliki titik server berikut:

| Server | Endpoint | Spesifikasi Server | Domain Default |
|---|---|---|
| Singapore A | sga.domcloud.id | 2 vCPU - 4 GB RAM | .dom.my.id |

Apabila anda ingin request lebih banyak lokasi server, anda dapat menghubungi kami.

Selanjutnya, anda akan tahu bagaimana kami membagi resource dan membatasi penggunaan hosting sesuai dengan paket yang anda beli.