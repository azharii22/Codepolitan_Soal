# Belajar Membuat Aplikasi Presensi Online Berbasis Web dan Mobile
## Install Framework dan Setup Migrations
1. laravel composer create-project --preafer-dist laravel/laravel:^7.0 attendance

   source code diatas adalah untuk menginstall laravel dengan nama project ?
   
   a. prefer
   
   b. dist
   
   c. laravel ^7.0
   
   **d. attendance**
   
2. php artisan make:model Attendance -m

   perintah diatas berfungsi untuk membuat model. model berfungsi untuk ?
   
   a. membuat kolom pada database
   
   **b. menghandle pemanggilan kolom**
   
   c. menambahkan kolom
   
   d. menghapus kolom
   
3. perintah untuk membuat database kita seperti baru dimigrate adalah ?

   **a. php artisan migrate:fresh**
   
   b. php artisan migrate:new
   
   c. php artisan migrate:clear
   
   d. php artisan migrate:drop

4. jika di dalam sebuah model terdapat 1 field yang tidak dicantumkan sesuai dengan migrations, maka yang terjadi adalah ?

   a. menampilkan 404
   
   b. menampilkan sesuai yang diinginkan jika konek internet
   
   **c. error**
   
   d. memanggil migrations

## Install Laravel Sanctum
5. laravel sanctum berfungsi untuk ?

   a. mendapatkan data user dari database
   
   b. membuat kolom pada database secara otomatis
   
   **c. memudahkan mobile developer dan juga frontend-js developer untuk membuat autentikasi pada aplikasi**
   
   d. membaca user yang sedang login

6. source code untuk menginstall composer pada laravel sanctum adalah ?

   a. composer install
   
   b. composer install laravel/sanctum
   
   c. composer require laravel sanctum
   
   **d. composer require laravel/sanctum**

7. php artisan vendor:publish --provider="Laravel\Sanctum\SanctumServiceProvider"

   source code diatas berfungsi ?
   
   a. untuk mempublish vendor provider
   
   **b. untuk mempublish config dari sanctum dan mendapat file baru**
   
   c. untuk mendapatkan config publish dari sanctum
   
   d. untuk melakukan database agar dapat dipublish
   
8.    
