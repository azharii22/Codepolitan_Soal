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
 
    d. menggunakan koneksi internet
 
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
 
10. Di bawah ini yang merupakan source code membuat table pada laravel adalah
    
    a. $ php artisan make:table create_space_table --create=space
    
    b. $ php artisan create:table --create=space
    
    c. $ php artisan make:migration create_space_table --create=space
    
    d. $ php artisan make:model(table)

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

14. File tampilan halaman index.blade.php (halaman utama) terletak pada folder

    **a. resource > views > pages > space**
    
    b. app > http > controllers
    
    c. routes
    
    d. resource > views > auth
    
15. Route pada laravel berfungsi sebagai
    
    **a. Penghubung antara user dengan keseluruhan framework**
    
    b. penghubung database dengan user
    
    c. menampilkan alamat web yang ingin dituju
    
    d. menyimpan database

## Menambahkan Marker Map Dalam Create Space
16. if(inputLat.value != '' && inputLng.value != '') 

    script diatas merupakan kondisi jika
    
    a. inputan kosong
    
    b. inputan angka
    
    **c. inputan tidak kosong**
    
    d. inputan alamat tujuan

17. Source code untuk menambahkan element id pada inputan adalah

    a. 
    ```
    {!! Form::text('latitude', null, ['class' => $error->has('latitude') ? 'form-control 
        is-invalid' : form-control, 'id' : 'lat' ]) !!}
    ```

    b.
    ```
    {!! Form::text('latitude', null, ['class' => $error->has('latitude') ? 'form-control 
        is-invalid' : form-control, 'id' = 'lat' ]) !!}
    ```

    **c.** 
    ```
    {!! Form::text('latitude', null, ['class' => $error->has('latitude') ? 'form-control 
        
        is-invalid' : form-control, 'id' => 'lat' ]) !!}
    ```
    **

    d.
    ```
    {!! Form::text('latitude', null, ['class' => $error->has('latitude') ? 'form-control 
        is-invalid' : form-control, 'id'('lat') ]) !!}
    ```

18. Source code untuk membuat marker adalah
    
    **a.**
    ```
    let marker = new H.map.Marker(objectLocalCoord, {
        volatility: true
    })

    marker.draggable = true;
    map.addObject(marker);
    ```
    **

    b.
    ```
    let marker = new H.map.Marker(objectLocalCoord, {
        volatility: false
    })

    marker.draggable = true;
    map.addObject(marker);
    ```

    c.
    ```
    let marker = new H.map.Marker(objectLocalCoord, {
        volatility: true
    })

    marker.draggable = false;
    map.addObject(marker);
    ```

    d.
    ```
    let marker = new H.map.Marker(objectLocalCoord, {
        volatility: false
    })

    marker.draggable = false;
    map.addObject(marker);
    ```


19. Apa yang perlu kita tambahkan agar saat menggeserkan/memindahkan marker, map nya tidak berpindah pindah adalah
    
    a. Membuat behavior baru

    b. membuat fungsi baru

    c. membuat objek baru

    **d. membuat eventListener**

20. Source code untuk mendapatkan latitude dan longitude pada saat kita selesai menggeserkar marker adalah..

    a.
    ```
    map.addEventListener('dragend', function(ev) {
        let target = ev.target;
        if(target instanceof H.map.Marker) {
            behavior.false();
            let resultCoord = map.screenToGeo(
                ev.currentPointer.viewportX,
                ev.currentPointer.viewportY,
            );
            inputLat.value = resultCoord.lat;
            inputLng.value = resultCoord.lng;
        }
    }, false);
    ```

    b.
    ```
    map.addEventListener('dragend', function(ev) {
        let target = ev.target;
        if(target instanceof H.map.Marker) {
            behavior.false();
            let resultCoord = map.screenToGeo(
                ev.currentPointer.viewportX,
                ev.currentPointer.viewportY,
            );
            inputLat = resultCoord.lat;
            inputLng = resultCoord.lng;
        }
    }, false);
    ```

    **c.**
    ```
    map.addEventListener('dragend', function(ev) {
        let target = ev.target;
        if(target instanceof H.map.Marker) {
            behavior.enable();
            let resultCoord = map.screenToGeo(
                ev.currentPointer.viewportX,
                ev.currentPointer.viewportY,
            );
            inputLat.value = resultCoord.lat;
            inputLng.value = resultCoord.lng;
        }
    }, false);
    ```
    **

    d.
    ```
    map.addEventListener('dragend', function(ev) {
        let target = ev.target;
        if(target instanceof H.map.Marker) {
            behavior.enable();
            let resultCoord = map.screenToGeo(
                ev.currentPointer.viewportX,
                ev.currentPointer.viewportY,
            );
            inputLat = resultCoord.lat;
            inputLng = resultCoord.lng;
        }
    }, false);
    ```

