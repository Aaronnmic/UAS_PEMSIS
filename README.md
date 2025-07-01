## Backend Simple LMS

Merupakan proyek backend untuk aplikasi LMS sederhana yang dibuat untuk tujuan studi kasus pembelajaran backend developement menggunakan Django dan Django Ninja.

ENDPOINT yang dikerjakan :
[Endpoint +1] Register: untuk memungkinkan calon user mendaftar secara langsung dengan mengisikan biodata dan data login.

[Endpoint +1] Batch Enroll Students: memungkinkan teacher untuk mendaftarkan beberapa siswa ke dalam kursus yang dimilikinya sekaligus.

[Endpoint +1] Content Comment Moderation: memungkinkan teacher untuk menentukan apakah suatu komentar pada content course-nya boleh ditampilkan atau tidak. Perubahan pada tampil komentar, di mana comment yang muncul hanya yang sudah dimoderasi.

[Endpoint +1] User Activity Dashboard: Menampilkan statistik aktivitas pengguna dalam kursus. Data yang harus ditampilkan adalah:

Jumlah course yang diikuti sebagai student

Jumlah course yang dibuat

Jumlah komentar yang pernah ditulis

Jumlah content yang diselesaikan (jika fitur content completion dibuat)

[Endpoint +1] Course Analytics: Menyediakan statistik course, meliputi:

Jumlah member pada course tersebut

Jumlah konten pada course tersebut

Jumlah komentar pada course tersebut

Jumlah feedback pada course tersebut (jika fitur feedback dibuat)

[Improve +1] Content Scheduling: Teacher dapat menjadwalkan konten untuk dirilis pada waktu tertentu saja. Di luar waktu tersebut, konten tidak boleh muncul pada 
saat di-list.

[Improve +1] Course Enrollment Limits: Menetapkan batasan jumlah pendaftar course:

Satu student hanya bisa enroll sekali pada course yang sama Teacher bisa menentukan jumlah maksimal student Jika kuota penuh, tidak ada lagi studen yang bisa masuk


[Fitur +4] Course Announcements merupakan fitur tambahan agar seorang teacher bisa memberikan pengumuman khusus pada course tertentu yang akan muncul pada tanggal  tertentu. Endpoint yang perlu ditambahakan untuk fitur ini adalah:

[Endpoint] Create announcement: untuk menambahkan pengumuman pada course tertentu (hanya teacher yang dapat membuat announcement)

[Endpoint] Show announcement: untuk menampilkan semua pengumuman pada course tertentu (teacher dan student dapat menampilkan announcement)

[Endpoint] Edit announcement: untuk mengedit announcement (hanya teacher yang dapat mengedit announcement)

[Endpoint] Delete announcement: endpoint untuk menghapus announcement (hanya teacher yang dapat menghapus announcement)

[Fitur +4] Course Categories Management: Memungkinkan teacher untuk menambah, mengedit, dan menghapus kategori dan menambahkan kategori tersebut pada course yang dibuat.

[Endpoint] Add Category: untuk membuat kategori baru

[Endpoint] Show category: untuk menampilkan semua kategori yang pernah dibuat (oleh semua user)

[Endpoint] Delete category: untuk menghapus kategori yang pernah dibuat oleh user tersebut.

[Improve] Add category column to course: pada saat membuat dan mengedit course, ada tambahan kolom course yang sifatnya boleh null.
Transcript

## Persyaratan

- **Docker** dan **Docker Compose**

## 📥 Clone Repository

```bash
    git clone https://github.com/Aaronnmic/UAS_PEMSIS.git
    cd be_simple_lms_main
```

## 📦 Instalasi 

### Build Aplikasi

Build dan jalankan aplikasi menggunakan `docker compose` :

```bash
    docker-compose up -d --build
```

### Migrasi Database

Masuk ke shell container aplikasi `be_simple_lms` dan migrasi database untuk membuat tabel:

```bash
    python manage.py makemigrations
    python manage.py migrate
```
