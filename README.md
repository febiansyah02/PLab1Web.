# Laporan Pratikum 1 : Framework PHP ( codelgniter4 )

Repository ini dibuat untuk memenuhi tugas mata kuliah ***Pemograman Web 2***. Fokus utama pratikum ini adalah instalasi, konfigurasi dasar, dan implementasi konsep MVC pada Framework Codelgniter 4.  

Di susun oleh :  
Nama : M.Febiansyah Mulyadi  
Nim : 312410593  
Universitas Pelita Bangsa

***Tujuan Pratikum***  
1. Memahami konsep dasar Framework
2. Memahami konsep dasar MVC (Model-View-Controller)
3. Mampu membuat program sederhana menggunakan Codelgniter 4

# Langkah-Langkah Praktikum  
1. Persiapkan Lingkungan (Websever)

   Sebelum instalasi, beberapa ekstensi PHP harus diaktifkan melalui file _php.ini_ pada XAMPP agar Codelgniter 4 berjalan optimal :
   - Ekstensi yang di aktifkan : intl, mbstring, openssl, mysqlnd, dan xml.
   - Tindakan : Menghilangkan tanda titik koma (;) pada baris ekstensi terkait di _php.ini_ dan melakukan _restart Apache_.
  
2. Instalasi Codelgniter 4 ( Manual )

   Instalasi dilakukan secara manual dengan langkah berikut :

   - Menguduh file CI4 dari situs resmi
   - Mengekstrak file ke direktori htdocs/lab11_php_ci/ci4
   - Mengakses melalui browser di alamat http://localhost/lab11_ci/ci4/public/ untuk memastikan halaman "welcome" muncul.
3. Mengaktifkan Mode Debugging
   Untuk mempermudah penanganan _eror_ selama pengembangan, mode _environment_ di ubah ke development :

   - Mengubah nama file _env_ menjadi _.env_
   - Mengatur baris CI_ENVIROMENT = development.
  
4. Impelementasi Routing dan Controller

   Menambahkan rute baru pada file _app/Config/Routes.php_ untuk mengatur navigasu halaman :
   
   $routes->get('/about', 'Page::about');
   
   $routes->get('/contact', 'Page::contact');
   
   $routes->get('/faqs', 'Page::faqs');

   Selanjutnya, membuat Controller _page.php_ di folder _app/Controllers_ untuk menangani logika permintaan tersebut.

5. Membuat Layout dengan CSS ( view )

   Memisahkan kompenen tampilan menjadi _header.php_, _footer.php_, dan _about.php_ agar kode lebih rapi dan modular menggunakan konsep MVC :

   - Header : Berisi navigasi dan pemanggilan _style.css_ dari folder _public_
   - Footer : Berisi informasi hal cipta
   - About : Menggabungkan kompenen menggunakan perintah _$this->include()_
  
# Hasil Tugas (Latihan)

# Struktur Direktori Utama

- app/ : Berisi kode aplikasi ( Controller, Model, View )
- Publuc/ : Berisi aset public ( Index.php, CSS, Gambar )
- Writable/ : Berisi file yang dihasilkan aplikasi ( Logs, Cache )
