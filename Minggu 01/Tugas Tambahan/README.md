    Nama		        : Raihan Eka Pramudya
    NRP		        : 3122600011
    Kelas		        : 2 D4 Teknik Informatika A
    Mata Kuliah	        : Workshop Administrasi Jaringan
    Dosen Pengampu	        : Dr. Ferry Astika Saputra S.T., M.Sc
    

- # _TUGAS TAMBAHAN_

**<h1 style="font-family:bahnschrift;">- Perbedaan Debian 12 (Bookworm) dan Debian 11 (Bullseye)</h1>**

| Perbedaan         | Debian 12 (Bookworm)                                                          | Debian 11 (Bullseye)                                                              |
| ----------------- | ----------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| Versi Kernel      | 6.1                                                                           | 5.10                                                                              |
| Kebutuhan Sistem  | Mungkin lebih tinggi                                                          | Moderat                                                                           |
| Penerapan systemd | Aktivasi jurnal persisten oleh default dengan fallback ke penyimpanan volatil | Tidak dijelaskan, tetapi mungkin ada perbedaan versi                              |
| Perbedaan Package | Lebih baru, 11.089 paket baru, non-free software disertakan dalam ISO primer  | Tidak dijelaskan jumlahnya, namun non-free packages disertakan dalam ISO terpisah |

#
**<h1 style="font-family:bahnschrift;">- Penjelasan mengenai $less /etc/group</h1>**
<img src="assets/deb1.png" width="500">
>Command ini akan membuka berkas group yang terletak di direktori /etc/ menggunakan less. less digunakan untuk melihat isi berkas secara bertahap dan memungkinkan untuk melakukan navigasi dengan lebih mudah. Kita dapat menggunakan tombol "Page Up" dan "Page Down", dan berbagai opsi lainnya untuk membaca dan menjelajahi isi berkas tersebut.
#
**<h1 style="font-family:bahnschrift;">- Perbedaan su dan su - pada linux</h1>**

  >command su pada linux memungkinkan user untuk mempertahankan current user environtment ketika switch user. Sedangkan su - digunakan untuk mengeksekusi shell login untuk transfer user account tertentu, serta secara umum mengubah environtment variables dan working directory set di environtmen milik user tertentu.

**<h3 style="font-family:bahnschrift;">Perintah su</h3>**

  Pada command ini, user dapat beralih ke user lain secara spesifik. Jika user tidak memilih user secara spesifik, maka linux secara default akan masuk ke root. Dengan menjalankan command su, ueser bisa switch ke user lain tanpa harus menjalankan login shell, dan environtment variables yang sudah di set pada akun saat ini tidak akan diubah.

- **contoh :** 
``` 
$ su raihan
```
>dengan menjalankan perintah tersebut, user saat ini akan dialihkan ke user yang bernama 'raihan' tanpa perlu menjalankan login shell, serta setting environtment variables yang tetap.

**<h3 style="font-family:bahnschrift;">Perintah su -</h3>**
    
  Pada command ini, user dapat beralih ke user lain, sama seperti perintah su. Namun, setting dari user saat ini akan diubah, dan environtment variables dari main user akan dihapus. 
- **contoh :**
```
$ su - raihan
```
>perintah ini digunakan untuk beralih ke user 'raihan' dengan menjalankan shell login. Jika user tidak menentukan user secara spesifik ke perintah ini, maka secara default user akan masuk ke Root.
#
**<h1 style="font-family:bahnschrift;">- Fungsi dari sudo</h1>**
>"sudo" (superuser do) adalah perintah yang memungkinkan pengguna untuk menjalankan perintah sebagai pengguna lain, biasanya sebagai superuser (root). Ini memberikan hak akses terbatas dan terkontrol kepada pengguna, yang dicatat dan dilacak.

#
**<h1 style="font-family:bahnschrift;">- Langkah-langkah penambahan user sebagai user sudo</h1>**

1. Gunakan perintah su - untuk masuk sebagai root.
2. Setelah masuk sebagai root, jalankan perintah visudo untuk mengedit file konfigurasi sudoers.
3. Tambahkan baris berikut di bawah baris yang mencakup user root pada bagian " # User privilege specification":

   username ALL=(ALL:ALL) ALL

   (Gantilah "username" dengan nama pengguna yang ingin User tambahkan.)

4. Simpan dan keluar dari editor.

Dengan langkah-langkah ini, pengguna yang User tambahkan akan memiliki hak akses sudo di sistem. Pastikan untuk memberikan hak akses sudo hanya kepada pengguna yang membutuhkannya dan amankan konfigurasi sudoers dengan hati-hati.
#
**<h1 style="font-family:bahnschrift;">- Role yang ada pada linux</h1>**
1. User (Pengguna):
    >Pengguna adalah individu yang dapat mengakses sistem. Masing-masing pengguna memiliki akunnya sendiri dengan hak akses tertentu.
    
    >Tugas: Mengelola file pribadi, menjalankan perintah di terminal, dan menggunakan sumber daya sistem.

2. Root (Superuser):

    >Root adalah pengguna dengan hak akses tertinggi. Hak akses root memungkinkan pengguna untuk melakukan perubahan sistem kritis.
    
    >Tugas: Menginstal dan menghapus perangkat lunak, mengelola pengguna, mengkonfigurasi sistem, dan melakukan tugas administratif lainnya.

3. Administrator (sudo):

    > Pengguna yang diberi hak akses khusus melalui konfigurasi sudo.   Administrator dapat menjalankan perintah dengan hak akses root sesaat.
    
    >Tugas: Menjalankan perintah dengan hak akses tambahan, membantu dalam administrasi sistem.

4. Sysadmin (Administrator Sistem):

    >Seorang administrator sistem memiliki tanggung jawab untuk merawat dan mengelola infrastruktur IT.

    >Tugas: Memastikan keamanan, ketersediaan, dan kinerja sistem, serta melakukan pemeliharaan dan pemecahan masalah.

5. Network Administrator (Administrator Jaringan):

    >Bertanggung jawab atas infrastruktur jaringan dan koneksi di dalam dan di luar sistem.

    > Tugas: Konfigurasi jaringan, pemecahan masalah koneksi, manajemen firewall, dan keamanan jaringan.

6. Database Administrator (Administrator Basis Data):

    > Bertanggung jawab atas manajemen dan kinerja basis data pada sistem.
    
    > Tugas: Pemasangan, konfigurasi, pemeliharaan, backup, dan pemulihan basis data.

7. Web Server (Pelayan Web):

    >Merujuk pada peran mesin yang menyediakan layanan web, seperti Apache atau Nginx.

    >Tugas: Menyajikan halaman web, menangani permintaan HTTP, dan menyediakan aplikasi web.

8. File Server (Pelayan File):

    >Berfungsi sebagai pusat penyimpanan dan distribusi file di dalam jaringan.

    >Tugas: Berbagi file, mengelola izin akses, dan menyediakan penyimpanan berbasis jaringan (NAS).
