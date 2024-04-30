    Nama		        : Raihan Eka Pramudya
    NRP		        : 3122600011
    Kelas		        : 2 D4 Teknik Informatika A
    Mata Kuliah	        : Workshop Administrasi Jaringan
    Dosen Pengampu	        : Dr. Ferry Astika Saputra S.T., M.Sc
    

- # _CHAT ANTAR KELOMPOK_

## MENGGUNAKAN TELNET

- Melakukan pengiriman pesan
  ketik `telnet mail.kelompok4.local 25` lalu masukkan sintaks berikut:
  - `HELO` untuk memulai sesi Telnet dengan server
  - `MAIL FROM:` untuk mendefinisikan alamat email pengirim
  - `RCPT TO:` untuk mendefinisikan alamat email penerima
  - `DATA` untuk memasukkan isi dari email yang dikirim
  
  ![kirim email](assets/kirim%20email.png)
  >Jika muncul output tersebut, maka email berhasil dikirim ke alamat tujuan

- Pengecekan pesan yang masuk
  ketik `telnet mail.kelompok4.local 110` lalu masukkan sintaks berikut:
  - `user` untuk memasukkan username dari user
  - `pass:` untuk memasukkan password dari user
  - `list:` untuk melihat list dari email yang diterima
  - `RETR {index}` untuk melihat isi pesan dari index tertentu
  
  ![terima email](assets/accept%20email.png)
  
## MENGGUNAKAN DEBIAN EVOLUTION

- Melakukan pengiriman pesan
  - Masukkan email pengirim
  - Masukkan email pengirim
  - Masukkan pesan yang akan dikirim
  
  ![mail send](assets/evol%20send%20email.png)

  Jika berhasil, maka akan muncul notifikasi berikut: 

  ![mail success](assets/evol%20success.png)
  
## MENGGUNAKAN akak
