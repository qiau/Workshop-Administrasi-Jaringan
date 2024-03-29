    Nama		        : Raihan Eka Pramudya
    NRP		        : 3122600011
    Kelas		        : 2 D4 Teknik Informatika A
    Mata Kuliah	        : Workshop Administrasi Jaringan
    Dosen Pengampu	        : Dr. Ferry Astika Saputra S.T., M.Sc
    

- # _Standar Struktur Direktori Pada Linux_ 
<p align="center">
  <br><img src="assets/tree.jpg"><br>
</p>
    
- ```/root```
    Ini merupakan direktori utama dimana semua operasi linux ada di sini. Direktori ini membawahi semua direktori sistem yang ada pada linux.
- ```/boot```
    Ini merupakan direktori dimana Boot Loader (file yang digunakan oleh sistem untuk booting) berada, seperti GRUB atau lilo, kernel, dan sebagainya. 
- ```/dev```
    Ini merupakan direktori dimana file-file sistem yang esensial, driver, serta perangkat yang terhubung tersimpan. Perangkat yang terhubung pada komputer akan dianggap file oleh linux, dan disimpan pada direktori ini.
- ```/etc```
    Ini merupakan direktori dimana konfigurasi file sistem berada. 
- ```/home```
    Ini merupakan direktori dimana file-file milik masing-masing user selain root disimpan
- ```/media```
    Ini merupakan direktori dimana user dapat men-mount removable media, seperti CD-ROM, USB, dsb.
- ```/mnt```
    Ini merupakan direktori dimana user dapat men-mount filesystem sementara. Biasanya digunakan untuk troubleshoot dari CDROM dan mengedit konfigurasinya.
- ```/opt```
    Direktori ini menyimpan software yang diinstall oleh user yang berasal dari distro lain. Direktori ini jarang digunakan di Linux untuk Optional Software Packages. 
- ```/proc```
    Direktori ini digunakan untuk informasi tentang proses, perangkat keras, jaringan, dan konfigurasi kernel secara dinamis.
- ```/storage```
    Direktori ini merupakan mount point dari partisi yang sudah dibuat sebelumnya.
- ```/sys```
    Direktori ini menyimpan firmware, kernel, dan file-file yang berkaitan.
- ```/tmp```
    Digunakan untuk menyimpan file sementara, yang akan dihapus ketika system melakukan reboot. 
- ```/usr```
    Direktori ini merupakan sub-hierarki dari direktori root yang berisi aplikasi dan tools yang bisa digunakan oleh user yang tidak esensial, seperti bin, sbin, dan lib. 
- ```/var```
    Direktori ini digunakan untuk menyimpan logs, lock files, crontlab, running process dsb. 
- ```/usr/bin```
    Direktori ini menyimpan program binary milik user, yang nantinya akan digunakan dalam mode single user.
- ```/usr/sbin```
    Direktori ini menyimpan System Binary dan System administration tools, yang digunakan jika bagi user root.
- ```/usr/lib```
    Ini merupakan direktori dimana file-file penting yang dibutuhkan oleh file binary disimpan.
- ```/usr/tmp```
    Merupakan direktori dimana file sementara disimpan, namun tidak terhapus ketika reboot.
