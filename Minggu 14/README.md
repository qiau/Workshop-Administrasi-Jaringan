    Nama		        : Raihan Eka Pramudya
    NRP		        : 3122600011
    Kelas		        : 2 D4 Teknik Informatika A
    Mata Kuliah	        : Workshop Administrasi Jaringan
    Dosen Pengampu	        : Dr. Ferry Astika Saputra S.T., M.Sc
    

- # _PROSES IMPLEMENTASI PROJECT MONITORING DOCKER CONTAINER_

### Instalasi Docker:
![alt text](assets/01.%20install%20docker.png)
### Membuat direktori baru bernama Monitoring:
![alt text](assets/03.%20buat%20direktori%20Monitoring.png)
### Membuat file docker-compose.yml dan prometheus.yml:
![alt text](assets/02.%20buat%20direktori%20untuk%20file%20monitoring.png)
### Instalasi kontainer Prometheus, Grafana, cAdvisor pada file docker-compose.yml:
![alt text](assets/04.%20isi%20docker-compose%20.%20yml.png)
### Konfigurasi prometheus pada file prometheus.yml untuk mengumpulkan metrik:
![alt text](assets/05.%20isi%20prometheus%20.%20yml.png)
### Mengecek kontainer:
![alt text](assets/06.%20cek%20kontainer%20berjalan.png)
### Mengecek metrics pada prometheus:
![alt text](assets/07.%20cek%20metrics%20di%20port%20prometheus.png)
### Menambahkan data source baru dari prometheus:
![alt text](assets/08.%20menambah%20datasource%20prometheus%20ke%20grafana.png)
![alt text](assets/09.%20import%20templat%20dashboard%20monitoring.png)
### Tampilan kondisi kontainer pada dashboard grafana:
![alt text](assets/10.%20tampilan%20dashboard.png)
### Membuat bot pada telegram dengan BotFather serta Get ID bot:
![alt text](assets/image.png)
### Konfigurasi Contact Points untuk telegram:
![alt text](assets/image-1.png)
### Konfigurasi Notification Policy untuk alert:
![alt text](assets/image-2.png)
### Konfigurasi alert rules untuk container yang mati:
![alt text](assets/image-3.png)
### Konfigurasi alert rules untuk memory pada tiap container:
![alt text](assets/image-4.png)
### Konfigurasi template message untuk susunan teks telegram:
![alt text](assets/image-5.png)
### Percobaan ketika ada container yang mati:
![alt text](assets/image-6.png)
