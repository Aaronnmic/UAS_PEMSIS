# 📚 Backend Simple LMS

Proyek backend untuk aplikasi Learning Management System (LMS) sederhana. Dibuat sebagai studi kasus pembelajaran backend development menggunakan **Django** dan **Django Ninja**.

---

## 🚀 Fitur & Endpoint yang Telah Dikerjakan

### 🔐 \[Endpoint +1] User Registration

✅ `register(request)`
Menangani pendaftaran user baru via metode `POST` dengan:

* Input berupa JSON
* Validasi field
* Pengecekan duplikat username

---

### 👥 \[Endpoint +1] Batch Enroll Students

✅ `batch_enroll(request)`
Menambahkan beberapa siswa ke dalam course sekaligus, dengan form dan pembatasan jumlah maksimal siswa.

---

### 💬 \[Endpoint +1] Content Comment Moderation

✅ `moderate_comment(request, content_id, comment_id)`

* Hanya *teacher* yang dapat menyetujui komentar.
  ✅ `list_comments()`
* Hanya menampilkan komentar yang sudah disetujui.

---

### 📊 \[Endpoint +1] User Activity Dashboard

✅ `user_activity_dashboard(request, user_id)`
Menampilkan statistik aktivitas pengguna menggunakan `get_course_stats()`.

---

### 📈 \[Endpoint +1] Course Analytics

✅ `course_analytics(request, course_id)`
Menampilkan analitik course tertentu dengan `get_course_stats()`.

---

### 🗓️ \[Improve +1] Content Scheduling

✅ `list_course_contents()`
Memfilter konten berdasarkan waktu mulai dan akhir (`scheduled_start_time`) serta memanggil method `is_available()`.

---

### 🚫 \[Improve +1] Course Enrollment Limits

✅ `enroll_student(request)`
Memastikan:

* Siswa belum terdaftar di course
* Kuota course belum penuh

---

### 📢 \[Fitur +4] Course Announcements

✅ `create_announcement`, `show_announcements`, `edit_announcement`, `delete_announcement`
Fitur lengkap dengan:

* Validasi peran *teacher*
* Validasi periode aktif pengumuman

---

### 🗂️ \[Fitur +4] Course Categories Management

✅ `create_category`, `show_category`, `delete_category`
Dengan validasi:

* Kepemilikan course
* Autentikasi user yang membuat kategori

---

## 🛠️ Persyaratan

* [Docker](https://www.docker.com/)
* [Docker Compose](https://docs.docker.com/compose/)

---

## 📥 Cara Clone Repository

```bash
git clone https://github.com/Aaronnmic/UAS_PEMSIS.git
cd UAS_PEMSIS-main
```

---

## ⚙️ Instalasi & Menjalankan Aplikasi

### 🔧 Build Aplikasi

Jalankan aplikasi menggunakan Docker Compose:

```bash
docker-compose up -d --build
```

---

### 🗄️ Migrasi Database

Masuk ke shell container dan jalankan migrasi untuk membuat tabel:

```bash
python manage.py makemigrations
python manage.py migrate
```

---