## Menyimpan dataspace ke Database
21. untuk melakukan request data user, script yang benar adalah

    a. $request->user.data(request->all());
    
    b. $request->user(data.all());
    
    c. $request->user(all);
    
    **d. $request->user()->spaces()->create($rewuest->all());**

22. return redirect()->route('space.index');

    script diatas adalah perintah untuk melakukan ?
    
    a. menampilkan halaman space index
    
    **b. mengembalikan ke route space index**
    
    c. menampilkan database space index
    
    d. mengembalikan database space index

23. JavaScript berfungsi untuk ?
    
    a. menampilkan perintah yang diinginkan
    
    **b. proses logika data**
    
    c. menyimpan data ke database
    
    d. membuat kolom input

## Menampilkan Codespace dalam list
24. @foreach pada laravel berfungsi untuk ?

    a. isi dari parameter
    
    b. mengisi form
    
    **c. perulangan**
    
    d. memanggil data user

25. script yang digunakan agar tombol berada di sebelah kanan adalah ?

    **a. float-right**
    
    b. allow-right
    
    c. allign-right
    
    d. text-right

26. <h6 class==card-subtittle>{{ $space->addres }}</h6>

    script di atas berfungsi untuk ?
    
    a. menginput alamat pada kolom addres dengan ukuran font besar
    
    b. menampilkan alamat yang ingin dituju
    
    **c. memampilkan alamat yang sudah tersimpan di table space**
    
    d. menghapus alamat yang sudah tersimpan di database

27. apa yang akan terjadi jika penulisan script seperti dibawah ini ?

    <a href==# class==card-link>Direction</a>
    
    **a. menampilkan tulisan Direction tetapi tidak bisa dibuka**
    
    b. menampilkan halaman Direction
    
    c. memanggil alamat yang ada pada Direction
    
    d. memanggil Direction

## Membuat Haversine Formula di Laravel
28. Haversine digunakan untuk ?
    
    **a. mencari jarak terdekat dari lokasi kita**
    
    b. mencari tujuan kita
    
    c. menampilkan padatnya lalu lintas jalan
    
    d. menampilkan rute pengguna mobil

29. referensi website harvesine yang terdapat banyak bahasa pemrogramman adalah ?

    a. petanikode.com
    
    **b. rosettacode.org**
    
    c. rottentomatoes.com
    
    d. glints.com

30. penulisan script untuk mencari jarak terdekat menggunakan skala KM yaitu ?

        a.  return $this->select('space.*')
       
         ->selectraw(
          
          '(1993 *
            
            acos( cos( radians(?) )*
              
              cos ( radians( latitude ) ) *
              
              cos ( radians(longitude ) - radians(?)) +
              
              sin ( radians(?) )*
              
              sin radians( latitude ) )
           
           )
       
         )
     
         b. return $this->select('space.*')
      
        ->selectraw(
          
          '(4378 *
            
            acos( cos( radians(?) )*
             
             cos ( radians( latitude ) ) *
             
             cos ( radians(longitude ) - radians(?)) -
             
             cos ( radians(?) )*
             
             sin ( radians( radians ) )
           
           )
      
        )
     
         c. return $this->select('space.*')
       
        ->selectraw(
          
          '(7865 *
            
            acos( cos( radians(?) )*
              
              cos ( radians( latitude ) ) *
              
              cos ( radians( latitude ) - ( radians(longitude )) +
              
              tan ( radians(?) )*
              
              sin ( radians( latitude ) )
           
           )
       
        )
     
        **d. return $this->select('space.*')
       
         ->selectraw(
          
          '(6371*
            
            acos( cos( radians(?) )*
              
              cos ( radians( latitude ) ) *
              
              cos ( radians(longitude ) - radians(?)) +
              
              sin ( radians(?) )*
              
              sin radians( latitude ) )
           
           )
       
         )**

