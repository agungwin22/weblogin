# WebLogin Flask

## Deskripsi Proyek

WebLogin Flask adalah proyek aplikasi web sederhana yang dibangun menggunakan **Python Flask** untuk mempelajari dan mengimplementasikan sistem **login (autentikasi pengguna)**. Proyek ini dirancang khusus untuk developer level **beginner–intermediate** yang ingin memahami alur kerja autentikasi di Flask secara rapi, terstruktur, dan mudah dikembangkan.

Fokus utama proyek ini bukan pada tampilan visual yang kompleks, melainkan pada **struktur proyek, alur autentikasi, penggunaan Flask-WTF, serta pemisahan logika backend dan frontend**.

---

## Tujuan Proyek

Proyek ini dibuat dengan tujuan:

* Memahami cara kerja routing di Flask
* Menerapkan sistem login menggunakan Flask-WTF
* Mengenal konsep template inheritance dengan Jinja2
* Membangun struktur folder Flask yang rapi dan scalable
* Menjadi fondasi untuk pengembangan fitur lanjutan (register, database, session, dll)

Jika kamu sedang belajar Flask dan ingin **belajar melalui proyek nyata**, repository ini cocok dijadikan referensi.

---

## Fitur Utama

* Halaman Login
* Validasi form menggunakan Flask-WTF
* Flash message (success & error)
* Template inheritance (base.html)
* Struktur proyek terorganisir
* Styling CSS sederhana

---

## Teknologi yang Digunakan

* Python 3
* Flask
* Flask-WTF
* Jinja2 Template Engine
* HTML5 & CSS3

---

## Struktur Folder

```
weblogin/
│
├── app/
│   ├── __init__.py        # Inisialisasi aplikasi Flask
│   ├── routes.py          # Routing / endpoint aplikasi
│   ├── forms.py           # Form Flask-WTF
│   ├── templates/
│   │   ├── base.html      # Template utama
│   │   ├── login.html     # Halaman login
│   │   └── home.html      # Halaman home
│   └── static/
│       └── css/
│           └── style.css  # Styling CSS
│
├── run.py                 # Entry point aplikasi
├── requirements.txt       # Daftar dependency
└── README.md              # Dokumentasi proyek
```

Struktur ini mengikuti praktik umum pada proyek Flask sehingga mudah dikembangkan ke skala yang lebih besar.

---

## Cara Menjalankan Proyek

### 1. Clone Repository

```bash
git clone https://github.com/username/weblogin.git
cd weblogin
```

### 2. Buat Virtual Environment (Opsional tapi Disarankan)

```bash
python -m venv venv
source venv/bin/activate  # Linux / Mac
venv\Scripts\activate     # Windows
```

### 3. Install Dependency

```bash
pip install -r requirements.txt
```

### 4. Jalankan Aplikasi

```bash
python run.py
```

Akses aplikasi melalui browser:

```
http://127.0.0.1:5000
```

---

## Alur Login Sederhana

1. User mengisi email dan password pada halaman login
2. Data divalidasi menggunakan Flask-WTF
3. Jika data sesuai (hardcode / simulasi), user dianggap berhasil login
4. Flash message ditampilkan sesuai hasil login

Catatan: Pada versi ini **belum menggunakan database**, sehingga cocok sebagai tahap awal pembelajaran.

---

## Pengembangan Selanjutnya (Opsional)

Beberapa fitur yang bisa kamu tambahkan:

* Register user
* Login menggunakan database (SQLite / MySQL)
* Password hashing (Werkzeug)
* Session & logout
* Proteksi halaman (login required)
* Role-based access

Proyek ini sengaja dibuat sederhana agar mudah dikembangkan sesuai kebutuhan.

---

## Catatan Penting

Jika kamu merasa proyek ini terlalu sederhana, itu **bukan kelemahan**, melainkan desain yang disengaja. Banyak developer pemula gagal memahami framework karena langsung membuat sistem yang terlalu kompleks.

Menguasai dasar dengan benar jauh lebih bernilai dibanding sekadar banyak fitur tapi tidak paham alurnya.

---

## Lisensi

Proyek ini bersifat **open-source** dan bebas digunakan untuk belajar maupun dikembangkan lebih lanjut.

---

Jika README ini kamu gunakan untuk portfolio, pastikan repository kamu bersih, rapi, dan mudah dipahami oleh recruiter atau developer lain.
