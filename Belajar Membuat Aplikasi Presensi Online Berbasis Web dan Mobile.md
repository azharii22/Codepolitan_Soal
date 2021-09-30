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

## Splash Activity (UI)
53. perintah untuk membuat halaman baru pada github yaitu ?

    **a. git checkout -b ui-splash**
    
    b. git new -b ui-splash
    
    c. git new page ui-splash
    
    d. git checkout -b ui - - splash

54. android:text="@string/app_name"/>

    maksud dari source code diatas adalah ?
    
    a. kolom text untuk menulis tahun aplikasi dibuat
    
    b. kolom text untuk menulis dimana aplikasi dibuat
    
    **c. kolom text untuk menulis nama aplikasi yang kita buat**
    
    d. kolom text untuk menulis nama pembuat aplikasi
    
55. perintah agar posisi gambar berada ditengah yaitu ?

    a. android:image="center"
    
    **b. android:gravity="center"**
    
    c. android:image="justify"
    
    d. android:gravity="justify"

56. android:textStyle="bold"

    yang dimaksud dengan bold adalah ?
    
    a. tulisan dengan style miring
    
    b. tulisan dengan style biasa
    
    c. tulisan dengan style vertical
    
    **d. tulisan dengan style tebal**

## Login Activity (UI)
57. source code untuk membuat kolom untuk mengisi email ketika login adalah ?

    **a. <?xml version="1.0" encoding="utf-8"?>**
       
       **<shape xmlns:android="http://schemas.android.com/apk/res/android"**
       
       **android:shape="rectangle">**

       **<corners android:radius="20dp"/>**
       
       **<solid android:color="#EFEFEF"/>**

       **</shape>**
       
   b. <?xml version="1.0" encoding="utf-8"?>
       
   <shape xmlns:android="http://schemas.android.com/apk/view/android"
       
       android:shape="rectangle">

       <corners android:radius="20dp"/>
       
       <solid android:color="#EFEFEF"/>

       </shape> 
       
 c. <?xml version="1.0" encoding="utf-8"?>
       
   <shape xmlns:android="http://schemas.android.com/apk/src/android"
       
       android:shape="rectangle">

       <corners android:radius="20dp"/>
       
       <solid android:color="#EFEFEF"/>

       </shape>  
       
 d. <?xml version="1.0" encoding="utf-8"?>
       
   <shape xmlns:android="http://schemas.android.com/apk/app/android"
       
       android:shape="rectangle">

       <corners android:radius="20dp"/>
       
       <solid android:color="#EFEFEF"/>

       </shape> 

58. agar password yang kita input tidak terlihat, maka perintah yang kita jalankan adalah ?

    a. app:endIconMode="password_star"
    
    **b. app:endIconMode="password_toggle"**
    
    c. app:endIconMode="password_code"
    
    d. app:endIconMode="password"

59. source untuk membuat button login adalah ?

    **a. android:id="@+id/btn_login"**
         
       **android:layout_width="match_parent"**
       
       **android:layout_height="wrap_content"**
       
       **android:text="@string/login"**
       
       **android:textColor="@android:color/white"**
       
       **android:background="@drawable/bg_btn_primary"**
       
       **android:layout_marginTop="24dp"/>**
       
   b. android:id="@+id/login"
      
   android:layout_width="match_parent"
      
   android:layout_height="wrap_content"
      
   android:text="@string/login"
      
   android:textColor="@android:color/white"
      
   android:background="@drawable/bg_btn_primary"
      
   android:layout_marginTop="24dp"/> 
   
   c. android:id="@+id/btn_login"
      
   android:layout_width="match_parent"
      
   android:layout_height="wrap_content"
      
   android:textColor="@android:color/white"
      
   android:background="@drawable/bg_btn_primary"
      
   android:layout_marginTop="24dp"/>
   
   d. android:id="@+id/login"
      
   android:layout_width="match_parent"
      
   android:layout_height="wrap_content"
      
   android:text="@string/login"
      
   android:textColor="@android:color/white"
      
   android:layout_marginTop="24dp"/>
   
