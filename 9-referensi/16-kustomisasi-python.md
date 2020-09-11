---
title: Kustomisasi Python
parent: Referensi
nav_order: 16
layout: default
permalink: kustomisasi-python.html
---

### Versi Python yang didukung

DOM Cloud mendukung Python versi 3.6 (default) dan 3.8 dengan daftar module global (pip) sebagai berikut:

|  |  |  |  |
|-|-|-|-|
| [Django](https://pypi.org/project/Django/) | [Flask](https://pypi.org/project/Flask/) | [requests](https://pypi.org/project/requests/) | [PyYAML](https://pypi.org/project/PyYAML/) |
| [mysql-connector-python](https://pypi.org/project/mysql-connector-python/) | [py-postgresql](https://pypi.org/project/py-postgresql/) | [sqlparse](https://pypi.org/project/sqlparse/) | [redis](https://pypi.org/project/redis/) |
| [python-dateutil](https://pypi.org/project/python-dateutil/) | [urllib3](https://pypi.org/project/urllib3/) | [threadpoolctl](https://pypi.org/project/threadpoolctl/) | [protobuf](https://pypi.org/project/protobuf/) |
| [scikit-learn](https://pypi.org/project/scikit-learn/) | [scipy](https://pypi.org/project/scipy/) | [numpy](https://pypi.org/project/numpy/) | [joblib](https://pypi.org/project/joblib/) |

<small>Masih banyak lagi daftar module global yang anda bisa cek sendiri lewat <code>pip list</code></small>

### Akses CLI

Menggunakan ssh, anda dapat menggunakan `python3` atau `python3.8` untuk mengakses python.

Untuk pip, anda dapat menggunakan `pip3` atau `pip3.8`. Ingat bahwa anda tidak bisa menginstall module secara global, jadi anda harus menginstall pada context user dengan cara menambahkan `--user` setiap operasi *pip install*.

### Passenger Entry Point

Agar bisa mengaktifkan entry point melalui file `passenger_wsgi.py` diatas server root (yang jika anda set ke `public_html/public`, maka `passenger_wsgi.py` harus ada di folder `public_html`) berisikan modul dalam variabel `application`, seperti berikut:

```py
from main import MyApp as application
```

Jika anda isikan `main.py` di folder yang sama seperti berikut

```py
def MyApp():
    return "Hello world"
```

Maka akan muncul pesan "Hello world" di hasil server. Inilah setup yang paling gampang dilakukan dengan python. Anda dapat membaca python entry point di [dokumentasi passenger ini](https://www.phusionpassenger.com/library/indepth/python/app_autodetection/apache/).

### Python Framework

DOM Cloud dapat menggunakan framework Python, yakni Flask dan Django. Framework tersebut sudah diinstall sehingga anda tak perlu harus menginstallnya sendiri.