31. ->orderBy('distance', 'asc');

    penulisan script diatas digunakan untuk ?
    
    a. urutan jarak yang sama
    
    b. urutan jarak dari yang terjauh ke terdekat
    
    **c. urutan jarak dari yang terdekat ke terjauh**
    
    d. urutan jarak yang terjauh

## Menampilkan Codespace di Here Maps
32. untuk menampilkan halaman codespace di here maps, yang perlu kita lakukan adalah ?
    a. membuat data base
    **b. membuat script layout codespace**
    c. membuat folder codespace
    d. membuat model codespace

33. penulisan script untuk mencari lokasi pada codespace yang benar adalah ?
    
    a. let spaces = []:
       
       const fetchSpaces = function (latitude, longitude, radius) {
       
       return new Promise(function (resolve, reject) {
              
       resolve(
                 
       fetch('/api/spaces?lat=${latitude}&lng=${longitude)&rad=${radius}')
                  
       .then((res) => res.json())
                  
       .then(function(data) {
                      
       data.forEach(function (value, index) {
                         
       let marker = new H.map.marker({
                            
       lat: value.latitude, lng: value.longitude
                         
       });
                          
       spaces.push(marker);
                         
       })
                      
       })
                       
       )
                     
       })
                    
       }
                    
       })**


        b. let spaces = []:
       
        const fetchSpaces = function (latitude, longitude, radius) {
       
        return new Promise(function (resolve, reject) {
              
              resolve(
                 
                 fetch('/api/spaces?lat=${latitude}&lng=${longitude)&rad=${radius}')
                  
                  .then((res) => res.json())
                  
                  .then(function(data) {
                      
                      data.forEach(function (value, index) {
                         
                         let marker = new H.map.marker({
                            
                            lat: value.latitude, lng: value.longitude
                         
                         });
                          
                          search.push(marker);
                         
                         })
                      
                      })
                       
                    )
                     
                  })
                    
                 }
                    
               })
               
               c. let spaces = []:
       
        const fetchSpaces = function (radius) {
       
        return new Promise(function (resolve, reject) {
              
              resolve(
                 
                 fetch('/api/spaces?lat=${latitude}&lng=${longitude)&rad=${radius}')
                  
                  .then((res) => res.json())
                  
                  .then(function(data) {
                      
                      data.forEach(function (radius, index) {
                         
                         let marker = new H.map.marker({
                            
                            lat: value.latitude, lng: value.longitude
                         
                         });
                          
                          spaces.push(marker);
                         
                         })
                      
                      })
                       
                    )
                     
                  })
                    
                 }
                    
               })
               
               d. let spaces = []:
       
        const fetchSpaces = function (latitude, longitude) {
       
        return new Promise(function (resolve, reject) {
              
              resolve(
                 
                 fetch('/api/spaces?lat=${latitude}&lng=${longitude)')
                  
                  .then((res) => res.json())
                  
                  .then(function(data) {
                      
                      data.forEach(function (value, index) {
                         
                         let marker = new H.map.marker({
                            
                            lat: value.latitude, lng: value.longitude
                         
                         });
                          
                          spaces.push(marker);
                         
                         })
                      
                      })
                       
                    )
                     
                  })
                    
                 }
                    
               })
               
        34. function clearSpace() {
        
        map.removeObjects(spaces);
        
        spaces = [];
     
        }
      
      fungsi diatas digunakan untuk ?
      
      a. menghapus spaces
      
      b. memindahkan object maps
      
      **c. menghapus object maps dan memindahkan ke titik yang baru**
      
      d. mengosongkan space
     
35. if (window.action == 'browse') adalah kondisi jika ?

    a. menghapus lokasi
    
    b. menambahkan lokasi
    
    c. memperbaru lokasi
    
    **d. mencari lokasi**