60. android:src="@drawable/image_login"

    source code diatas digunakan untuk ?
    
    a. menghapus gambar yang sudah ada
    
    b. mengedit gambar yang sudah ada
    
    **c. menambahkan gambar pada tampilan**
    
    d. agar gambar yang diinput bisa banyak

## Forgot Password Activity (UI)
61. agar tombol forgot password berada di sebelah kanan, maka source code yang digunakan adalah ?

    a. android:layout_gravity="right"
    
    b. android:layout_gravity="center"
    
    c. android:layout_gravity="justify"
    
    **d. android"layout_gravity="end"**

62. Kita perlu mematikan Action Bar terlebih dahulu karena tidak semua activity menggunakan action bar.

    dimanakah letak action bar ?
    
    a. colors.xml
    
    b. strings.xml
    
    **c. styles.xml**
    
    d. activity.xml

63. app:layout_constraintTop_toTopOf="parent"

    source code diatas akan menampilkan app layout yang posisinya berada di ?
    
    **a. atas**
    
    b. bawah
    
    c. kanan
    
    d. kiri

64. fitur yang memudahkan untuk menulis kode yang berinteraksi dengan tampilan adalah fitur ?

    a. activity
    
    b. style
    
    c. splash
    
    **d. view binding**

## Main Activity (UI)
65. untuk menampilkan ikon, maka kita perlu mencarin ikon tersebut di ?

    a. drawable/new/icon
    
    **b. drawable/new/vector asset**
    
    c. drawable/new/image asset
    
    d. drawable/new/fragment
    
66. source code untuk membuat bottom navigation berupa lokasi adalah ?

    **a. <item
        
       android:id="@+id/action_attendance"
       
       android:title="@string/history"
       
       android:icon="@drawable/ic_baseline_location_on_24"
       
       app:showAsAction="ifRoom"/>
       
    b. <item
        
       android:id="@+id/action_attendance"
       
       android:title="@string/history"
       
       android:icon="@drawable/ic_baseline_location"
       
       app:showAsAction="ifRoom"/>   
       
    c. <item
        
       android:id="@+id/action_attendance"
       
       android:title="@string/history"
       
       android:icon="@drawable/navigation_location"
       
       app:showAsAction="ifRoom"/>  
       
    d. <item
        
       android:id="@+id/action_attendance"
       
       android:title="@string/history"
       
       android:icon="@drawable/maps_location"
       
       app:showAsAction="ifRoom"/>  

67. bahasa yang digunakan untuk membuat fragment adalah ?

    a. Java
    
    b. PhP
    
    **c. kotlin**
    
    d. C++

68. source code untuk membuat fragment history adalah ?

    **a. R.id.action_history -> {
       
       **openFragment(HistoryFragment())
       
       **return@setOnNavigationItemSelectedListener true
       
       **}
       
    b. R.id.action_history -> {
       
       openFragment(FragmentHistory())
       
       return@setOnNavigationItemSelectedListener true
       
       }   
       
    c. R.id.action_history -> {
       
       openFragment(FragmentHistory())
       
       }  
       
    d. R.id.action_history -> {
       
       openFragment(Fragment_History())
       
       return@setOnNavigationItemSelectedListener true
       
       }    

## Bottom Sheet Dialog (UI) - 01

69. Bottom Sheet Dialog adalah ?

    a. 

    b. 

    c. 

    d. 

70. app:behavior_hideable = false

    maksud dari source code diatas adalah  ?

    a. memunculkan menu back

    **b. agar bottom sheet selalu tampil dan tidak sembunyi**

    c. agar lokasi kita tidak aktif

    d. agar lokasi kita tetap aktif

71. Dimanakah letak Bottom Sheet Dialaog ?

    a. Atas

    b. Tengah

    **c. Bawah**

    d. Pojok kanan atas

