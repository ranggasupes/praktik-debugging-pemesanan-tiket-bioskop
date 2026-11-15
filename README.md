
# PRAKTIK DEBUGGING
## Sistem Pemesanan Tiket Bioskop

### Identitas Kelompok

**Kelompok 4**

| Nama | NIM |
|---|---|
| Khatamarrasyid | F5212510002 |
| Aditya Eka Kumara | F5212510019 |
| Rendra Akbar Fauzi | F5212510024 |
| Rangga Ferdi Kurniawan | F5212510032 |

---

## 1. Deskripsi Studi Kasus

Sistem Pemesanan Tiket Bioskop merupakan aplikasi web sederhana yang digunakan untuk menyimulasikan proses pemesanan tiket bioskop.

Aplikasi dibuat menggunakan HTML, CSS, dan JavaScript. Pengguna dapat memasukkan nama pemesan, memilih film, menentukan jumlah tiket, melihat daftar pemesanan, serta menghapus seluruh data pemesanan.

Proyek ini memiliki dua versi program, yaitu versi BUG dan versi FIX, untuk memperlihatkan perbedaan perilaku aplikasi sebelum dan sesudah proses debugging.

## 2. Daftar File

| Nama File | Keterangan |
|---|---|
| bug.html | Program sebelum diperbaiki |
| fix.html | Program setelah diperbaiki |
| README.md | Dokumentasi proyek |

## 3. Fitur Program

- Formulir nama pemesan.
- Pilihan film.
- Input jumlah tiket.
- Daftar pemesanan.
- Penghitung jumlah pemesanan.
- Tombol mengosongkan formulir.
- Tombol menghapus seluruh pemesanan.
- Pesan status pemesanan.

## 4. Perbedaan Versi BUG dan FIX

### Versi BUG

Pada versi BUG, sistem langsung menambahkan data pemesanan tanpa melakukan validasi input.

Akibatnya:
- Nama pemesan boleh kosong.
- Film boleh tidak dipilih.
- Jumlah tiket boleh kosong.
- Jumlah tiket 0 tetap diterima.
- Jumlah tiket desimal tetap diterima.
- Jumlah tiket lebih dari 10 tetap diterima.

### Versi FIX

Pada versi FIX, sistem sudah dilengkapi validasi input sebelum data disimpan.

Ketentuan validasi:
- Nama pemesan wajib diisi.
- Film wajib dipilih.
- Jumlah tiket wajib diisi.
- Jumlah tiket harus berupa bilangan bulat.
- Jumlah tiket harus berada pada rentang 1 sampai 10.

Jika input tidak sesuai, sistem menampilkan pesan kesalahan dan data tidak ditambahkan ke daftar pemesanan.

## 5. Skenario Pengujian

| No. | Skenario | Hasil pada FIX |
|---|---|---|
| 1 | Semua input kosong | Ditolak |
| 2 | Nama pemesan kosong | Ditolak |
| 3 | Film belum dipilih | Ditolak |
| 4 | Jumlah tiket kosong | Ditolak |
| 5 | Jumlah tiket 0 | Ditolak |
| 6 | Jumlah tiket desimal | Ditolak |
| 7 | Jumlah tiket lebih dari 10 | Ditolak |
| 8 | Semua input valid | Diterima |

Pada versi BUG, data tetap ditambahkan meskipun input belum lengkap atau tidak sesuai.

## 6. Teknologi yang Digunakan

- HTML: digunakan untuk membuat struktur halaman.
- CSS: digunakan untuk mengatur tampilan dan tata letak aplikasi.
- JavaScript: digunakan untuk menjalankan proses pemesanan, mengelola daftar pemesanan, dan melakukan validasi input pada versi FIX.

## 7. Cara Menjalankan Program

1. Siapkan folder proyek.
2. Simpan kode program pertama dengan nama `bug.html`.
3. Simpan kode program kedua dengan nama `fix.html`.
4. Simpan dokumentasi ini dengan nama `README.md`.
5. Buka file `bug.html` menggunakan browser untuk menjalankan versi BUG.
6. Buka file `fix.html` menggunakan browser untuk menjalankan versi FIX.

Program dapat dijalankan langsung melalui browser tanpa instalasi library tambahan atau server.

## 8. Kesimpulan

Melalui studi kasus ini, proses debugging dilakukan dengan membandingkan program sebelum dan sesudah perbaikan.

Versi BUG menunjukkan bahwa tidak adanya validasi dapat menyebabkan data yang tidak sesuai tetap diterima oleh sistem. Sementara itu, versi FIX memperbaiki permasalahan tersebut dengan menambahkan pemeriksaan kelengkapan data dan validasi jumlah tiket.

Dengan demikian, proses debugging membantu meningkatkan ketepatan dan keandalan proses input pada aplikasi web sederhana.

## 9. Catatan

Data pemesanan disimpan sementara menggunakan array JavaScript selama halaman masih berjalan. Aplikasi belum menggunakan database sehingga data akan hilang ketika halaman dimuat ulang.