## Mengubah data Codespace
36. dimanakah letak script untuk membuat fungsi edit ?
    a. Model
    
    b. View
    
    **c. Controller**
    
    d. API

37. $space = Space::findOrFail($id);
    
    jika kondisi diatas error, maka apa yang terjadi ?
    
    a. menampilkan halaman utama
    
    **b. menampilkan 404**
    
    c. reload secara terus menerus
    
    d. tidak terjadi apa-apa

38. if ($space->user_id != request()->user()->id)
    
    kondisi diatas merupakan proses validasi berdasarkan ?
    
    **a. id dari user**
    
    b. username
    
    c. nomor hp user
    
    d. permintaan user

## Menghapus data codespace
39. @csrf @method('DELETE')
    
    method diatas digunakan untuk ?
    
    a. Tambah
    
    b. Edit
    
    **c. Hapus**
    
    d. Update

40. sebelum menghapus data, ada baiknya sistem melakukan konfirmasi kepada pengguna guna memastikan data yang dipilih untuk dihapus. penulisan script untuk mengkonfirmasi tersebut adalah ?
    
    **a. onClick="return confirm('are you sure?');">Delete</button>**
    
    b. onClick="return validation('are you sure?');">Delete</button>
    
    c. onClick="view confirm('are you sure?');">Delete</button>
    
    d. onClick="return validation('are you sure?');">Delete</button>

41. method yang digunakan dalam fungsi delete adalah ?
    
    a. GET
    
    **b. POST**
    
    c. Update
    
    d. Destroy
    
## Membuat Tampilan Route Codespace
42. event onclick biasanya terletak pada ?

    **a. tombol submit**
    
    b. tombol login
    
    c. tombol register
    
    d. tombol logout

43. source code untuk open url direction adalah ?

    a. function openDirection(lat, lng) {
       
       window.open('/space/${id}?from={objLocalCoord, latitude}, ${objLocalCoord, longitude}&to={lat}, ${lng}', "self");
       
       }
       
    b. function openDirection(lat, lng, id) {
       
       window.open('/space/${id}?from={latitude}, ${longitude}&to={lat}, ${lng}', "self");
       
       }
       
    c. function openDirection(lat, lng, id) {
       
       window.open('/space/${id}?from={objLocalCoord}, ${objLocalCoord, longitude}&to={lat}, ${lng}', "self");
       
       }
       
    **d. function openDirection(lat, lng, id) {**
       
       **window.open('/space/${id}?from={objLocalCoord, latitude}, ${objLocalCoord, longitude}&to={lat}, ${lng}', "self");**
       
       **}**   

44. semua peran fungsi pada laravel terdapat pada ?

    a. model
    
    b. view
    
    **c. controller**
    
    d. database

## Menampilkan Route Codespace di Here Maps
45. dalam laravel, garis rute pada maps disebut juga dengan ?
    a. lineAddres
    
    **b. lineString**
    
    c. lineStreet
    
    d. lineRoute

  46. map.getViewModel().setLookAtData({
        
        bounds: polyline.getBoundingBox()
    
    });
    
   script diatas berfungsi untuk ?
    
   a. menampilkan maps yang kita tuju
    
   b. fitur pencarian lokasi
    
   **c. fitur zoom in dan zoom out pada maps
    
   d. lokasi kita saat ini

47. <li>Travel Time: ${sunmary.travelTime.toMMS()} (in cureent traffic)</li>
    
    script diatas berfungsi untuk ?
    
    **a. menghitung waktu jarak tempuh sesuai keadaan lalu lintas**
    
    b. mengetahui waktu jarak tempuh
    
    c. menghitung waktu jarak tempuh hanya pada saat lalu lintas padat
    
    d. menghitung waktu jarak tempuh hanya pada saat lalu lintas lancar

## Membuat Multiple Input Photo
48. class yang berfungsi agar kita bisa mengupload banyak foto adalah ?
    
    a. class form-group input
    
    b. class form-group
    
    **c. class form-group increment**
    
    d. class form-group photo

49. name"photo[]" script disamping memiliki makna ?
    
    a. nama photo yang diakhiri dengan kurung siku
    
    **b. nama photo dengan tipe data array**
    
    c. nama photo
    
    d. nama photo dengan parameter kosong