72. Menu apa saja yang terdapat pada Bottom Sheet Dialog ?

    **a. History, Attendance, Profile**

    b. Profile, Logout

    c. History, Maps

    d. Maps, Waktu, Profile

## Bottom Sheet Dialog (UI) - 02

73. Source code untuk menambahkan foto pada Bottom Sheet Dialog adalah ?

    a. <TextView
        
        android:id="@+id/text_view_your_photo"
        
        android:layout_width="wrap_content"
        
        android:layout_height="wrap_content"
        
        android:text="@string/your_photo"
        
        android:textColor="@color/colorPrimary"
        
        android:textStyle="bold"
        
        android:layout_marginTop="20dp"
        
        app:layout_constraintStart_toStartOf="parent"
        
        app:layout_constraintTop_toBottomOf="@id/tv_current_photo"/>

    b. <TextView
        
        android:id="view_your_photo"
        
        android:layout_width="wrap_content"
        
        android:layout_height="wrap_content"
        
        android:text="your_photo"
        
        android:textColor="@color/colorPrimary"
        
        android:textStyle="bold"
        
        android:layout_marginTop="20dp"
        
        app:layout_constraintStart_toStartOf="parent"
        
        app:layout_constraintTop_toBottomOf="@id/tv_current_location"/>

    c. <TextView
        
        android:layout_width="wrap_content"
        
        android:layout_height="wrap_content"
        
        android:text="@string/your_photo"
        
        android:textColor="@color/colorPrimary"
        
        android:textStyle="bold"
        
        android:layout_marginTop="20dp"
        
        app:layout_constraintTop_toBottomOf="@id/tv_current_location"/>

    **d. <TextView**
        
        android:id="@+id/text_view_your_photo"
        
        android:layout_width="wrap_content"
        
        android:layout_height="wrap_content"
        
        android:text="@string/your_photo"
        
        android:textColor="@color/colorPrimary"
        
        android:textStyle="bold"
        
        android:layout_marginTop="20dp"
        
        app:layout_constraintStart_toStartOf="parent"
        
        app:layout_constraintTop_toBottomOf="@id/tv_current_location"/>

74. <ImageView
    
    android:id="@+id/iv_capture_photo"
    
    android:layout_width="match_parent"
    
    android:layout_height="wrap_content"
    
    app:layout_constraintHeight_min="40dp"
    
    app:layout_constraintHeight_max="200dp"
    
    android:scaleType="fitCenter"
    
    android:src="@drawable/ic_baseline_add_circle_24"
    
    android:background="@drawable/bg_capture_photo"
    
    android:layout_marginTop="12dp"
    
    app:layout_constraintTop_toBottomOf="@id/text_view_your_photo"/>

    a. agar mengetahui lokasi saat kita menambahkan foto

    **b. agar foto yang kita tambah dapat tampil**

    c. agar kita dapat menambahkan foto

    d. agar foto yang kita tambah berada di profile

75. untuk menambahkan tombol maka source code yang digunakan adalah ?

    **a. Button**

    b. TextView

    c. ImageView

    d. String

76. 

## Show Google Maps (UI)

77. untuk menampilkan google maps di android pada project yang kita buat, maka langkah pertama yang kita lakukan adalah ? ?

    a. masuk ke google dengan akun yang sudah terdaftar

    b. mendaftar ke google maps untuk mendapatkan akun

    **c. mendapatkan API Key dari google maps**

    d. 

78. setelah langkah pertama dilakukan, maka selanjutnya kita perlu untuk ?

    a. install php

    **b. mengaktifkan SDK untuk android**

    c. mendownload maps agar tetap terlihat secara offline

    d. menginstall android studio

79. setelah kita mendapatkan meta-data pada google maps, maka kita perlu membuat salinannya pada folder ?

    a. activity

    b. fragment

    c. layout

    **d. manifests**

80. source code untuk tampilan google maps adalah ?

    **a. <fragment**
    
    **android:id="@+id/map_attendance"**
    
    **android:name="com.google.android.gms.maps.SupportMapFragment"**
    
    **android:layout_width="match_parent"**
    
    **android:layout_height="match_parent"**
    
    **tools:context="com.example.mapwithmarker.MapsMarkerActivity" />**

