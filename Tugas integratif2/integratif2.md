# INTEGRATIF PHARSE 2 #

Mengubah DB_DATABASE di .env sesuai dengan nama database yang dibuat di phpmyadmin

![](gambar/1.PNG)

Buat 2 migrations yaitu table rss dan news

    - php artisan make:migration create_rss_table
    - php artisan make:migration create_news_table

![](gambar/2.PNG)

Tambahkan kolom name dan url pada tabel rss, seperti pada gambar dibawah

![](gambar/3.PNG)

Tambahkan kolom title, img_url, description, source_url,  dan rss_id pada tabel news, seperti pada gambar dibawah

![](gambar/4.PNG)

Untuk menjalankan migrasi yang dibuat, jalankan perintah

    php artisan migrate

![](gambar/5.PNG)

![](gambar/6.PNG)

Buat koneksi  model  ke database  dengan membuat seeder dan controller untuk tabel Rss dan News, dengan command

    php artisan make:model Rss –-seed –-controller

![](gambar/7.PNG)

Tambahkan script  (protected $table = 'rss';) pada file Rss.php dan ubah file RssSeeder.php serta DatabaseSeeder.php seperti pada gambar dibawah

![](gambar/8.PNG)

![](gambar/9.PNG)

![](gambar/10.PNG)

Kemudian cek koneksi dengan perintah

    php artisan db:seed

![](gambar/11.PNG)

![](gambar/12.PNG)

    php artisan make:model News –-controller

![](gambar/13.PNG)

Tambahkan script  (protected $table = 'news';) pada file News.php dan ubah file NewsController.php serta web.php seperti pada gambar dibawah

![](gambar/14.PNG)

![](gambar/15.PNG)

![](gambar/16.PNG)

Cek localhost http://127.0.0.1:8000/aggregrate/1 

![](gambar/17.PNG)

Buat logic untuk get rss data dengan id_rss, dengan script seperti pada gambar dibawah

![](gambar/18.PNG)

![](gambar/19.PNG)

Parsing XML ke Object
Tuliskan script seperti pada gambar dibawah

![](gambar/20.PNG)

Cek hasilnya di localhost http://127.0.0.1:8000/aggregrate/1

![](gambar/20b.PNG)

Buat script seperti pada gambar dibawah untuk menyimpan data pada tabel News

![](gambar/21.PNG)

Cek database pada tabel News

![](gambar/22.PNG)

Cek localhost http://127.0.0.1:8000/aggregrate/1

![](gambar/23.PNG)

Cek localhost http://127.0.0.1:8000/aggregrate/2

![](gambar/24.PNG)

![](gambar/26.PNG)

Cek localhost http://127.0.0.1:8000/aggregrate/4

![](gambar/27.PNG)

![](gambar/29.PNG)

### TETEP SEMANGAT LURR ###