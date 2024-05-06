    Nama		        : Raihan Eka Pramudya
    NRP		        : 3122600011
    Kelas		        : 2 D4 Teknik Informatika A
    Mata Kuliah	        : Workshop Administrasi Jaringan
    Dosen Pengampu	        : Dr. Ferry Astika Saputra S.T., M.Sc
    

- # _INSTALL DOCKER ENGINE DEBIAN 12_

## - MENGHAPUS VERSI LAMA

- Ketik `for pkg in docker.io docker-doc docker-compose podman-docker containerd runc; do sudo apt-get remove $pkg; done`:
  ![](assets/docker1.png)

## - INSTALL DENGAN REPOSITORI APT

- Masukkan command berikut ini:
  - `sudo apt-get update`:
  - `sudo apt-get install ca-certificates curl`:
  - `sudo install -m 0755 -d /etc/apt/keyrings`:
  - `sudo curl -fsSL https://download.docker.com/linux/debian/gpg -o /etc/apt/keyrings/docker.asc`:
  - `sudo chmod a+r /etc/apt/keyrings/docker.asc`:
  - `echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/debian \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null`:
  ![](assets/docker2.png)
  - `sudo apt-get update`:
  ![](assets/docker2.png)
  
## - MENGGUNAKAN ROUNDCUBE

1. Lakukan instalasi roundcube dengan perintah
   ```bash
   sudo apt install roundcube
   ```
![](assets/rc1.png)

![](assets/rc2.png)

![](assets/rc3.png)

2. Lalu kita buat MariaDB database dan user untuk roundcubenya

![](assets/rc4.png)

3. Lalu konfigurasi config.inc.php di roundcube.

![](assets/rc5.png)

4. Konfigurasi apache.conf.

![](assets/rc6.png)

5. Konfigurasi 000-default.conf.

![](assets/rc7.png)

6. Lalu kita rekonfigurasi dengan perintah
   ```bash
   sudo dpkg-reconfigure roundcube-core
   ```
![](assets/rc8.png)

![](assets/rc9.png)

![](assets/rc10.png)

![](assets/rc11.png)

![](assets/rc12.png)

![](assets/rc13.png)

![](assets/rc14.png)

![](assets/rc15.png)

![](assets/rc16.png)

![](assets/rc17.png)

![](assets/rc18.png)

![](assets/rc19.png)

![](assets/rc20.png)
