# ProfilApp

Aplikasi Android sederhana untuk menampilkan halaman profil mahasiswa. Project ini dibuat menggunakan **Jetpack Compose** untuk memenuhi Tugas Praktikum Bab 2 Pemrograman Aplikasi Perangkat Bergerak (PAPB).

---

## Penjelasan Kode

### `MainActivity.kt`
File ini merupakan tampilan utama aplikasi yang dibangun secara deklaratif menggunakan Jetpack Compose:

* **Box & Card:** Digunakan sebagai wadah utama untuk memberikan latar belakang serta kartu profil berbayang (*elevation*) yang rapi di tengah layar.
* **Column:** Menyusun komponen UI secara vertikal dan diatur agar rata tengah (`Alignment.CenterHorizontally`).
* **Image:** Menampilkan foto profil (`profile.png`) dari folder `res/drawable` yang dipotong berbentuk lingkaran (`CircleShape`).
* **Text:** Menampilkan data diri mahasiswa, meliputi **Nama Lengkap** (Roniarta Sibarani), **NIM** (245150200111036), dan Program Studi / Fakultas (Teknik Informatika FILKOM UB).
* **Spacer:** Memberikan jarak vertikal yang konsisten antar elemen UI.
* **Button & State (`mutableStateOf`):** Komponen tombol interaktif yang nilainya tersimpan dalam state `isFollowed`. Tombol dapat berganti teks dan warna secara dinamis antara **Follow** dan **Unfollow** saat diklik melalui proses *recomposition*.

---

## Tangkapan Layar (Screenshot)

## Tangkapan Layar (Screenshot)

| Portrait | Landscape |
| :---: | :---: |
| ![screenshot_portrait](https://github.com/user-attachments/assets/090c85e8-b636-42d8-9bdb-86c2195d2079) | ![screenshot_landscape](https://github.com/user-attachments/assets/ad485b04-1f31-4b80-8605-cb5db262d0a2) |
---

## Keuntungan Compose Dibandingkan XML Layout

* **Pendekatan Deklaratif:** Jetpack Compose memungkinkan pengembang untuk mendeskripsikan tampilan UI secara langsung dalam satu file Kotlin (`@Composable`). Berbeda dengan XML tradisional yang memisahkan antara struktur tampilan (file `.xml`) dan logika interaksi (file `.kt`).
* **Produktivitas Tinggi:** Pengembangan aplikasi menjadi jauh lebih cepat dan praktis karena tidak perlu berpindah-pindah file antara XML dan Kotlin. Penanganan event seperti `onClick` serta pengelolaan *State* dapat langsung ditulis di dalam komponen yang bersangkutan.
* **Pemeliharaan Kode Lebih Mudah (*Maintainability*):** Kode UI jauh lebih modular, ringkas (*less boilerplate code*), dan mudah dibaca secara sekuensial. Struktur hirarki UI seperti `Column` dengan jelas menggambarkan urutan elemen dari `Image`, `Text`, hingga `Button`.
* **Reusability & Modern Tools:** Fungsi `@Composable` memudahkan penggunaan kembali komponen UI di berbagai tempat, serta didukung fitur `@Preview` untuk melihat tampilan UI secara *real-time* tanpa harus selalu menjalankan emulator atau perangkat fisik.
