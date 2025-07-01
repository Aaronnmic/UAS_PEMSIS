## Backend Simple LMS

Merupakan proyek backend untuk aplikasi LMS sederhana yang dibuat untuk tujuan studi kasus pembelajaran backend developement menggunakan Django dan Django Ninja.

ENDPOINT yang dikerjakan :

 [Endpoint +1] Register
✅ Fungsi register(request) ada dan menangani pembuatan user baru via metode POST.

Menggunakan JSON, validasi field, dan pengecekan duplikat username.

🔹 [Endpoint +1] Batch Enroll Students
✅ Fungsi batch_enroll(request) menggunakan form dan menambahkan siswa ke course sekaligus, dengan batas maksimal siswa.

🔹 [Endpoint +1] Content Comment Moderation
✅ Fungsi moderate_comment(request, content_id, comment_id) tersedia, hanya teacher yang dapat menyetujui komentar.

✅ Fungsi list_comments hanya menampilkan komentar yang disetujui.

🔹 [Endpoint +1] User Activity Dashboard
✅ Fungsi user_activity_dashboard(request, user_id) menampilkan statistik aktivitas pengguna menggunakan method get_course_stats.

🔹 [Endpoint +1] Course Analytics
✅ Fungsi course_analytics(request, course_id) menampilkan statistik course menggunakan method get_course_stats.

🔹 [Improve +1] Content Scheduling
✅ Fungsi list_course_contents memfilter konten berdasarkan waktu mulai dan akhir (scheduled_start_time), dan memanggil method is_available().

🔹 [Improve +1] Course Enrollment Limits
✅ Fungsi enroll_student(request) memeriksa apakah siswa sudah terdaftar dan apakah kuota penuh.

🔹 [Fitur +4] Course Announcements
✅ Fungsi create_announcement, show_announcements, edit_announcement, dan delete_announcement lengkap.

Validasi role teacher dan periode aktif pengumuman.

🔹 [Fitur +4] Course Categories Management
✅ Fungsi create_category, show_category, dan delete_category lengkap.

Validasi request.user dan kepemilikan.

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