## History Fragment (UI) - 01

81. Fragment adalah ?

    **a. Merupakan bagian dari UI dalam activity**

    b. Merupakan bagian model

    c. Merupakan bagian dari Mockup UI

    d. Merupakan bagian dari padding

82. Constraint layout adalah ?

    **a. Adalah sekelompok tampilan yang menyejajarkan semua anak dalam satu arah, secara vertikal atau horizontal**

    b. Komponen untuk menampilkan informasi dalam bentuk grid

    c. Adalah elemen yang berfungsi untuk menampilkan output berupa text

    d. Semua salah

83. ScrollView digunakan pada saat?

    **a.  Digunakan pada saat konten pada layar aplikasi harus di Scroll secara vertikal**

    b. Digunakan untuk mendapatkan nilai dari attribute

    c. Digunakan untuk menyisipkan satu atau lebih ke elemen terakhir ke database

    d. A dan B benar

84. Agar lebar atribut sesuai dengan lebar dari perangkat ?
    
    **a. android:layout_width="match_parent"**

    b. android:layout_width="match"

    c. android:layout_width="parent"

    d. android:layout_width="parent_match"
 
85. Agar lebar atribut sesuai dengan tinggi dari perangkat ?
    
    **a. android:layout_height="match_parent"**

    b. android:layout_width="match_parent"

    c. android:layout_height="parent_match"

    d. android:layout_width="parent"

##  History Fragment (UI) - 02

86. CardView digunakan untuk ?

    **a. Sebagai wrapper atau frame layout yang akan membungkus layout di dalamnya dengan desain menyerupai kartu**

    b. Komponen untuk menampilkan gambar

    c. Adalah sekelompok tampilan yang menyejajarkan semua anak dalam satu arah, secara vertikal atau horizontal

    d. komponen untuk menampilkan informasi dalam bentuk grid

87. Digunakan untuk apa properti CardElevation ?

    **a. Dipakai untuk menentukan ukuran dan kehalusan dari shadow sealami mungkin**

    b. Digunakan untuk mendapatkan nilai dari attribute

    c. Digunakan untuk menyisipkan satu atau lebih ke elemen terakhir ke database

    d. Semua salah

88. android:width="1dp", yang dimaksud dengan dp adalah ?

    a. Depend-independent Pixels
 
    **b. Density-independent Pixels**

    c. Density-internal Pixels

    d. Density-independent parts

89. Menentukan warna background dari card ?

    a. cardbackground

    **b. cardbackgroundColor**

    c. backgroundColor

    d. cardcolorbackground

90. Padding digunakan untuk ?

    **a. Mempertebal atau memperlapis sebuah konten View**

    b. Mempertipis atau memperlapis sebuah konten View

    c. Melebarkan atau memperlapis sebuah konten View
    
    d. Mempertebal atau memperlapis sebuah konten View

## Profile Fragment (UI)

91. Textview adalah ?

    **a. adalah elemen yang berfungsi untuk menampilkan output berupa text**

    b. Komponen untuk menampilkan gambar

    c. Adalah sekelompok tampilan yang menyejajarkan semua anak dalam satu arah, secara vertikal atau horizontal

    d. komponen untuk menampilkan informasi dalam bentuk grid

92. Agar background Appbar menjadi transparan ?

    a. android:background="@android:color=transparent

    b. android:background="@android:color/transparan

    c. android:cardbackground="@android:color/transparent

    **d. android:background="@android:color/transparent"**

92. Apa itu nested layout ?

    **a. Nested layout adalah kondisi di mana sebuah parent layout yang memiliki parent layout lagi di dalamnya**

    b. Nested layout adalah kondisi di mana sebuah parent layout yang tidak memiliki parent layout lagi di dalamnya

    c. Nested layout adalah kondisi di mana sebuah parent layout yang memiliki linear layout lagi di dalamnya

    d. Nested layout adalah kondisi di mana sebuah parent layout yang memiliki coonstraint layout lagi di dalamnya

