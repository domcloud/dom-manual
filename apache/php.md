---
title: PHP Engine
nav_order: 4
layout: default
parent: Apache
---

### Versi PHP dan Ekstensi yang didukung

DOM Cloud mendukung PHP versi 7.2 (default), 7.3 dan 7.4 dengan daftar ekstensi sebagai berikut:

|  |  |  |  |  |  |
|-|-|-|-|-|-|
| [bcmath](https://www.php.net/manual/en/book.bc.php) | [bz2](https://www.php.net/manual/en/book.bzip2.php) | [calendar](https://www.php.net/manual/en/book.calendar.php) | cgi-fcgi | Core | [ctype](https://www.php.net/manual/en/book.ctype.php) |
| [curl](https://www.php.net/manual/en/book.curl.php) | [date](https://www.php.net/manual/en/book.datetime.php) | [dom](https://www.php.net/manual/en/book.dom.php) | [exif](https://www.php.net/manual/en/book.exif.php) | [fileinfo](https://www.php.net/manual/en/book.fileinfo.php) | [filter](https://www.php.net/manual/en/book.filter.php) |
| [ftp](https://www.php.net/manual/en/book.ftp.php) | [gd](https://www.php.net/manual/en/book.image.php) | [gettext](https://www.php.net/manual/en/book.gettext.php) | [hash](https://www.php.net/manual/en/book.hash.php) | [iconv](https://www.php.net/manual/en/book.iconv.php) | [igbinary](https://pecl.php.net/package/igbinary) |
| [intl](https://www.php.net/manual/en/book.intl.php) | [json](https://www.php.net/manual/en/book.json.php) | [ldap](https://www.php.net/manual/en/book.ldap.php) | [libxml](https://www.php.net/manual/en/book.libxml.php) | [mbstring](https://www.php.net/manual/en/book.mbstring.php) | [memcached](https://www.php.net/manual/en/book.memcached.php) |
| [msgpack]() | [mysqli](https://www.php.net/manual/en/book.mysqli.php) | [mysqlnd](https://www.php.net/manual/en/book.mysqlnd.php) | [openssl](https://www.php.net/manual/en/book.openssl.php) | [pcntl]() | [pcre](https://www.php.net/manual/en/book.pcre.php) |
| [PDO](https://www.php.net/manual/en/book.pdo.php) | [pdo_mysql](https://www.php.net/manual/en/ref.pdo-mysql.php) | [pdo_pgsql](https://www.php.net/manual/en/ref.pdo-pgsql.php) | [pdo_sqlite](https://www.php.net/manual/en/ref.pdo-sqlite.php) | [pgsql](https://www.php.net/manual/en/book.pgsql.php) | [Phar](https://www.php.net/manual/en/book.phar.php) |
| [posix](https://www.php.net/manual/en/book.posix.php) | [readline](https://www.php.net/manual/en/book.readline.php) | [Reflection](https://www.php.net/manual/en/book.reflection.php) | [session](https://www.php.net/manual/en/book.session.php) | [shmop](https://www.php.net/manual/en/book.shmop.php) | [SimpleXML](https://www.php.net/manual/en/book.simplexml.php) |
| [sockets](https://www.php.net/manual/en/book.sockets.php) | [SPL](https://www.php.net/manual/en/book.spl.php) | [sqlite3](https://www.php.net/manual/en/book.sqlite3.php) | standard | sysvmsg | sysvsem |
| sysvshm | [tokenizer](https://www.php.net/manual/en/book.tokenizer.php) | [wddx*](https://www.php.net/manual/en/book.wddx.php) | [xml](https://www.php.net/manual/en/book.xml.php) | [xmlreader](https://www.php.net/manual/en/book.xmlreader.php) | [xmlrpc](https://www.php.net/manual/en/book.xmlrpc.php) |
| [xmlwriter](https://www.php.net/manual/en/book.xmlwriter.php) | [xsl](https://www.php.net/manual/en/book.xsl.php) | [yaml](https://www.php.net/manual/en/book.yaml.php) | [zip](https://www.php.net/manual/en/book.zip.php) | [zlib](https://www.php.net/manual/en/book.zlib.php) |  |

<small>*) wddx <a href="https://wiki.php.net/rfc/deprecate-and-remove-ext-wddx">dihapus</a> untuk PHP versi 7.4 keatas.</small>

Pemilihan versi PHP yang disediakan adalah up-to-date dengan versi PHP yang saat ini dalam [aktif pengembangan](https://www.php.net/supported-versions.php). Apabila ada ekstensi PHP yang anda butuhkan tidak tersedia, sebaiknya anda mencari library yang menyediakan alternatif (shim) dari komponen ekstensi yang tidak tersedia.

### PHP CLI

Melalui SSH, anda dapat memanggil script dengan `php` (versi 7.2). 

Untuk versi PHP CLI lain, anda dapat menggunakan `php73` dan `php74`.

Composer juga tersedia, anda dapat memanggilnya dengan `composer` untuk menginstall komponen.

Jangan mengaktifkan development server yang membuka port localhost. Namun atur agar server root menyesuaikan ke lokasi PHP entry point (`index.php`) yang ada dalam framework. 

### PHP Framework

DOM Cloud sudah dipastikan dapat bekerja untuk beberapa framework PHP yang terkenal, yakni Laravel dan CodeIgniter. Anda pula dapat memasang framework tersebut melalui template hosting.

Apabila anda ingin memasukkan aplikasi PHP kedalam server, dan anda memiliki kendala, mohon anda cek:

+ Apakah versi PHP yang aktif mendukung
+ Apakah ekstensi yang dibutuhkan semuanya ada
+ Apakah komponen composer sudah diinstall (`composer install`)
+ Apakah server root benar dan .htaccess sudah kompatibel
+ Apakah koneksi database sudah benar

### Pengaturan Default

Berikut dibawah adalah pengaturan master PHP untuk semua hosting. Jika anda ingin merubah beberapa konfigurasi (misalnya, maksimum ukuran upload atau waktu eksekusi script), gunakan file `.user.ini` pada server root (`$_SERVER['DOCUMENT_ROOT']`, biasanya dalam folder `public_html`). Anda bisa baca lebih lanjut [disini](https://www.php.net/manual/en/configuration.file.per-user.php).

```ini
[PHP]
;;;;;;;;;;;;;;;;;;;;
; Language Options ;
;;;;;;;;;;;;;;;;;;;;
engine = On
short_open_tag = Off
precision = 14
output_buffering = 4096
zlib.output_compression = Off
implicit_flush = Off
unserialize_callback_func =
serialize_precision = -1
disable_functions =
disable_classes =
zend.enable_gc = On
;;;;;;;;;;;;;;;;;
; Miscellaneous ;
;;;;;;;;;;;;;;;;;
expose_php = On
;;;;;;;;;;;;;;;;;;;
; Resource Limits ;
;;;;;;;;;;;;;;;;;;;
max_execution_time = 30
max_input_time = 60
memory_limit = 128M
;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;
; Error handling and logging ;
;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;
error_reporting = E_ALL & ~E_DEPRECATED & ~E_STRICT
display_errors = Off
display_startup_errors = Off
log_errors = On
log_errors_max_len = 1024
ignore_repeated_errors = Off
ignore_repeated_source = Off
report_memleaks = On
html_errors = On
;;;;;;;;;;;;;;;;;
; Data Handling ;
;;;;;;;;;;;;;;;;;
; Production Value: "GPCS";
variables_order = "GPCS"
request_order = "GP"
register_argc_argv = Off
auto_globals_jit = On
post_max_size = 8M
auto_prepend_file =
auto_append_file =
default_mimetype = "text/html"
default_charset = "UTF-8"
;;;;;;;;;;;;;;;;;;;;;;;;;
; Paths and Directories ;
;;;;;;;;;;;;;;;;;;;;;;;;;
doc_root =
user_dir =
enable_dl = Off
;;;;;;;;;;;;;;;;
; File Uploads ;
;;;;;;;;;;;;;;;;
file_uploads = On
upload_max_filesize = 2M
max_file_uploads = 20
;;;;;;;;;;;;;;;;;;
; Fopen wrappers ;
;;;;;;;;;;;;;;;;;;
allow_url_fopen = On
allow_url_include = Off
default_socket_timeout = 60
;;;;;;;;;;;;;;;;;;;
; Module Settings ;
;;;;;;;;;;;;;;;;;;;
[CLI Server]
cli_server.color = On
[Pcre]
pcre.jit=0
[Pdo_mysql]
pdo_mysql.cache_size = 2000
pdo_mysql.default_socket=
[mail function]
sendmail_path = /usr/sbin/sendmail -t -i
mail.add_x_header = On
[ODBC]
odbc.allow_persistent = On
odbc.check_persistent = On
odbc.max_persistent = -1
odbc.max_links = -1
odbc.defaultlrl = 4096
odbc.defaultbinmode = 1
[Interbase]
ibase.allow_persistent = 1
ibase.max_persistent = -1
ibase.max_links = -1
ibase.timestampformat = "%Y-%m-%d %H:%M:%S"
ibase.dateformat = "%Y-%m-%d"
ibase.timeformat = "%H:%M:%S"
[MySQLi]
mysqli.max_persistent = -1
mysqli.allow_persistent = On
mysqli.max_links = -1
mysqli.cache_size = 2000
mysqli.default_port = 3306
mysqli.default_socket =
mysqli.default_host =
mysqli.default_user =
mysqli.default_pw =
mysqli.reconnect = Off
[mysqlnd]
mysqlnd.collect_statistics = On
mysqlnd.collect_memory_statistics = Off
[PostgreSQL]
pgsql.allow_persistent = On
pgsql.auto_reset_persistent = Off
pgsql.max_persistent = -1
pgsql.max_links = -1
pgsql.ignore_notice = 0
pgsql.log_notice = 0
[bcmath]
bcmath.scale = 0
[Session]
session.save_handler = files
session.use_strict_mode = 0
session.use_cookies = 1
session.use_only_cookies = 1
session.name = PHPSESSID
session.auto_start = 0
session.cookie_lifetime = 0
session.cookie_path = /
session.cookie_domain =
session.cookie_httponly =
session.serialize_handler = php
session.gc_probability = 1
session.gc_divisor = 1000
session.gc_maxlifetime = 1440
session.referer_check =
session.cache_limiter = nocache
session.cache_expire = 180
session.use_trans_sid = 0
session.sid_length = 26
session.trans_sid_tags = "a=href,area=href,frame=src,form="
session.sid_bits_per_character = 5
[Assertion]
zend.assertions = -1
[Tidy]
tidy.clean_output = Off
[soap]
soap.wsdl_cache_enabled=1
soap.wsdl_cache_dir="/tmp"
soap.wsdl_cache_ttl=86400
soap.wsdl_cache_limit = 5
[ldap]
ldap.max_links = -1
```