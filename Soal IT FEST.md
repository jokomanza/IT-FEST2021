# SOAL IT FEST 2021 - Divisi Aplikasi

|Catatan khusus:|
|--|
|<ol><li>Gunakan format berikut untuk nama proyek Anda: IT-FEST2021_[KELAS]_[NAMA], contoh: IT-FEST2021_XIISIJAB_MARTIN.</li> <li>Anda harus menyerahkan seluruh proyek dan memastikan bahwa proyek dapat dijalankan di komputer lain (PC) tanpa konfigurasi tambahan. Harap perhatikan string koneksi database Anda! </li> <li> Jika Anda gagal mengirimkan proyek yang tepat yang menyebabkan proyek tidak dapat dikompilasi, tidak ada skor akan diberikan. </li> <li> Anda tidak diperbolehkan untuk memodifikasi atau mengubah struktur database yang diberikan. Namun, Anda dapat memasukkan catatan tambahan. </li> <li> Proses penandaan akan dilakukan menggunakan database asli yang diberikan dengan catatan tambahan. </li> </ol>|

<h1 align="center">STEMSEND Books</h1>

STEMSEND Books adalah aplikasi baru yang bertujuan untuk membantu mengelola sistem penyimpanan buku di SMK Negeri 2 Klaten. Sebagai developer yang baru diangkat, Anda ditugaskan untuk membuat Aplikasi Desktop. Diberikan di sepanjang proyek adalah ERD, sample data, dan detail dari setiap fitur yang diminta.

## A. Database
Nama Database : STEMSEND_BooksDB
### ERD
![ERD](./Database/Database%20STEMSEND%20Books.png)

### Detail
| Table | Key | Column          | Data Type   | Nullable | Default Value | Notes                                              |
|-------|-----|-----------------|-------------|----------|---------------|----------------------------------------------------|
| Users | PK  | Id              | INT         | No       | -             | Auto Increment                                     |
|       |     | Username        | VARCHAR(50) | No       | -             |                                                    |
|       |     | Password        | VARCHAR(50) | No       | -             |                                                    |
|       |     | Email           | VARCHAR(50) | No       | -             | Unique Value                                       |
|       |     | Nama            | VARCHAR(50) | No       | -             |                                                    |
| Books | PK  | Id              | INT         | No       | -             |                                                    |
|       | FK  | User_Id         | INT         | No       | -             |                                                    |
|       |     | Judul           | VARCHAR(50) | No       | -             | Unique Value                                       |
|       |     | Pengarang       | VARCHAR(50) | No       | -             |                                                    |
|       |     | Penerbit        | VARCHAR(50) | No       | -             |                                                    |
|       |     | Jumlah          | INT         | No       | 1             |                                                    |
|       |     | Tanggal_Dirubah | DATE TIME   | No       | -             | Waktu data dibuat atau waktu terakhir data diubah. |

## B. Login
- [x] Form login digunakan oleh staf untuk mengakses menu di dalam sistem. 
- [x] Memvalidasi bahwa informasi login ada di database. 
- [x] Tampilkan pesan kesalahan yang tepat jika perlu.
- [x] Jika login sukses, langsung diarahkan ke Home.
<img src="./STEMSEND%20Books%20Wireframe/Login%20Form.png" alt="Login" width="45%" height="45%"/>

## C. Home
- [x] Semua data Buku harus tampil.
- [x] Jika tombol Tambah Buku ditekan, akan memunculkan Form Tambah Buku.
- [x] Jika tombol Edit Buku ditekan, akan memunculkan Form Edit Buku.
- [x] Jika tombol Hapus Buku ditekan, akan memunculkan Form Hapus Buku.
- [x] Jika tombol Logout ditekan, maka user akan keluar dari aplikasi dan kembali ke Form Login.
- [x] Tampilkan pesan kesalahan yang tepat jika perlu.
<img src="./STEMSEND%20Books%20Wireframe/Home%20Form.png" alt="Home" width="50%" height="50%"/>

