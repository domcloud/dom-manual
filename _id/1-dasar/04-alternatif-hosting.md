---
title: Media Hosting Alternatif
parent: Dasar Hosting
nav_order: 4
layout: default
permalink: id/media-hosting-alternatif.html
---


## Media Hosting Alternatif

Selain menggunakan DOM Cloud atau layanan shared hosting **(Platform-as-a-Service)** sejenis, ada alternatif lain tentang hosting website sesuai budget dan kebutuhan website anda.

---

![](https://www.cloudflare.com/img/learning/serverless/serverless-vs-containers/serverless-computing-deploy-speed-comparison.svg)

### On Premise Server (Traditional)

On Premise bisa dibilang sebagai cara tradisional mengadakan website. Yakni, anda mengatur semua aspek hosting, termasuk bangunan, datacenter, storage, replikasi, backup, software dan semacamnya.

Cara seperti ini mempunyai banyak tantangan, diantaranya:

+ Biaya budget dan waktu membangun insfrastruktur
+ Maintenance ekstra termasuk bangunan, listrik dan konektivitas
+ Anda yang mengatur virtualisasi dan software server sendiri
+ Lebih rentan terhadap serangan cyber lewat fisik atau bencana alam
+ Biaya dan preparasi untuk scale up kadang membutuhkan waktu lama
+ Server anda akan crash apabila trafik tiba-tiba meningkat tajam

Meski cukup sulit, on promise menjajikan hal-hal berikut yang tidak ada di media hosting lainnya:

+ Keamanan data, karena tidak ada pihak lain yang terlibat.
+ Spesifikasi selalu tinggi, dan tidak terbagi oleh pengguna lain.
+ Biaya operasional lebih rendah daripada dedicated server (dalam jangka panjang)

On Promise cocok apabila anda membangun sistem yang didalamnya ada data penting atau rahasia, termasuk data pemerintahan atau sensitif lainnya. Jika tidak, anda akan jauh menghemat biaya membangun sistem melalui media lainnya.

### Virtual Machine (VM/VPS) / Infrastructure-as-a-Service

Dengan menyewa VM melalui datacenter ternama, anda memberikan tanggung jawab infrastruktur ke pihak lain, sehingga anda hanya perlu fokus ke instalasi dan maintenance software yang dibutuhkan. Namun tentu, mempunyai VM sendiri mempunyai tantangan berikut:

+ Biaya tidak kecil, apalagi jika anda membutuhkan spesifikasi host besar
+ Anda yang mengatur instalasi dan maintenance kebutuhan software sendiri
+ Anda masih akan terkendala apabila trafik meningkat tajam

Mempunyai VM sendiri akan masuk akal jika anda menggunakan software yang tidak didukung oleh banyak provider shared hosting, atau anda tidak ingin terlibat dengan pembatasan resource ataupun tidak ingin performa web anda terganggu oleh pengguna host lain (jika menggunakan dedicated VM). Namun desain molitik *(Satu server untuk satu website)* dari VM ini pasti akan mengganggu anda suatu saat apabila trafik website anda sudah mencapai angka jutaan per hari.

Dimana anda bisa menyewa VM? Anda dapat menyewa VM di provider cloud terkemuka seperti [Digital Ocean](https://m.do.co/c/facab6f3ac67), Vultr, AWS, GCP, Azure, AWS dan sebagainya. Beberapa provider hosting yang menyediakan VPS atau Dedicated Server meskipun bisa dibilang harga yang ditawarkan cukup liar perbedannya.

### Containers / Kubernetes-as-a-Service

![](https://i2.wp.com/www.docker.com/blog/wp-content/uploads/Blog.-Are-containers-..VM-Image-1.png?fit=1600%2C680&ssl=1)

Containers adalah solusi yang cukup populer agar website anda scale up dengan mudah. Containers ada untuk menjawab problem dari sistem monolitik dari VM dengan perbedaan sebagai berikut:

+ Containers dan VM adalah sama-sama virtualisasi dengan hak akses sistem penuh dengan ruang mereka sendiri-sendiri, namun tiap VM dapat berbeda beda OS/Kernel sedangkan container tidak.
+ Untuk memulai VM anda cukup memilih template OS yang dimulai, sedangkan untuk container anda juga harus mempersiapkan script yang dijalankan untuk menginstall software dan menyalakan server web sebelum memulai.
+ Tidak seperti VM, Container tidak dapat dimodifikasi ditempat. Apabila anda ingin mengupdate code dalam container anda harus menghapus dan memulai ulang container.

Dengan sifat *immutability* inilah, anda tidak cuma hanya bisa membuat satu container, tapi banyak container sekaligus, dan trafik website dapat dibagi sesuai dengan jumlah container yang ada, yang dikenai dengan sistem **Load Balancer**. Agar distribusi dan pengelolaan banyak container lebih mudah, anda pasti akan mengenal istilah **Kubernetes**, itulah istilah software yang digunakan untuk mengelola containers secara kelompok / cluster. Dengan Containers dan Kubernetes, anda dapat mengelola sistem web yang jauh lebih kompleks dan mampu scale up hingga jutaan pengguna per hari.

Meskipun demikian, merubah sistem tradisional ke container tidak semudah itu, karena dalam container, storage yang permanen seperti database dan file upload harus menggunakan layanan tambahan yang bisa anda baca dibawah.

Dimana anda bisa menyewa Containers? [**Docker**](https://docker.com/) adalah tempat yang paling cocok untuk menggunakan Container. Mereka juga mempunyai banyak resource untuk anda meresapi perbedaan Containers dengan host monolitik yang tradisional.

### Serverless / Function-as-a-Service

![](https://www.simform.com/wp-content/uploads/2018/08/Serverless-Examples-with-AWS-Lambda-Use-Cases.png)

Serverless adalah terobosan sistem web yang paling kompleks namun dapat sangat mudah untuk scale up hingga berapapun load website yang anda terima. Serverless memiliki konsep yang mirip seperti containers, namun kali tanpa menginstall software. Anda hanya diminta untuk menyiapkan kode server (dengan kata lain, *fungsi*) yang akan dieksekusi. Agar desain serverless ini berguna dan efektif, anda juga harus menyiapkan banyak integrasi dengan banyak produk di provider cloud, seperti berikut:

Dengan desain FaaS, tidak ada lagi delay karena menunggu instalasi container selesai. Selain itu, biaya operasional serverless sangat terjangkau, karena tidak seperti Containers yang harus ON 24 jam,  FaaS hanya ditarif dari berapa penggunaan CPU / lama fungsi tersebut berjalan.

Namun, merubah desain container menjadi function pun sulit, atau bisa dibilang, harus memulai dari nol untuk merubah desain server menjadi serverless. Dan apabila anda mendesain website serverless, anda mungkin harus mendesainnya dengan matang, sehingga tidak terlalu banyak fungsi yang membuat maintenance cukup susah.

# Kesimpulan


| Aspek | On Premise | IaaS | PaaS | KaaS | FaaS |
|---|---|---|---|---|---|
| **Penentu Biaya** | Infrastruktur Maintenance | Spesifikasi Storage | Storage | # Container | CPU Runtime |
| **Bebas Bandwidth** | Ya | Tidak | Tidak | Tidak | Tidak
| **Akses Root** | Ya | Ya | Tidak | Tidak | Tidak
| **Akses Storage** | Ya | Ya | Ya | Tidak | Tidak
| **Bisa Install** | Ya | Ya | Ya | Ya | Tidak
| **Server Cloud** | Tidak | Ya | Ya | Ya | Ya
| **Konfigurasi Cepat** | Tidak | Tidak | Ya | Ya | Ya
| **Load Balancer** | Tidak | Tidak | Tidak | Ya | Ya
| **Scale Otomatis** | Tidak | Tidak | Tidak | Tidak | Ya

### Daftar Produk Layanan Cloud dari Providers

| Produk | DO | AWS | GCP | Azure |
|---|---|---|---|---|
|FaaS|-|[Lambda](https://aws.amazon.com/lambda/)|[Cloud Functions](https://cloud.google.com/functions)|[Functions](https://azure.microsoft.com/en-us/services/functions/)|
|KaaS|[Kubernetes](https://digitalocean.com/products/kubernetes/)|[EKS](https://aws.amazon.com/eks/)|[Kubernetes Engine](https://cloud.google.com/kubernetes-engine?hl=id)|[Kubernetes Service](https://azure.microsoft.com/en-us/services/kubernetes-service/)
|IaaS|[Droplets](https://www.digitalocean.com/products/droplets/)|[EC2](https://aws.amazon.com/ec2/)|[Cloud Engine](https://cloud.google.com/compute)|[Virtual Machines](https://azure.microsoft.com/en-us/services/virtual-machines/)
|Storage|[Spaces](https://www.digitalocean.com/products/spaces/) <br> [Block Storage](https://digitalocean.com/products/block-storage/)|[S3](https://aws.amazon.com/s3/) <br> [EBS](https://aws.amazon.com/ebs/) <br> [EFS](https://aws.amazon.com/efs/) | [Cloud Storage](https://cloud.google.com/storage?hl=id) <br> [Cloud Filestore](https://cloud.google.com/filestore?hl=id) |[Blob](https://azure.microsoft.com/en-us/services/storage/blobs/) <br> [File](https://azure.microsoft.com/en-us/services/storage/files/)
|Database|[Databases](https://www.digitalocean.com/products/managed-databases/)|[RDS](https://aws.amazon.com/rds/) <br> [DynamoDB](https://aws.amazon.com/dynamodb/) <br> [ElastiCache](https://aws.amazon.com/elasticache/) | [Cloud SQL](https://cloud.google.com/sql?hl=id) <br> [Firestore](https://cloud.google.com/firestore?hl=id) <br> [Memorystore](https://cloud.google.com/memorystore?hl=id) | [SQL Database](https://azure.microsoft.com/en-us/services/sql-database/) <br> [Table Storage](https://azure.microsoft.com/en-us/services/storage/tables/) <br>[Cache for Redis](https://azure.microsoft.com/en-us/services/cache/)
