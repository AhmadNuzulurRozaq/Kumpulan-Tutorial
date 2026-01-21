===========================================================
CARA INSTALL PHP 8.4 DI UBUNTU SERVER 24.04 LTS
===========================================================
- by : Ahmad Nuzulur Rozaq
===========================================================

01. Jalankan Perintah Update terlebih dahulu.
    Perintah : sudo apt update

02. Tambahkan repositori ppa:ondrej
    Perintah : sudo add-apt-repository ppa:ondrej/php

03. Install PHP 8.4
    Perintah : sudo apt install php8.4

04. Install ekstensi tambahan PHP yang umum digunakan.
    Perintah : sudo apt install libapache2-mod-php8.4 php8.4-fpm php8.4-mysql php8.4-xml php8.4-mbstring php8.4-curl
    
    CATATAN :
    Perintah diatas akan mendownload beberapa ekstensi pendukung php 8.4, sesuai nama paket diatas akan saya lampirkan dibawah ini :
    ---> libapache2-mod-php8.4
    ---> php8.4-fpm
    ---> php8.4-mysql
    ---> php8.4-xml
    ---> php8.4-mbstring
    ---> php8.4-curl

05. Aktifkan php8.4 fpm
    Perintah : ---> a2enmod proxy_fcgi setenvif
               ---> a2enconf php8.4-fpm

06. Tampilkan versi php
    Perintah : sudo nano /etc/www/html/info.php
    Catatan  : Akan terbuka editor nano, setelah terbuka ketik teks berikut dibawah ini :
               <?php
               phpinfo();
               ?>

07. Jalankan server
    Buka browser anda kemudian ketikkan ip ubuntu anda dan panggil file nya.
    Contoh : 192.168.1.8/info.php
