# SOAL STUDI KASUS WEB GEOLOCATION DAN HERE MAPS
## Pendahuluan

1. Pengertian Here Maps adalah

   **a. Aplikasi petunjuk jalan**

   b. Aplikasi jual beli

   c. Aplikasi Pendaftaran CPNS

   d. Aplikasi pencarian penginapan

2. Bagaimana jika ingin menggunakan Here Maps pada Web yang kita buat ?
 
    a. Mendownload Maps
    
    b. Menggunakan CSS
    
    **c. Menggunakan API dan SDK**
    
    d. Menggunakan Laravel
    
 3. Salah satu keuntungan menggunakan Here Maps adalah ?
 
    a. Dapat mengetahui kepadatan lalu lintas secara akurat
 
    **b. tidak menggunakan koneksi internet**
 
    c. aplikasi berbayar
 
    d. 
 
 4. Apakah kita harus mendaftar untuk mendapatkan API & SDK ?
  
    **a. Ya**
 
    b. Tidak
 
 5. Dimana letak jika kita ingin menambahkan lokasi menggunakan Here Maps pada web yang kita buat ?
  
    a. Parameter
    
    b. Class
    
    c. Database
    
    **d. Method**
 
 ## Instalasi dan Desain Tabel di Laravel
 
 6. Apa source code instal laravel menggunakan laravel installer ?
 
    a. composer create-project laravel/laravel nama_direktori_projek
    
    b. composer install
    
    **c. laravel new nama_direktori**
    
    d. php artisan serve
 
 7. Penggunaan perintah di bawah ini berfungsi untuk ?
    
    php artisan make:model
    
    a. membuat class
    
    b. membuat database
    
    c. membuat tabel
    
    **d. membuat model**
  
 8. Pngertian konsep MVC pada laravel adalah ?
    
    a. Model, Viewers, Controller
    
    **b. Model, View, Controller**
    
    c. Model, Viu, Controller
    
    d. Modul, View, Controller
  
 9. $table->foreign('user_id')->references('id')**on('users')->onDelete('cascade')**
    
    tulisan tebal diatas berfungsi untuk ?
   
    **a. menghapus data user**
    
    b. mengubah data user
    
    c. menambahkan data user
    
    d. memperbaiki data user
 
10. sassa
    
    a. 
    
    b. 
    
    c. 
    
    d. 

## Membuat Halaman Index Space
11. Fungsi Controller pada laravel adalah ?
    
    a. untuk menampilkan halaman yang telah kita desain
    
    b. untuk menyimpan data-data yang telah kita buat
    
    **c. sebagai penghubung antara View ke model**
    
    d. sebagai penghubung antara Database ke View

12. public function index()
    
    {
    
       return view('pages.space.index');
    
    }
    
    kutipan source code diatas berfungsi untuk ?
    
    a. memanggil database yang telah dibuat
    
    b. memanggil controller yang dituju
    
    c. menampilkan pesan error
    
    **d. menampilkan halaman space**
    
13. Pada suatu web kita diharuskan login terlebih dahulu jika ingin menampilkan halaman yang kita tuju. apa penulisan source code yang tepat !
    
    a. public function __construct()
    
    **b. $this->middleware(['auth']);**

    c. if(!Auth::attempt(request->only('email', 'password')))
    
    d. Auth::user()->revoke();

14. 
