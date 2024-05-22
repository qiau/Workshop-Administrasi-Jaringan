    Nama		        : Raihan Eka Pramudya
    NRP		        : 3122600011
    Kelas		        : 2 D4 Teknik Informatika A
    Mata Kuliah	        : Workshop Administrasi Jaringan
    Dosen Pengampu	        : Dr. Ferry Astika Saputra S.T., M.Sc
    

- # _DOCKER 101_

## - GETTING STARTED

1. Setelah masuk ke labs buat instance baru.
2. Setelah terminal muncul masukkan kode berikut untuk membuka port 80 yang berisi tutorial.
   ```bash
   docker run -dp 80:80 docker/getting-started:pwd
   ```
![](assets/1.png)

## - OUR APPLICATION

1. Download file app.zip pada laman tutorial.
2. Ekstrak file tersebut dengan mengetikkan kode berikut pada terminal.
   ```bash
   unzip app.zip
   ```
   ![](assets/5.png)

3. Pindah ke direktori app dengan perintah.
   ```bash
   cd app/
   ```
4. Lihat isi dari direktori dengan perintah
   ```bash
   ls
   ```
5. Buat dan isi file bernama Dockerfile dengan perintah.
   ```bash
   touch Dockerfile
   vi Dockerfile
   ```
![](assets/6.png)

6. Tambahkan kode berikut ke dalam file.
   ```bash
    FROM node:10-alpine
    WORKDIR /app
    COPY . .
    RUN yarn install --production
    CMD ["node", "/app/src/index.js"]
   ```
   ![](assets/7.png)

7. Buat Container Image dengan perintah.
   ```bash
   docker build -t docker-101 .
   ```
   ![](assets/8.png)

8. Memulai kontainer dengan perintah.
   ```bash
   docker run -dp 3000:3000 docker-101
   ```
   ![](assets/9.png)
   
9. Tekan port 3000 dan hasil akan seperti berikut.
   ![](assets/27.png)

## - UPDATING OUR APP

1. Edit code pada file app.js dengan perintah berikut.
   ```bash
   vi ~/app/src/static/js/app.js
   ```

2. Hapus code pada line 56 dan ganti dengan.
   ```bash
    <p className="text-center">You have no todo items yet! Add one above!</p>
   ```
   ![](assets/10.png)

3. Update image dengan perintah.
   ```bash
    docker build -t docker-101 .
   ```
   ![](assets/11.png)

4. Jalankan container baru dengan perintah.
   ```bash
    docker run -dp 3000:3000 docker-101
   ```
   ![](assets/12.png)
   
5. Terdapat error karena port 3000 masih dipakai, jadi perlu menghapus port lama dan memulainya kembali.
   ```bash
   docker ps
   docker stop <the-container-id>
   docker rm <the-container-id>
   ```
   ![](assets/13.png)

6. Tekan port 3000 yang baru dan hasilnya seperti berikut.
   ![](assets/x.png)

## - SHARING OUR APP

1. Login terlebih dahulu ke Docker Hub dan buat repository baru bernama '101-todo-app' dengan visibilitas public.
   ![](assets/y.png)

2. Push ke repo dengan perintah.
   ```bash
   docker push dockersamples/101-todo-app
   ```
   ![](assets/15.png)
   
3. Terjadi error karena nama 'dockersamples' tidak sesuai sehingga perlu dilakukan login terlebih dahulu.
   ```bash
   docker login -u YOUR-USER-NAME
   ```
   ![](assets/16.png)

4. Setelah login kita lakukan kembali dengan memberikan tag.
   ```bash
   docker tag docker-101 YOUR-USER-NAME/101-todo-app
   ```
   ![](assets/17.png)

5. Coba push kembali dengan perintah.
   ```bash
   docker push YOUR-USER-NAME/101-todo-app
   ```
   ![](assets/18.png)

6. Buat instance baru dan jalankan kode berikut.
   ```bash
   docker run -dp 3000:3000 YOUR-USER-NAME/101-todo-app
   ```
   ![](assets/z.png)
   
7. Buka port 3000 dan hasilnya seperti berikut.
   ![](assets/z.png)

## - PERSISTING OUR DB

1. Mulai kontainer ubuntu dengan perintah.
   ```bash
   docker run -d ubuntu bash -c "shuf -i 1-10000 -n 1 -o /data.txt && tail -f /dev/null"
   ```
   ![](assets/22.png)

2. Untuk mengecek isi file data.txt kita perlu jalankan perintah berikut.
   ```bash
   docker ps
   docker exec <container-id> cat /data.txt
   ```
   ![](assets/23.png)
   
3. Kita cek apakah file data.txt ada didalam ubuntu dengan.
   ```bash
   docker run -it ubuntu ls /
   ```
   ![](assets/24.png)

4. Buat volume baru dengan nama todo-db.
   ```bash
   docker volume create todo-db
   ```
   ![](assets/25.png)

5. Jalankan kontainer todo dengan port 3000.
   ```bash
   docker run -dp 3000:3000 -v todo-db:/etc/todos docker-101
   ```
   ![](assets/26.png)