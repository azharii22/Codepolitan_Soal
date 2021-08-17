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