## D. Tambah Buku
- [x] Form Tambah Buku digunakan untuk menambahkan data buku baru.
- [x] Pada saat tombol Simpan ditekan, simpan data yang telah dimasukan user.
- [x] Pada saat akan menyimpan data, gunakan validasi data yang tepat.
- [x] Jika tombol Batal ditekan, tutup Form Tambah Buku dan kembali ke Form Home.
- [x] Setelah data berhasil disimpan, tutup Form Tambah Buku dan kembali ke Form Home serta refresh data grid yang ada di Form Home.
- [x] Tampilkan pesan kesalahan yang tepat jika perlu.
<img src="./STEMSEND%20Books%20Wireframe/Tambah%20Buku%20Form.png" alt="Tambah Buku" width="45%" height="45%"/>

## E. Edit Buku
- [x] Form Edit Buku digunakan untuk mengedit data buku yang sudah ada.
- [x] Pada saat pertama kali form muncul, semua Id buku ada di Combo Box Id buku.
- [x] Pada saat pertama kali form muncul, semua field selain Id buku secara otomatis terisi dengan data buku sesuai id buku yang terpilih pertama kali.
- [x] Pada saat id buku yang dipilih berubah, field lain juga ikut terisi secara otomatis dengan data buku sesuai id buku yang dipilih.
- [x] Pada saat tombol Simpan ditekan, update data yang telah dimasukan user.
- [x] Pada saat akan menyimpan data, gunakan validasi data yang tepat.
- [x] Jika tombol Batal ditekan, tutup Form Edit Buku dan kembali ke Form Home.
- [x] Setelah data berhasil disimpan, tutup Form Edit Buku dan kembali ke Form Home serta refresh data grid yang ada di Form Home.
- [x] Tampilkan pesan kesalahan yang tepat jika perlu.
<img src="./STEMSEND%20Books%20Wireframe/Edit%20Buku%20Form.png" alt="Edit Buku" width="45%" height="45%"/>

## F. Hapus Buku
- [x] Form Hapus Buku digunakan untuk menghapus data buku yang sudah ada.
- [x] Pada saat pertama kali form muncul, semua Id buku ada di Combo Box Id buku.
- [x] Pada saat pertama kali form muncul, semua field selain Id buku secara otomatis terisi dengan data buku sesuai id buku yang terpilih pertama kali.
- [x] Pada saat id buku yang dipilih berubah, field lain juga ikut terisi secara otomatis dengan data buku sesuai id buku yang dipilih.
- [x] Pada saat tombol Hapus ditekan, hapus data buku sesuai buku yang dipilih.
- [x] Pada saat akan menghapus data, tampilkan pesan konfirmasi yang sesuai sebelum data benar benar terhapus.
- [x] Jika tombol Batal ditekan, tutup Form Hapus Buku dan kembali ke Form Home.
- [x] Setelah data berhasil dihapus, tutup Form Hapus Buku dan kembali ke Form Home serta refresh data grid yang ada di Form Home.
- [x] Tampilkan pesan kesalahan yang tepat jika perlu.
<img src="./STEMSEND%20Books%20Wireframe/Hapus%20Buku%20Form.png" alt="Hapus Buku" width="45%" height="45%"/>

**Waktu Pengerjaan : 6 jam**
## General Requirements

1. Setiap window harus dilengkapi validasi dan error message.
2. Gunakan proper naming conventions untuk semua material yang dikumpulkan.
3. Tampilkan form atau report pada tengah layer.
4. Wireframe yang disediakan hanyalah sebagai acuan. Modifikasi diperbolehkan selama tidak mempengaruhi kinerja fitur yang ada.
5. Perhatikan waktu pengerjakan dan gunakan waktu yang diberikan sebaik mungkin.

## Details 

|Module Name  |  Estimated Duration (Hours)| Requirements |
|--|--|--|
|Database Creation|<p align="center">2</p>|<ul> <li>Insert sample data yang telah diberikan ke database</li> <li>Insert sample data that has been given to the database</li> |
| Desktop Application| <p align="center"> 4 </p> | <ul><li> Create windows forms and its components based on given __requirements__ </li> <li>Login and logout mechanism</li> <li> Validate user input </li> <li> Show, insert, update, or delete records in the database </li> <li> Searching and filtering </li></ul>

## Marking Percentage
|Module|Percentage|
|--|--|
|Database Creation| 40%|
|Desktop Application| 60%|

