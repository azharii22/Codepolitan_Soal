## Pengenalan Sistem
1. kepanjangan API adalah ?
   
   a. Application Programing Index
   
   **b. Application Programing Interface**
   
   c. Application Programmer Interface
   
   d. Application Programing indexSpace
  
2. salah satu proyek laravel yang dikembangkan untuk melakukan otentikasi berbasis token adalah ?
   
   a. **Passport**
   
   b. API
   
   c. Vue.js
   
   d. json

3. yang bukan merupakan kegunaan dari fungsi API adalah ?
   
   a. login
   
   b. user profile
   
   **c. membaca berita**
   
   d. register
   
## Persiapan Passport Project
4. ketika kita belum menyiapkan sama sekali dalam passport project, hal yang pertama kali kita siapkan adalah ?
   
   **a. install laravel**
   
   b. make migrations
   
   c. make controller
   
   d. make factory

5. php artisan make:model Tweet -mcf

   -mcf diatas bermakna ?
   
   a. make create face
   
   b. make create function
   
   c. model create factory
   
   **d. model controller factory**

6. script agar dapat banyak kolom pada proses querry yaitu ?

   a. protected $table = [];
   
   **b. protected $guarded = [];**
   
   c. protected $migration = [];
   
   d. protected $model = [];

7. Database seeder pada laravel berfungsi untuk ?
   
   a. menjalankan DDL (data definition language)
   
   b. membuat table yang berulang
   
   c. membuat database ganda
   
   **d. menjalankan DML (data manipulation language)**
   
## Membuat Timeline Component
8. Apakah ExampleComponent.vu pada laravel sudah terpasang otomatis ketika kita menginstall laravel ?
   a. Ya
   **b. Tidak**

       9.  <template>
   
            <div>
   
            <div> 
   
            </div>
               
            </div>
   
           </template>
     
   Jika terdapat penulisan div 2 kali dan sejajar, maka yang terjadi adalah ?
   
   a. akan tetap berjalan sesuai perintah
   
   **b. error**
   
   c. menampilkan halaman 404
   
   d. menampilkan kolom

10. untuk memanggil componen kita harus melakukan compile terlebih dahulu. penulisannya scriptnya adalah ?
    
    a. npm run component
    
    **b. npm run dev**
    
    c. npm component start
    
    d. npm component run
    
## Menampilkan Data Tweets    
11. untuk mendapatkan data tweet pada halaman beranda maka kita membutuhkan ?
    
    a. route
    
    b. database
    
    c. akun user
    
    **d. API endpoint**
    
         12. mounted () {
      
          axios.get('/tweets').than((response) => {
            
            this.tweets = response.data;
      
         }).catch(err) => {
         
         console.log(err)
      
         });
       
   kondisi diatas adalah ?
   
   a. jika pemanggilan data tweets tidak sesuai
   
   **b. jika data tweets benar maka akan menampilkan sesuai respon dan jika salah akan menampilkan pesan error**
   
   c. jika salah maka sistem akan merespon untuk user agar menginput kembali data tweets
   
   d. jika benar maka sistem akan merespon sesuai data tweets

13. script untuk menampilkan nama dari pemilik tweets pada media heading adalah ?
    
          a. <h5 class="mt-0">{{ tweet.username }}</h5>
    
          b. <h5 class="mt-0">{{ tweet.name.user }}</h5>
    
         c. <h5 class="mt-0">{{ tweet.user }}</h5>
    
          **d. <h5 class="mt-0">{{ tweet.user.name }}</h5>**

14. middleware pada class controller digunakan untuk mengecek apakah user sudah pernah login atau belum. penulisan scriptnya adalah ?

    a. public fucntion _ _construct()
       
       {
            $middleware->('auth');
            
       }
    
    b. public fucntion _ _construct()
       
       {
            middleware=>('$auth');
            
       }
    
    **c. public fucntion _ _ construct()**
       
       **{
            $this->middleware('auth');**
            
       **}**
    
    d. public fucntion _ _construct()
       
       {
            middleware('auth');
            
       }

## Membuat Post Component
15. agar component template post.vue digunakan, maka kita perlu untuk mendaftarkannya terlebih dahulu pada folder ?
    
    a. Timeline.vue
    
    b. ExampleComponent.vue
    
    c. Post.vue
    
    **d. app.js**

16. import post from "./Post";
    
    maksud dari penulisan script di atas adalah ?
    
    **a. memanggil component post ke timeline lalu mengimportnya**
    
    b. mengimport method dari post
    
    c. mengimport database yang terhubung ke post
    
    d. memamnggil post yang terdapat pada route

17. penulisan script untuk memanggil nama component yang sudah diimport adalah ?
    
    a. components {
    
       $Post
       
       };
    
    b. components {
    
       Post()
       
       };
    
    c. components {
    
       Post
       
       };
    
    d. components {
    
       Post(import)
       
       };