93. Menetapkan arah tata letak secara Vertical ?

    a. android:orientation="Horizontal"

    b. android:vertical="Orientation"

    c. android:orientasi="Vertical"

    **d. android:orientation="Vertical"**

94. ImageView adalah ?

    **a. Komponen untuk menampilkan gambar**

    b. komponen untuk menampilkan informasi dalam bentuk list

    c. Komponen untuk menampilkan informasi dalam bentuk grid

    d. Semua salah

## Change Password Activity (UI)

95. Untuk menulis kode program untuk membuat aplikasi Android di file ?

    a. File Exe

    b. File Docx

    c. File Text

    **d. file Xml**

96. Berikut ini merupakan karakteristik bahasa pemrograman Android adalah ?
    a. Tidak memiliki library sendiri

    b. Pemrograman tidak berorientasi objek
    
    **c. Pemrograman berorientasi objek**

    d. Semua benar

97. Jika kita ingin membuat tombol, perlu menggunakan tag ?

   a. <Image>

    b. <View>

    **c. <Button>**

    d. <Text>

98. Kegunaan dari @+id/ ?

    **a. Digunakan saat akan memberikan sebuah id pada elemen atau tag dari layout XML untuk membedakan kegunaan masing-masing elemen atau tag**

    b. Digunakan saat akan memberikan sebuah title pada elemen atau tag dari layout XML untuk membedakan kegunaan masing-masing elemen atau tag

    c. Digunakan saat akan menggunakan salah satu elemen yang sudah diberikan @+id/ misalnya saat kita melakukan layouting menggunakan RelativeLayout

    d. A dan B benar

99. Jenis metode inputan untuk password ?
    
   **a. textPassword**

   b. textView

   c. textMail
 
   d. textButton

## Menggabung Seluruh Halaman & Debug

100. Fungsi dari postDelayed() adalah ?

   **a. Memberikan waktu jeda sebelum eksekusi**

   b. Langsung eksekusi tanpa waktu jeda untuk eksekusi

   c. Tidak memberikan efek apa-apa

   d. Memberikan waktu jeda selama satu jam

101. Penulisan untuk implementasi librari Anko ?

   a. intent "org.jetbrains.anko:anko-commons:0.10.8"

   b. implement "org.jetbrains.anko:anko-commons:0.10.8"

   c. implementasi "org.jetbrains.anko:anko-commons:0.10.8"

   **d. implementation "org.jetbrains.anko:anko-commons:0.10.8"**

102. Fungsi onClick() ?

   **a. Memberikan aksi ketika tombol disentuh**

   b. Memberikan efek visual

   c. Menjalankan aplikasi 

   d. Menjalankan Localhost

103. ImageButton digunakan untuk ?

   **a. Adalah suatu tombol dengan tampilan sebuah gambar atau image**

   b.  Adalah suatu tombol dengan tampilan sebuah text atau tulisan

   c.  Adalah suatu tombol dengan tampilan sebuah tulisan dengan gaya password

   d.  Semua salah

## Cek Sudah Login di Splash Activity

104. Difolder manakah kita dapat melihat login ?
     
     a. LoginActivity.kt
   
     **b. HawkStorage.kt**
   
     c. LoginResponse.kt
     
     d. LoginActivity.xml

105. tipe data boolean memiliki 2 nilai, yaitu ?
   
      a. 1 dan 2
   
      b. maju atau mundur
   
      **c. benar atau salah**
   
      d. angka atau huruf

106. if (isLogin){
      
      startActivity<MainActivity>()
      
      finishAffinity()  
   
      kondisi diatas adalah ketika ?
   
      a. ketika belum login
   
      b. ketika sudah daftar akun
   
      c. ketika belum punya akun
   
      **d. ketika sudah login maka akan diarahkan ke mainActivity**

## Forgot Password Activity
   
107.    
   
