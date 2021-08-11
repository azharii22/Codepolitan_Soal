## Pengenalan Sistem
1. kepanjangan API adalah ?
   
   a. Application Programing Index
   
   **b. Application Programing Interface**
   
   c. Application Programmer Interface
   
   d. Application Programing indexSpace
  
2. salah satu proyek laravel yang dikembangkan untuk melakukan otentikasi berbasis token adalah ?
   
   **a. Passport**
   
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
       
## Membuat API Endpoint Create Data
18. Method store pada tweetConttroller berfungsi untuk ?
    
    a. memanggil database
    
    **b. menampilkan sesuai request**
    
    c. verifikasi data user
    
    d. membuat kolom baru

19. apakah Tipe data Json pada laravel otomatis terbuat ?
    
    **a. Ya**
    
    b. Tidak

20. keunggulan dari method axios adalah ?
    
    a. script yang mudah diingat
    
    b. dapat melakukan verifikasi data secara otomatis
    
    **c. mendukung async dan awai untuk kode yang asinkronus**
    
    d. karena didukung oleh JSon
    
21. props: {
         
       twweets: Array
    
    }
    
    tipe data diatas adalah ?
    
    a. String
    
    **b. Array**
    
    c. Integer
    
    d. text

22. pada method form action digunakan untuk submit, akan tetapi submit tersebut dicegah lalu diarah kepada method post axios. dari logika tersebut, bagaimanakah penulisan source code nya ?
    
    **a. form action="#" @submit.prevent="post">**
    
    b. form action="#" @submit.post>
    
    c. form action="post" @submit>
    
    d. form action="prevent" @submit="post">

## Installasi Laravel Passport
23. untuk menginstall passport pada laravel kita dapat menggunakan ?
    
    a. text editor
    
    b. xampp
    
    c. kali linux 
    
    **d. composser**

24. untuk menambahkan tabel yang tersedia pada laravel passport, perintah yang kita lakukan di command prompt yaitu ?

    a. php artisan tabel
    
    b. php artisan serve
    
    **c. php artisan migrate**
    
    d. php artisan colom

25. php artisan passport::install

    perintah diatas digunakan untuk menginstall laravel passport. hal ini digunakan untuk ?
    
    **a. generate encryption keys agar akses token aman**
    
    b. agar passport laravel bisa berjalan
    
    c. generate encryption keys agar akses token terdaftar
    
    d. generate encryption keys agar akses token bisa login
    

26. agar dapat menggunakan laravel passport pada model user, kita perlu menambahkan ?
    
    a. API Endpoint
    
    b. HasApiEndpoint
    
    c. API Token
    
    **d. HasApiTokens**

## Menggunakan Vue Component dari Laravel Passport
27. Use Laravel\Passport\Passport;

    fungsi scrypt diatas adalah ?
    
    a. menggunakan laravel passport
    
    **b. mengimport laravel passport**
    
    c. mengekspor laravel passport
    
    d. generate laravel passport

28. perintah yang dijalankan pada command prompt agar kita dapat melihat daftar route adalah ?

    a. php artisan view::route
    
    b. php route::list
    
    **c. php artisan route::list**
    
    d. php laravel route::list\

29. setelah melakukan generate passport componen, kita perlu melakukan registrasi component-component tersebut. dimana registrasi component-component dilakukan ?

    a. laravel.com
    
    b. folder component
    
    **c. folder app.js**
    
    d. google.com

30. perbedaan method post dan get pada route adalah ?

    **a. Method POST data dikirimkan tidak melalui url parameter namun melalui form sedangkan GET melakukan parsing data melalui url parameter.**
    
    b. method post 
    
    c. 
    
    d. 

## Menguji Personal Token Laravel Passport
31. untuk melakukan pengujian, kita dapat menggunakan
    
    a. visual studio code
    
    b. sublime text
    
    c. xampp
    
    **d. postman**

32. token yang dihasilkan pada laravel yaitu melalui ?

    a. route
    
    b. controller
    
    **c. passport**
    
    d. post

33. untuk mendapatkan data user yang sedang login, kita perlu melakukan key dan value yang berisi ?

    a. key = auth dan value = bearer
    
    **b. key = authorization dan value = bearer (lalu paste value user)**
    
    c. key = authorization dan value = bearer
    
    d. key = auth dan value = bearer (lalu paste data user)

