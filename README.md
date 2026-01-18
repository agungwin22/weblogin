# WebLogin Flask (Login & Register)

## Deskripsi Proyek

WebLogin Flask adalah proyek aplikasi web berbasis **Python Flask** yang mengimplementasikan sistem **autentikasi pengguna lengkap**, mencakup fitur **registrasi (register)** dan **login**. Proyek ini dikembangkan sebagai lanjutan dari versi sebelumnya yang hanya memiliki login, dengan penambahan alur pendaftaran akun serta penyesuaian struktur folder agar lebih rapi dan mendekati standar aplikasi Flask yang scalable.

Proyek ini ditujukan untuk developer level **beginner–intermediate** yang ingin benar-benar memahami bagaimana sistem autentikasi bekerja di Flask, mulai dari validasi form, routing, template, hingga alur data user.

---

## Tujuan Proyek

Proyek ini dibuat untuk:

* Memahami alur autentikasi user (register & login) di Flask
* Menggunakan Flask-WTF untuk validasi form
* Menerapkan template inheritance menggunakan Jinja2
* Membiasakan diri dengan struktur folder Flask yang lebih terorganisir
* Menjadi fondasi sebelum menggunakan database dan sistem autentikasi yang lebih kompleks

Proyek ini sengaja dibuat **sederhana namun benar secara konsep**, agar mudah dikembangkan ke tahap berikutnya.

---

## Fitur Utama

* Registrasi akun (Register)
* Login pengguna
* Validasi form dengan Flask-WTF
* Flash message (success & error)
* Template inheritance (`base.html`)
* Styling CSS sederhana
* Struktur folder yang diperbarui dan lebih rapi

---

## Teknologi yang Digunakan

* Python 3
* Flask
* Flask-WTF
* Jinja2 Template Engine
* HTML5 & CSS3

---

## Struktur Folder

Struktur folder telah diperbarui untuk menyesuaikan penambahan fitur register dan pemisahan logika aplikasi:

```
weblogin/
│
├── app/
│   ├── __init__.py        # Inisialisasi aplikasi Flask
│   ├── routes.py          # Routing login & register
│   ├── forms.py           # Form Login & Register (Flask-WTF)
│   ├── templates/
│   │   ├── base.html      # Template utama
│   │   ├── login.html     # Halaman login
│   │   ├── register.html  # Halaman register
│   │   └── home.html      # Halaman home
│   └── static/
│       └── css/
│           └── style.css  # Styling CSS
│
├── run.py                 # Entry point aplikasi
├── requirements.txt       # Dependency proyek
└── README.md              # Dokumentasi
```

Struktur ini memudahkan penambahan fitur lanjutan seperti database, session, dan proteksi halaman.

---

## Cara Menjalankan Proyek

### 1. Clone Repository

```bash
git clone https://github.com/username/weblogin.git
cd weblogin
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

### 4. Jalankan Aplikasi

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
2. Data divalidasi menggunakan Flask-WTF
3. Jika valid, akun berhasil didaftarkan (simulasi / belum database)
4. Flash message ditampilkan

### Login

1. User memasukkan email dan password
2. Data diverifikasi sesuai data yang tersedia
3. Jika sesuai, login berhasil dan user diarahkan ke halaman utama

Catatan: Versi ini **belum menggunakan database**, sehingga data user masih bersifat simulasi untuk keperluan pembelajaran.

---

## Pengembangan Selanjutnya

Beberapa pengembangan yang sangat disarankan:

* Integrasi database (SQLite / MySQL)
* Password hashing (Werkzeug)
* Session & logout
* Proteksi halaman dengan `login_required`
* Role user (admin / user)

---

## Catatan untuk Pembelajar

Jika proyek ini terlihat sederhana, itu disengaja. Banyak developer pemula gagal memahami Flask karena langsung melompat ke sistem yang kompleks tanpa memahami alur autentikasi dasar.

Proyek ini dirancang sebagai **pondasi yang kuat**, bukan sekadar demo.

---

## Lisensi

Proyek ini bersifat open-source dan bebas digunakan untuk belajar maupun dikembangkan lebih lanjut.
