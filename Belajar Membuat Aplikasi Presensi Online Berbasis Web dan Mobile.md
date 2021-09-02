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
   
8. agar token bisa digunakan pada laravel sanctum, kita perlu untuk ?

   a. eksport
   
   b. konek database
   
   c. memanggil
   
   **d. import**

## Membuat API Endpoint Register Login dan Logout
9. php artisan make::controller Api/Auth/AuthController

   nama file controller dari source code diatas adalah ?
   
   a. Api
   
   b. Auth
   
   **c. AuthController**
   
   d. controller
   
10. source code untuk proses otentikasi pada saat register adalah ?

    **a. public function register(Request $request)**
       
       **{**
       
       **$data = $request->validate([**
       
       **'name' => ['required', 'string', 'max:255'],**
       
       **'email' => ['required', 'string', 'email', 'max:255', 'unique:users],**
       
       **'device_name' => ['required']**
       
       **]);**
    
    b. public function register(Request $request)
       
       {
       
       'name' => ['required', 'string', 'max:255'],
       
       'email' => ['required', 'string', 'email', 'max:255', 'unique:users],
       
       'device_name' => ['required']
      
    c. public function register(Request $request)
      
       {
       
       $data = $request->validate([
       
       'name' => ['required', 'string', 'email', 'max:255', 'unique:users],
       
       'device_name' => ['required']
       
       ]);
       
    d. public function register($request)
       
       {
       
       $data = $request->validate([
       
       'name' => ['required', 'string', 'max:255'],
       
       'email' => ['required', 'string', 'email', 'max:255', 'unique:users],
       
       'device_name' => ['required']   
       
       ]);
       
11. $user = User::where('email', $request->email)->first();

    source code diatas menjelaskan tentang ?
    
    a. koneksi database
    
    **b. otentikasi**
    
    c. relasi foreign key
    
    d. user

12. source code untuk proses logout adalah ?

    a. public function logout(Request $request)
       
       {
       
       $request->logout();
       
       return respons()->json([
       
       'message' => "log out succes'
       
       ], Response::HTTP_OK);
       
    b. public function logout(Request $request)
       
       {
       
       $request->tokens()->delete();
       
       return respons()->json([
       
       'message' => "log out succes'
       
       ], Response::HTTP_OK);
       
    **c. public function logout(Request $request)**
       
       **{**
       
       **$request->user()->tokens()->delete();**
       
       **return respons()->json([**
       
       **'message' => "log out succes'**
       
       **], Response::HTTP_OK);**
       
    d. public function logout(Request $request)
       
       {
       
       $request->user()->tokens()->delete();
       
       return respons()->json([
       
       'message' => "log out succes'
       
       ]; 

## Membuat API Endpoint Reset Password
13. Route::post ('/password/reset', 'Api\Auth\PasswordController@reset')
    
    ->middleware('auth:sanctum');
    
    nama endpoint pada source code diatas adalah ?
    
    a. post
   
    **b. password/reset**
    
    c. Auth
    
    d. reset

14. ->middleware('auth:sanctum');

    penjelasan source code diatas adalah ?
    
    a. posisi middleware untuk auth
    
    b. otentikasi sanctum
    
    c. method sanctum
    
    **d. untuk melakukan reset password kita perlu melakukan otentikasi**
    
15. public function reset(Request $request)
    
    {
    
    $request->validate([
    
    'password_old' => ['required', 'string', 'min:8],
    
    'password' => ['required', 'string', 'min:8', 'confirmed'],
    
    ]);
    
    bagian untuk memasukkan password baru adalah ?
    
    a. 'password_old' => ['required', 'string', 'min:8],
    
    b. 'password_new' => ['required', 'string', 'min:8],
    
    **c. 'password' => ['required', 'string', 'min:8', 'confirmed'],**
    
    d. $request->validate([

16. return response([
    
    'message' => 'Update password failed',
    
    ], Response::HTTP_UNPROCESSABLE_ENTITY);
    
    apa yang terjadi jika source code diatas dijalankan ?
    
    a. akan menampilkan form input
    
    **b. error**
    
    c. akan melakukan reset password
    
    d. koneksi ke database terkait passowrd baru
    
## Membuat API Endpoint Attendance In dan Out
17. source code untuk attendance in adalah ?

    **a. if ($attendanceType == 'in')** 
       
       **{**
       
       **if (! $UserAttendanceToday) {**
       
       **}**
       
       **return response()->json(**
       
       [
       
       **'message' => 'User has been checked in',**
       
       **],**
       
       **Response:: HTTP_OK**
       
       **);**
       
    b. if ($attendanceType == 'in') 
       
       {
       
       if ($UserAttendanceToday) {
       
       }
       
       return response()->json(
       
       [
       
       'message' => 'User has been checked in',
       
       ],
       
       Response:: HTTP_OK
       
       );
       
    c. if ($attendanceType =! 'in') 
       
       {
       
       if (! $UserAttendanceToday) {
       
       }
       
       return response()->json(
       
       [
       
       'message' => 'User has been checked in',
       
       ],
       
       Response:: HTTP_OK
       
       );
       
    d. if ($attendanceType = 'in') 
       
       {
       
       if (! $UserAttendanceToday) {
       
       }
       
       return response()->json(
       
       [
       
       'message' => 'User has been checked in',
       
       ],
       
       Response:: HTTP_OK
       
       );  
       
18. source code untuk attendance in adalah ?

     a. if ($attendanceType == 'out')
       
       {
       
       if (! $UserAttendanceToday) {
       
       if (UserAttendanceToday->status) {
       
       return response()->json(
       
       [
       
       'message' => 'User has been checked in',
       
       ],
       
       Response:: HTTP_OK
      
       ); 
       
       }
       
     b. if ($attendanceType =! 'out')
       
       {
       
       if ($UserAttendanceToday) {
       
       if (UserAttendanceToday->status) {
       
       return response()->json(
       
       [
       
       'message' => 'User has been checked in',
       
       ],
       
       Response:: HTTP_OK
      
       ); 
       
       }
       
    **c. if ($attendanceType == 'out')** 
       
       **{**
       
       **if ($UserAttendanceToday) {**
       
       **if (UserAttendanceToday->status) {**
       
       **return response()->json(**
       
       [
       
       **'message' => 'User has been checked in',**
       
       **],**
       
       **Response:: HTTP_OK**
      
       **);** 
       
       **}**
       
    d. if ($attendanceType = 'out')
       
       {
       
       if ($UserAttendanceToday) {
       
       if (UserAttendanceToday->status) {
       
       return response()->json(
       
       [
       
       'message' => 'User has been checked in',
       
       ],
       
       Response:: HTTP_OK
      
       ); 
       
       }
       
19. return response()->json(

    [
    
    'messgae' => 'Please do check in first',
    
    ],
    
    Response::HTTP_UNPROCESSABLE_ENTITY
    
    );
    
    kondisi diatas adalah ?
    
    a. untuk check out
    
    **b. nilai balik ketika ingin check out tapi belum log in**
    
    c. respon dari user
    
    d. menjalankan perintah request
    
20. pada saat kita ingin mengisi presensi online biasanya kita diminta untuk mengupload foto. variabel penyimpnan foto dalam laravel yaitu ?

    a. $photo
    
    b. $name
    
    **c. $path**
    
    d. $update

## Membuat API Endpoint Attendance History
21. untuk membuat attendance history, maka kita menggunakan route dengan method ?

    **a. get**
    
    b. post
    
    c. public
    
    d. private

22. $request->validate(
    
    [
    
    'form' => ['required'],
    
    'to' => ['required'],
    
    ]
    
    );
    
    kutipan source diatas merupakan proses ?
    
    a. input
    
    b. output
    
    c. proses
    
    **d. validasi**
    
23. response yang terdapat pada nilai balik fungsi history adalah ?

    a. response vue
    
    **b. response json**
    
    c. response user
    
    d. response db

## Implementasi Laravel UI Auth dan Proses Import Template
24. php artisan ui bootstrap --auth

    script diatas digunakan untuk >
    
    **a. generate ui auth**
    
    b. artisan dalam php
    
    c. auth laravel
    
    d. koneksi database

25. untuk menggunakan template web yang kita dapati dari internet, yang perlu kita lakukan adalah ?

    a. membuat folder baru
    
    b. menghapus semua folder yang ada
    
    **c. copy dan paste template**
    
    d. install laravel ui

26. untuk dapat menggunakan scaffolding bootstrap pada laravel kita perlu mengistallnya terlebih dahulu. cara installasinya yaitu:

    a. composer install laravel/ui:^2.4
    
    **b. composer require laravel/ui:^2.4**
    
    c. install laravel/ui:^2.4
    
    d. installlaravel --ui:^2.4

## Membuat Halaman CRUD User
27. method yang kita gunakan untuk menghapus adalah method ?

    a. create
    
    b. delete
    
    **c. destroy**
    
    d. index

28. if ($space->user_id != request()->user()->id)

    kondisi diatas merupakan proses validasi berdasarkan ?

    **a. id dari user**

    b. username

    c. nomor hp user

    d. permintaan user

29. sebelum menghapus data, ada baiknya sistem melakukan konfirmasi kepada pengguna guna memastikan data yang dipilih untuk dihapus. penulisan script untuk mengkonfirmasi tersebut adalah ?
    
    **a. onClick="return confirm('are you sure?');">Delete</button>**
    
    b. onClick="return validation('are you sure?');">Delete</button>
    
    c. onClick="view confirm('are you sure?');">Delete</button>
    
    d. onClick="return validation('are you sure?');">Delete</button>

30. source code untuk membuat data user baru adalah ?

    a. public function createNew()
       
       {
       
       return view('pages.user.create');
       
       }
       
    b. public function userNew()
       
       {
       
       return view('pages.user.create');
       
       }
       
    c. public function create()
       
       {
       
       return view('pagesUser.create');
       
       }
       
    **d. public function create()**
       
       **{**
       
       **return view('pages.user.create');**
       
       **}**   

## Membuat Halaman Index dan Show Attendance
31. public function index (Request $request)

    {
    
    if ($request->ajax()) {
    
    }
    
    return view ('pages.attendance.index')
    
    }
    
    penjelasan source code diatas adalah ?
    
    a. membuat fungsi index yang bersifat public
    
    **b. fungsi yang jika berhasil akan menampilkan request ajax dan jika tidak maka akan menampilkan pages attendance index**
    
    c. request ajax untuk menampilkan fungsi index
    
    d. validasi berdasarkan id user
    
32. berikut route yang benar untuk menampilkan attendance adalah ?

    **a. Route::resource('attendance', 'AttendanceController')->only(['index', 'show]);** 
    
    b. Route::resource('attendance', 'AttendanceController');
    
    c. Route::resource(AttendanceController)->only(['index', 'show]); 
    
    d. Route::resource('attendance', 'AttendanceController')->only(['show]); 

33. Cara menambahkan relasi Attendance dengan user adalah

    a. 
    ```
    public function user() {
        return $this->belongsTo(User::class);
    }
    ```

    b.
    ```
    public function user() {
        return $this->belongsTo(User::class);
    }
    ```

    c.
    ```
    public function user() {
        return $this->belongsTo(User::class);
    }
    ```

    d.
    ```
    public function user() {
        return $this->belongsTo(User::class);
    }
    ```

34. ``return row.status ? "Check Out" : "Check In"`` artinya adalah

    a. Mengembalikan nilai status jika true menampilkan Check In

    **b. Mengembalikan nilai status jika true menampilkan Check Out**

    c. Mengembalikan nilai status jika false menampilkan Check In

    d. a dan c benar

## Membuat Chart di Laravel

35. Cara menginstall package laravel charts adalah

    a. composer install consoletvs/charts "7.x"

    b. composer update consoletvs/charts "7.x"

    **c. composer require consoletvs/charts "7.x"**

    d. composer required consoletvs/charts "7.x"

36. Perintah artisan untuk membuat chart dengan laravel charts adalah

    a. php artisan create:chart SampleChart

    b. php artisan create:charts SampleChart

    **c. php artisan make:chart SampleChart**

    d. php artisan make:charts SampleChart

37. Method yang digunakan untuk mendapatkan jumlah data dari query adalah...

    a. length()

    **b. count()**
    
    c. max()

    d. exists()

38. Dimanakah letak directory untuk meregistrasikan chart...

    **a. app/Providers/AppServiceProvider**

    b. app/Providers/AuthServiceProvider

    c. app/Providers/EventServiceProvider

    d. app/Providers/RouteServiceProvider

## Membuat API Endpoint Forgot Password

39. Source code untuk membuat API Endpoint forgot password adalah...

    a. Route::update('/password/forgot', 'Api\Auth\PasswordController@SendResetLinkEmail');
    
    b. Route::update('/password/forgot', 'Api\Auth\PasswordController@SendResetLinkEmail')->middleware('auth:sanctum');

    **c. Route::post('/password/forgot', 'Api\Auth\PasswordController@SendResetLinkEmail');**

    d. Route::post('/password/forgot', 'Api\Auth\PasswordController@SendResetLinkEmail')->middleware('auth:sanctum');

40. Source code untuk memanggil SendPasswordResetEmails adalah...

    a. ``SendPasswordResetEmails;``

    b. ``SendPasswordResetEmails();``

    **c. ``use SendPasswordResetEmails;``**

    d. ``use SendPasswordResetEmails();``

41. Apa yang perlu di inputkan untuk mendapatkan SendPasswordResetEmails adalah...

    a. email dan password

    b. username dan password

    **c. email**

    d. username

42. Cara untuk mencoba atau mengetes apakah mendapatkan link reset password adalah

    a. Mengganti MAIL_MAILER=smtp

    **b. Mengganti MAIL_MAILER=log**

    c. Mengganti MAIL_DRIVER=smtp

    d. Mengganti MAIL_DRIVER=log


## Implementasi Middleware untuk Admin

43. Tujuan dari membuat middleware IsAdmin adalah?

    **a. Untuk mengecek apakah yang melakukan request merupakan user yang berstatus admin jika true lanjut melakukan request jika false redirect halaman home**

    b. Untuk mengecek apakah yang melakukan request merupakan user yang berstatus user jika true lanjut melakukan request jika false redirect halaman home

    c. Untuk mengecek apakah yang melakukan request merupakan user yang berstatus admin jika false lanjut melakukan request jika true redirect halaman home

    d. Untuk mengecek apakah yang melakukan request merupakan user yang berstatus user jika false lanjut melakukan request jika true redirect halaman home

44. Perintah artisan untuk membuat middleware IsAdmin adalah

    a. php artisan create:middleware IsAdmin

    b. php artisan build:middleware IsAdmin

    **c. php artisan make:middleware IsAdmin**

    d. php artisan migrate:middleware IsAdmin

45. Dimana meregistrasikan middleware yang telah dibuat?

    a. pada file kernel di variable middlewareGroup

    **b. pada file kernel di variable routeMiddleware**

    c. pada file AppServiceProvider di method register

    d. pada file AppServiceProvider di method boot

46. Bagaimana cara menambahkan middleware auth dan is_admin pada method construct?

    a. $this->middleware('auth', 'is_admin');

    b. $this->middleware({'auth', 'is_admin'});

    **c. $this->middleware(['auth', 'is_admin']);**

    d. $this->middleware('auth')->('is_admin');

## Intro

47. Library apa yang akan digunakan untuk consume API?

    a. volley

    **b. retrofit**

    c. dagger

    d. chuck

48. Web backend yang sudah dibuat digabungkan dengan mobile melalui...

    a. http request

    **b. API**

    c. database

    d. semua benar 

## Prepare Project

49. Untuk membuat project Activity apa yang dipilih

    a. Basic Activity

    **a. Empy Activity**

    a. No Activity

    a. Bottom Navigation Activity

50. Language dan minimum SDK yang digunakan adalah

    a. java, API 23

    b. java, API 25

    **c. kotlin, API 23**

    d. kotlin, API 25

51. Dimanakah letak untuk menaruh folder/file asset

    **a. drawable**

    b. layout

    c. values

    d. minmap

52. Dimanakah letak untuk mengatur warna

    a. res/values/styles.xml

    **b. res/values/colors.xml**

    c. res/values/color.xml

    d. res/values/strings.xml