50. class clone invisible berfungsi untuk ?
    
    a. membuat table
    
    b. group
    
    **c. tidak terlihat**
    
    d. menampilkan halaman utama
    
51. input type="file" artinya adalah
    
    a. inputan berupa pdf
    
    b. inputan berupa jpg/jpeg/png karena digunakan untuk foto
    
    c. inptan berupa 
    
    **d. inputan berupa file**

## Membuat Fungsi Upload dan Delete File
52. untuk mengupload foto yang lebih dari 1 dan bentuknya fotonya itu berbeda, bagaimanakah penulisan scrypt nya ?

    **a. 'photo' => ['required'],**
       
       **'photo' => ['mimes:jpg,png']**

      b. 'photo' => ['required'],
       
       'photo' => ['mimes jpg,png']
       
       c. 'photo' => ['required'],
       
       'photo' => ['jpeg,jpg,png,pdf']
       
       d. 'photo' => ['required'],
       
       'photo' => ['mimes:jpg,png,pdf']

53. putFile('spaces', $file);

    penjelesan sederhana dari kutipan scrypt diatas adalah ?
    
    a. proses input file yang mana spaces berfungsi untuk tombol submit dan $file berfungsi menyimpan gambar yang kita upload
    
    b. proses input file yang mana spaces berfungsi untuk menyimpan foto yang kita upload dan $file berfungsi untuk lokasi foto yang ingin kita upload
    
    c. proses input file yang mana spaces berfungsi untuk kolom kecil yang menampilkan gambar dan $file berfungsi untuk mengetahui lokasi pemnyimpnan gambar
    
    **d. proses input file yang mana spaces berfungsi untuk lokasi foto yang ingin kita upload dan $file berfungsi untuk menyimpan foto yang kita upload**

54. agar folder storage->public dapat digunakan pada teritori public, maka perintah apa yang kita jalankan ?
    
    a. artisan storage controller
    
    **b. artisan storage link**
    
    c. artisan storage serve
    
    d. artisan storage public

55. ketika kita mengupload gambar kosong maka akan menampilkan pesan error. penulisan scrypt dari logika disamping yaitu >

    a. @if ($errors->has('photo'))
    
      <ul class=photo>
  
      @foreach($errors->get('photo') as $ error)
  
      <li>{{ $error }}</li>
  
      @endforeach
      
      </ul>
      
      @endif
   
    b. @if ($errors->has('photo'))
    
      <ul class=($errors->get('photo') as $ error)>
  
      <li>{{ $error }}</li>
  
      @endforeach
      
      </ul>
      
      @endif
      
    c. @if ($errors->has('photo'))
  
      @foreach($errors->get('photo') as $ error)
  
      <li>{{ $error }}</li>
  
      @endforeach
      
      </ul>
      
      @endif   
      
    **d. @if ($errors->has('photo'))**
    
      **<ul class="alert alert-danger">**
  
      **@foreach($errors->get('photo') as $ error)**
  
      **<li>{{ $error }}</li>**
  
      **@endforeach**
      
      **</ul>**
      
      **@endif**   

56. Method apa yang digunakan untuk menghapus foto ?

    a. photo
    
    **b. destroy**
    
    c. add
    
    d. public
    
57. Method apa yang digunakan untuk menghapus foto ?

    a. photo

    **b. destroy**

    c. add

    d. public  
    
58. untuk menampilkan foto yang bersifat carousel, kita dapat mengambil source code pada ?

    a. xampp.php
    
    **b. getbootstrap.com**
    
    c. phplaravel.com
    
    d. html.com

59. key == 0 ? 'active' : ' ' ">

    logika dari scrypt diatas adalah ?
    
    **a. jika key bernilai 0 maka akan menampilkan class active**
    
    b. jika key bernilai lebih dari 0 maka akan menampilkan class active
    
    c. jika key bernilai 0 maka akan menampilkan tanda petik dua
    
    d. jika key bernilai active maka akan menampilkan halaman login
    
60. semua fungsi yang terdapat pada laravel ada di folder ?

    a. model
    
    b. view
    
    **c. controller**
    
    d. database
