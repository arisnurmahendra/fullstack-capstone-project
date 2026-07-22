# User Stories - GiftLink

## User Story 1
**Title:** Registrasi Akun
**As a** pengguna baru,
**I want** untuk membuat akun,
**so that** saya dapat mengakses fitur GiftLink seperti memberikan dan mencari barang.

**Acceptance Criteria:**
1. Pengguna dapat mengisi form registrasi dengan nama, email, dan password.
2. Sistem memvalidasi bahwa email belum terdaftar sebelumnya.
3. Setelah registrasi berhasil, pengguna diarahkan ke halaman utama dan menerima token autentikasi.

**Priority:** High
**Story Points:** 2
**Labels:** new

---

## User Story 2
**Title:** Login ke Akun
**As a** pengguna terdaftar,
**I want** untuk masuk ke akun saya,
**so that** saya dapat mengelola profil dan barang yang saya tawarkan.

**Acceptance Criteria:**
1. Pengguna dapat login menggunakan email dan password yang valid.
2. Sistem menampilkan pesan error jika kredensial salah.
3. Setelah login berhasil, token JWT disimpan untuk sesi pengguna.

**Priority:** High
**Story Points:** 2
**Labels:** new

---

## User Story 3
**Title:** Melihat Daftar Barang
**As a** pengguna,
**I want** untuk melihat daftar barang yang tersedia,
**so that** saya dapat menemukan barang yang saya butuhkan secara gratis.

**Acceptance Criteria:**
1. Halaman utama menampilkan daftar seluruh barang dari database.
2. Setiap barang menampilkan gambar, nama, dan kategori singkat.
3. Data diambil melalui endpoint `/api/gifts`.

**Priority:** High
**Story Points:** 3
**Labels:** new

---

## User Story 4
**Title:** Mencari Barang berdasarkan Kategori
**As a** pengguna,
**I want** untuk mencari barang berdasarkan kategori atau kata kunci,
**so that** saya bisa lebih cepat menemukan barang yang relevan.

**Acceptance Criteria:**
1. Terdapat kolom pencarian di halaman utama.
2. Hasil pencarian difilter berdasarkan kategori yang dipilih.
3. Data diambil melalui endpoint `/api/search`.

**Priority:** Medium
**Story Points:** 3
**Labels:** backlog

---

## User Story 5
**Title:** Melihat Detail Barang
**As a** pengguna,
**I want** untuk melihat detail sebuah barang,
**so that** saya dapat mengetahui kondisi, deskripsi, dan lokasi barang tersebut sebelum mengambilnya.

**Acceptance Criteria:**
1. Pengguna dapat mengklik sebuah barang untuk melihat detail lengkapnya.
2. Halaman detail menampilkan gambar, deskripsi, kondisi, dan nama pemberi.
3. Data diambil melalui endpoint `/api/gifts/:id`.

**Priority:** Medium
**Story Points:** 2
**Labels:** new

---

## User Story 6
**Title:** Memberikan Komentar pada Barang
**As a** pengguna,
**I want** untuk memberikan komentar pada sebuah barang,
**so that** saya dapat bertanya atau memberi informasi tambahan kepada pemberi barang.

**Acceptance Criteria:**
1. Pengguna yang sudah login dapat menambahkan komentar di halaman detail barang.
2. Komentar tersimpan dan ditampilkan secara real-time di halaman tersebut.
3. Hanya pengguna terautentikasi yang dapat mengirim komentar.

**Priority:** Low
**Story Points:** 3
**Labels:** icebox

---

## User Story 7
**Title:** Mengedit Profil Pengguna
**As a** pengguna terdaftar,
**I want** untuk mengedit informasi profil saya,
**so that** data saya selalu akurat dan terbaru.

**Acceptance Criteria:**
1. Pengguna dapat mengubah nama, email, dan informasi lain di halaman profil.
2. Perubahan disimpan melalui endpoint update pada `authRoutes.js`.
3. Sistem menampilkan konfirmasi setelah perubahan berhasil disimpan.

**Priority:** Medium
**Story Points:** 2
**Labels:** technical debt

---

## User Story 8
**Title:** Logout dari Akun
**As a** pengguna yang sedang login,
**I want** untuk keluar dari akun saya,
**so that** akun saya tetap aman ketika perangkat digunakan orang lain.

**Acceptance Criteria:**
1. Terdapat tombol logout yang dapat diakses dari halaman manapun setelah login.
2. Token autentikasi dihapus dari sesi/local storage setelah logout.
3. Pengguna diarahkan kembali ke halaman login.

**Priority:** Low
**Story Points:** 1
**Labels:** backlog