34. untuk menampilkan data user dari database berdasarkan id user yang terbesar, maka penulisan scrypt nya adalah ?

    **a. public function scopeLatestFirst($querry)**
    
       **{**
            
       **return $querry->orderBy('created_at', 'desc'**
            
       **}**
       
     b. public function scopeLatestFirst($querry)
    
       {
            
       return $querry->orderBy('created_at', 'asc'
            
       }
       
     c. public function scopeLatestFirst($querry)
    
       {
            
       return $querry->orderBy('created_at', '>1'
            
       }
       
     d. public function scopeLatestFirst($querry)
    
       {
            
       return $querry->orderBy('created_at', 'id_user'
            
       } 

## Persiapan Passclient Project
35. untuk membuat auth scaffolding kita perlu melakukan ?

    a. mengistall laravel scaffolding
    
    b. membuat scaffolding
    
    c. menginstall laravel ux
    
    **d. mengistall laravel ui**

36. laravel ui yang digunakan pada passclient project ini yaitu ?

    a. laravel ui json
    
    **b. laravel ui vue**
    
    c. laravel ui php
    
    d. laravel ui route
    
37. scrypt untuk memberitahukan bahwa user id sebagai foreign key yaitu ?

    a. $table->foreign('user_id')->references('users')->on('id')->onDelete('cascade');   
    
    b. $table->foreign('user_id')->references('users')->on('table_id')->onDelete('cascade');
    
    **c. $table->foreign('user_id')->references('id')->on('users')->onDelete('cascade');**
    
    d. $table->foreign('user_id')->references('user')->on('id')->onDelete('cascade');

         38. public function token()
    
            {
         
                  return $this->hasOne(Token::class, 'user_id', 'id')
     
            }
            
       maksud dari penulisan scrypt diatas adalah ?
       
       **a. relasi has one**
       
       b. mendapatkan user id
       
       c. memanggil id
       
       d. relasi database

## Membuat Request Authorize pada Laravel Passport
39. langkah pertama untuk request authorize ini adalah ?

    a. memanggil user id
    
    b. memanggil controller
    
    **c. membuat data client**
    
    d. membuat package baru

40. secret key pada authorize ini berfungsi untuk ?

    a. membuat scaffolding
    
    b. kode rahasia pengguna ketika login
    
    c. mendapatkan user id
    
    **d. membuat permintaan ke API**

41. Route::get('/auth/passport', 'Auth\OauthController@callBack');

    maksud dari method callback adalah ?
    
    a. panggilan balik sesuai request dari user
    
    **b. akan dijalanlan pada saat authorize di secret key berhasil**
    
    c. mendapatkan method post melalui form url
    
    d. mengirimkan data langsung ke action

42. penulisan nilai balik agar authorize ini dapat berjalan yaitu ?

    a. return redirect('http://passport.test/auth/authorize?' , $querry');
    
    b. return redirect('http://passport.test/oauth/authorize?' , $querry');
    
    c. return redirect('http://passport.test/authorize?' , $querry');
    
    **d. return redirect('http://passport.test/oauth/authorize?' , $querry');**

## Membuat Fungsi Callback dan Menyimpan Token
43. source code untuk method callback adalah ?

    **a. public function callback(Request $request)**
       
       **{**
       
       **dd($request)**
       
       **$this->client->post('http:://passport.test/oauth/token', [
       
       **'form_params' => [
       
       **'grant_type => 'authorization_code',**
       
       **'client_id' => '3',**
       
       **'client_secret' => '**pada bagian ini diisi secret key user**',**
       
       **'redirect_url' => http::/passCLient.test/auth/passport/callback',**
       
       **'code' => $request->code,**
       
       **]**
       
       **]);**
       
       **}**
       
    b. public function callback(Request $request)
       
       {
       
       $this->client->post('http:://passport.test/oauth/token', [
       
       'form_params' => [
       
       'grant_type => 'authorization_code',
       
       'client_id' => '3',
       
       'client_secret' => '**pada bagian ini diisi secret key user**',
       
       'redirect_url' => http::/passCLient.test/auth/passport/callback',
       
       'code' => $request->code,
       
       ]
       
       ]);
       
       }
       
    c. public function callback(Request $request)
       
       {
       
       dd($request)
       
       $this->client->post('http:://passport.test/oauth/token', [
       
       'grant_type => 'authorization_code',
       
       'client_id' => '3',
       
       'client_secret' => '**pada bagian ini diisi secret key user**',
       
       'redirect_url' => http::/passCLient.test/auth/passport/callback',
       
       'code' => $request->code,
       
       ]);
       
       }
       
    d. public function callback($request)
       
       {
       
       dd($request)
       
       $this->client->post('http:://passport.test/oauth/token', [
       
       'form_params' => [
       
       'grant_type => 'authorization_code',
       
       'client_id' => '3',
       
       'client_secret' => '**pada bagian ini diisi secret key user**',
       
       'redirect_url' => http::/passCLient.test/auth/passport/callback',
       
       'code' => $request->code,
       
       ]
       
       ]);
       
       }

44. Method Guzzle pada fungsi callback ini adalah >

    a. Method data yang dikirimkan tidak melalui url parameter namun melalui form
    
    b. Method anggilan balik sesuai request dari user
    
    c. Method yang akan dijalanlan pada saat authorize di secret key berhasil
    
    **d. package composer yang berisi segala function untuk melakukan request api**

45. source code untuk mengubah nilai response dari post method callback ke json adalah ?

    a. $response = json_decode($response->);
    
    **b. $response = json_decode($response->getBody());**
    
    c. $response = json_decode($response());
    
    d. $response = json($response->getBody());

46. $request->user()->token()->create([

    'access_token' => $response->access_token
    
    ]);
    
    maksud dari source code diatas adalah ?
    
    **a. nilai response yang akan disimpan ke dalam tabel token**
    
    b. membuat nilai respon pada tabel token
    
    c. mengakses token pada nilai respon
    
    d. nilai response yang diakses melalui token

## Menggunakan Token yang Disimpan
47. untuk menampilkan seluruh data tweets, kita perlu melakukan ?

    a. meminta akses pada admin
    
    **b. request pada API Endpoint**
    
    c. membuka database
    
    d. membuka halaman pencarian

48. source code untuk menampilkan data tweets pada method index di homeController adalah ?

    **a. public function index(Request $request)**
       
       **{**
       
       **$tweets = collect();**
       
       **if ($request->()->token) {**
       
       **$response = $this->client->get('http://passport.test/api/tweets' , [**
       
       **'headers' => [**
       
       **'Accept' => 'application/json',**
       
       **'Authrization' => 'Bearer' , . $request->user()->token->access_token**
       
       **]**
       
       **]);**
       
       **$tweets = collect (json_decode($response->getBody()));**
       
       **}**
       
       **return view('home')->with([**
       
       **'tweets' => $tweets**
       
       **]);**
       
       **}**
       
    b. public function index(Request $request)
       
       {
       
       $tweets = collect();
       
       if ($request->()->token) {
       
       $response = $this->client->get('http://passport.test/api/tweets' , [
       
       'headers' => [
       
       'Accept' => 'json_decode',
       
       'Authrization' => 'Bearer' , . $request->user()->token->access_token
       
       ]
       
       ]);
       
       $tweets = collect (json_decode($response->getBody()));
       
       }
       
       return view('home')->with([
       
       'tweets' => $tweets
       
       ]);
       
       }
       
    c. public function index(Request $request)
       
       $tweets = collect();
       
       if ($request->()->token) {
       
       $response = $this->client->get('http://passport.test/api/tweets' , [
       
       'headers' => [
       
       'Accept' => 'application/json',
       
       'Authrization' => 'Bearer' , . $request->user()->token->access_token
       
       ]
       
       ]);
       
       $tweets = collect (json_decode($response->getBody()));
       
       }
       
       return view('home')->with([
       
       'tweets' => $tweets
       
       ]);
       
    d. public function index(Request $request)
       
       {
       
       
       $tweets = collect();
       
       if ($request->()->token) {
       
       $response = $this->client->get('http://passport.test/api/tweets' , [
       
       'headers' => [
       
       'Accept' => 'application/json',
       
       'Authrization' => 'Bearer' , . $request->user()->token->access_token
       
       ]
       
       ]);
       
       $tweets = collect (application/json($response->getBody()));
       
       }
       
       return view('home')->with([
       
       'tweets' => $tweets
       
       ]);
       
       }

49. @if (Auth::user()->token)

    @if ($tweets->count())
    
    @foreach ($tweets as $tweets)
    
    <div class = "media mb-3">
   
    <img class = "mr-3" src="https://placehold.it/64x64" alt="Generic placeholder image">
   
    <div class = "media-body">
       
    <h5 class = "at-0">{{ $tweet->user->name }}</h5>
     
    {{ $tweet->body }}
    
    </div>
   
    </div>
   
    @endforeach
   
    @endif
   
    @else
   
    <p>Please <a href="{{ url('/auth/passport') }}" >authorize with Passport</a></p>
   
    @endif
    
    source code diatas merupakan ?
    
    a. perulangan
    
    b. tambah data
    
    **c. verifikasi**
    
    d. input data

50. kondisi yang salah maka akan diarahkan untuk mengisi passport, maka penulisan source code nya adalah ?

    **a. @else**
   
       <p>Please <a href="{{ url('/auth/passport') }}" >authorize with Passport</a></p>
   
       **@endif**
    
    b. @else
   
       <p> Please <a href="{{ url('/login') }}" >authorize with Passport</a></p>
   
       @endif
    
    c. @else
   
       <p>Please <a href="{{ url('/register') }}" >authorize with Passport</a></p>
   
       @endif
    
    d. @else
   
       <p>Please <a href=" url('/auth/passport') " >authorize with Passport</a></p>
   
       @endif

## Implementasi Scope di Laracel Passport
51. untuk menggunakan scope pada laravel, kita perlu menggunakan ?

    a. xampp
    
    b. akun user
    
    c. id user
    
    **d. middleware**

52. source code untuk middleware yang digunakan untuk user yang memiliki scope post tweet adalah ?

    a. Route::middleware('scope:post-tweet')->post('/tweets', 'TweetController@store');
    
    b. Route::middleware('auth:api', 'scope:post-tweet')->post('/tweets', 'TweetController@store');
    
    **c. Route::middleware(['auth:api', 'scope:post-tweet'])->post('/tweets', 'TweetController@store');**
    
    d. Route::middleware(['auth:api', 'scope:post-tweet'])->post'TweetController@store');
    
53. Route::middleware(['auth:api', 'scope:view-tweet'])->get('/tweets', 'TweetController@index');    

    penjelasan dari source code diatas adalah ?
    
    a. menampilkan scope tweet
    
    **b. menampilkan banyak data scope tweet**
    
    c. menampilkan scope tweet kosong
    
    d. menampilkan data scope tweet yang diinginkan
    
## Persiapan Fungsi Refresh Token
54. Apakah fungsi Token pada Laravel Passport ada batas waktu penggunaannya ?

    **a. Ya**
    
    b. Tidak
    
55. source code method untuk menyimpan data token yang sudah expire dan menyimpan data refresh token adalah ?

    **a. public function up()**
       
       **{**
       
       **Schema::table('tokens', function (Blueprint $table) {**
       
       **$table->bigInteger('expire_in');**
       
       **$table->text('refresh_token');**
       
       **});**
       
       **}**
       
    b. public function up()
       
       {
       
       Schema::table('tokens', (Blueprint $table) {
       
       $table->bigInteger('expire_in');
       
       $table->text('refresh_token');
       
       });
       
       }
       
    c. public function up()
       
       {
       
       Schema::table('tokens', function (Blueprint $table) {
       
       $table->bigInteger('expire_inSave');
       
       $table->text('refresh_token');
       
       });
       
       }
       
    d. public function up()
       
       {
       
       Schema::table('tokens', function (Blueprint $table) {
       
       $table->bigInteger('expire_save');
       
       $table->text('refresh_token');
       
       });
       
       }   

56. Passport::tokenExpireIn(now()->addSeconds(20));

    penjelasan dari source code diatas adalah ?
    
    a. menambahkan waktu 20 detik setelah waktu expire
    
    b. mperpanjang passport laravel
    
    c. memperbanyak table pada token
    
    **d. durasi token hanya 20 detik setelah dibuka**

## Implementasi Refresh Token di Laravel Passport

57. source code sebuah method yang digunakan untuk mengecek tanggal expire token adalah ?

    a. public function hasExpired()
       
       {
       
       return now()->gets($this->check->addSeconds($this->expires_in));
       
       }
       
    b. public function hasExpired()
       
       {
       
       return now()->gets($this->updated_at->seconds($this->expired_in));
       
       }
       
    **c. public function hasExpired()**
       
       **{**
       
       **return now()->gets($this->updated_at->addSeconds($this->expires_in));**
       
       **}**
       
    d. public function hasExpired()
       
       {
       
       return now()->gets($this->updated_at->addSeconds($this->hasExpired_in));
       
       }  
       
58. if (!$request->user() || !$request->user()->token) {
    
    return $next($request);
    
    }
    
    penjelesaran dari source code diatas adalah ?
    
    a. kondisi jika user melakukan autentikasi atau memiliki token maka akan dibiarkan untuk melanjutkan rquestnya
    
    **b. kondisi jika user tidak melakukan autentikasi dan tidak memiliki token maka akan dibiarkan untuk melanjutkan rquestnya**
    
    c. kondisi jika user tidak melakukan autentikasi atau tidak memiliki token maka akan error
    
    d. kondisi jika user tidak melakukan autentikasi maka akan dibiarkan untuk melanjutkan rquestnya

59. apa yang terjadi jika user yang sudah memiliki token tidak melakukan update ?

    a. masih bisa digunakan
    
    b. akan logout otomatis
    
    **c. token yang dimiliki akan hangus**
    
    d. error
    
60. berapa lama token di laravel passport berlaku ?

    a. 20 detik
    
    b. 1 minggu
    
    c. 1 bulan
    
    **d. 1 tahun**
