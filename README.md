# WebLogin Flask (Login, Register, Database & Session)

## Deskripsi Proyek

WebLogin Flask adalah aplikasi web berbasis **Python Flask** yang mengimplementasikan sistem autentikasi pengguna **end-to-end**, meliputi **registrasi akun, login, penyimpanan data ke database, password hashing, serta manajemen session**. Proyek ini merupakan versi lanjutan dari implementasi sebelumnya dan dirancang untuk mendekati praktik nyata aplikasi web modern.

Proyek ini cocok untuk developer level **intermediate** yang ingin naik kelas dari sekadar form login menjadi sistem autentikasi yang aman, terstruktur, dan siap dikembangkan lebih lanjut.

---

## Tujuan Proyek

Tujuan utama proyek ini adalah:

* Memahami autentikasi user secara lengkap di Flask
* Menggunakan database sebagai penyimpanan data user
* Mengamankan password dengan hashing
* Mengelola session login dan logout
* Menerapkan struktur folder Flask yang lebih scalable
* Menyiapkan fondasi sebelum menggunakan Flask-Login atau JWT

Proyek ini tidak dibuat sebagai "demo cepat", tetapi sebagai **pondasi teknis yang benar**.

---

## Fitur Utama

* Register akun (simpan ke database)
* Login user dengan validasi database
* Password hashing (keamanan dasar)
* Session login & logout
* Flash message (success & error)
* Proteksi halaman berbasis session
* Template inheritance (Jinja2)
* Struktur folder diperbarui dan lebih modular

---

## Teknologi yang Digunakan

* Python 3
* Flask
* Flask-WTF
* Flask SQLAlchemy / SQLite (database)
* Werkzeug Security (password hashing)
* Jinja2 Template Engine
* HTML5 & CSS3

---

## Struktur Folder

Struktur folder telah disesuaikan dengan penggunaan database dan session:

```
login/
│
├── app/
│   ├── __init__.py          # Inisialisasi Flask, DB, secret key
│   ├── routes.py            # Routing login, register, logout
│   ├── models.py            # Model database (User)
│   ├── forms.py             # Form Login & Register (Flask-WTF)
│   ├── templates/
│   │   ├── base.html        # Template utama
│   │   ├── login.html       # Halaman login
│   │   ├── register.html    # Halaman register
│   │   └── dashboard.html   # Halaman setelah login
│   └── static/
│       └── css/
│           └── style.css    # Styling CSS
│
├── instance/
│   └── app.db               # Database SQLite
│
├── run.py                   # Entry point aplikasi
├── requirements.txt         # Dependency proyek
└── README.md                # Dokumentasi
```

Struktur ini memisahkan **logic, data, dan presentation** sehingga mudah dirawat dan dikembangkan.

---

## Cara Menjalankan Proyek

### 1. Clone Repository

```bash
git clone https://github.com/username/login.git
cd login
```

### 2. Buat Virtual Environment (Disarankan)

```bash
python -m venv venv
source venv/bin/activate  # Linux / Mac
venv\Scripts\activate     # Windows
```

### 3. Install Dependency

```bash
pip install -r requirements.txt
```

### 4. Inisialisasi Database

```bash
python
>>> from app import db
>>> db.create_all()
>>> exit()
```

### 5. Jalankan Aplikasi

```bash
python run.py
```

Akses melalui browser:

```
http://127.0.0.1:5000
```

---

## Alur Autentikasi

### Register

1. User mengisi form register
2. Password di-hash menggunakan Werkzeug
3. Data user disimpan ke database
4. Flash message ditampilkan

### Login

1. User memasukkan email dan password
2. Password diverifikasi dengan hash di database
3. Jika valid, session login dibuat
4. User diarahkan ke dashboard

### Logout

1. Session dihapus
2. User dikembalikan ke halaman login

---

## Keamanan Dasar yang Diterapkan

* Password tidak disimpan dalam bentuk plain text
* Session berbasis secret key
* Validasi input menggunakan Flask-WTF

Catatan: Ini adalah **keamanan level dasar–menengah**, belum termasuk CSRF advanced, rate limiting, atau OAuth.

---

## Pengembangan Selanjutnya

Beberapa peningkatan yang disarankan:

* Flask-Login (user management lebih rapi)
* Role & permission user
* Email verification
* Reset password
* Deployment (Gunicorn + Nginx)

---

## Catatan untuk Developer

Jika kamu memahami proyek ini dengan baik, kamu sudah **melewati tahap beginner Flask**. Banyak developer berhenti di form login tanpa memahami database, hashing, dan session.

Proyek ini menempatkanmu **di jalur yang benar**.

---

## Lisensi

Proyek ini bersifat open-source dan bebas digunakan untuk pembelajaran maupun pengembangan lanjutan.
