Nama : Raden Kodrat

Kelas : TI.20.D.1

NIM : 312010271

Langkah-langkah Praktikum:

Membuat folder lab11_php_
![12](https://user-images.githubusercontent.com/101814131/175825826-d5ef0bfe-6a47-425b-b196-bb36146cdd57.png)



2.Sebelum memulai menggunakan Framework Codeigniter, perlu dilakukan konfigurasi pada webserver. Beberapa ekstensi PHP perlu diaktifkan untuk kebutuhan pengembangan Codeigniter 4. Berikut beberapa ekstensi yang perlu diaktifkan: • php-json ekstension untuk bekerja dengan JSON; • php-mysqlnd native driver untuk MySQL; • php-xml ekstension untuk bekerja dengan XML; • php-intl ekstensi untuk membuat aplikasi multibahasa; • libcurl (opsional), jika ingin pakai Curl. Untuk mengaktifkan ekstentsi tersebut, melalu XAMPP Control Panel, pada bagian Apache klik Config -> PHP.ini
![image](https://user-images.githubusercontent.com/101814131/175823924-389e906c-f2e3-4c82-b1cb-7c60076b88e7.png)


Pada bagian extention, hilangkan tanda ; (titik koma) pada ekstensi yang akan diaktifkan. Kemudian simpan kembali filenya dan restart Apache web server.
![2](https://user-images.githubusercontent.com/101814131/175823968-efe10c27-342e-426a-a3b4-ef9781a276ff.PNG)


3.Instalasi Codeigniter 4 Untuk melakukan instalasi Codeigniter 4 dapat dilakukan dengan dua cara, yaitu cara manual dan menggunakan composer. Pada praktikum ini kita menggunakan cara manual. • Unduh Codeigniter dari website https://codeigniter.com/download • Extrak file zip Codeigniter ke direktori htdocs/lab11_ci. • Ubah nama direktory framework-4.x.xx menjadi ci4. • Buka browser dengan alamat http://localhost/lab11_ci/ci4/public/
![image](https://user-images.githubusercontent.com/101814131/176965173-6f436240-e73e-4e67-8f3f-0d2e30893271.png)



4.Menjalankan CLI (Command Line Interface) Codeigniter 4 menyediakan CLI untuk mempermudah proses development. Untuk mengakses CLI buka terminal/command prompt. Kemudian arahkan lokasi direktori sesuai dengan direktori kerja project dibuat (xampp/htdocs/lab11_ci/ci4/)
![image](https://user-images.githubusercontent.com/101814131/175824003-1b88020d-16d9-4d6b-bb52-a05dc8fdb69a.png)

Perintah yang dapat dijalankan untuk memanggil CLI Codeigniter adalah:
![image](https://user-images.githubusercontent.com/101814131/175824039-2c6eaa7f-35b0-4274-9897-4a45caf2afa2.png)


5.Mengaktifkan Mode Debugging Codeigniter 4 menyediakan fitur debugging untuk memudahkan developer untuk mengetahui pesan error apabila terjadi kesalahan dalam membuat kode program. Secara default fitur ini belum aktif. Ketika terjadi error pada aplikasi akan ditampilkan pesan kesalahan seperti berikut.

![image](https://user-images.githubusercontent.com/101814131/176965291-bc01c44e-8736-4a3c-812e-307e794c7f27.png)



Semua jenis error akan ditampilkan sama. Untuk memudahkan mengetahui jenis errornya, maka perlu diaktifkan mode debugging dengan mengubah nilai konfigurasi pada environment variable CI_ENVIRINMENT menjadi development. Ubah nama file env menjadi .env kemudian buka file tersebut dan ubah nilai variable CI_ENVIRINMENT menjadi development.
![image](https://user-images.githubusercontent.com/101814131/175824062-5d2096a7-dfde-4897-8c75-1629d62716c6.png)


Contoh eror Untuk mencoba error tersebut, ubah kode pada file app/Controller/Home.php hilangkan titik koma pada akhir kode.

![image](https://user-images.githubusercontent.com/101814131/175824075-91da8a79-ceb7-402b-953d-077d877d0966.png)
![image](https://user-images.githubusercontent.com/101814131/176965372-b51ac729-8986-470c-8745-48b837c36c2b.png)



7.Membuat route baru dalam Routes.php Tambahkan kode berikut ini pada Routes.php
![image](https://user-images.githubusercontent.com/101814131/175824123-8a2ffc9a-737a-4103-be34-50707e6924fa.png)
![image](https://user-images.githubusercontent.com/101814131/175824138-00b08800-e04e-4449-b190-e591e53396dc.png)


Selanjutnya coba akses route yang telah dibuat dengan mengakses alamat url http://localhost:8080/about seperti berikut. Maka hasilnya akan terjadi error, yang artinya file/page tersebut tidak ada. Untuk dapat mengakses halaman tersebut, harus dibuat terlebih dahulu Contoller yang sesuai dengan routing yang dibuat yaitu Contoller Page.
![image](https://user-images.githubusercontent.com/101814131/176965424-916595ec-72a8-4326-99b4-08c5521435ff.png)



8.Membuat Controller Kemudian membuat Controller Page. Buat file baru dengan nama page.php pada direktori Controller kemudian isi kodenya seperti berikut.
![image](https://user-images.githubusercontent.com/101814131/175824172-08253e23-c7a5-4b80-bd76-30e6092f0c17.png)


Selanjutnya refresh Kembali browser, maka akan ditampilkan hasilnya yaotu halaman sudah dapat diakses.
![image](https://user-images.githubusercontent.com/101814131/176965486-681bcb72-ee01-491e-b335-8b7c5ec98d38.png)



9.Auto Routing Secara default fitur autoroute pada Codeiginiter sudah aktif. Untuk mengubah status autoroute dapat mengubah nilai variabelnya. Untuk menonaktifkan ubah nilai true menjadi false.
![image](https://user-images.githubusercontent.com/101814131/175824206-09b09a48-9e10-4413-a2b4-f5571039a8ee.png)


Method ini belum ada pada routing, sehingga cara mengaksesnya dengan menggunakan alamat: http://localhost:8080/page/tos
![image](https://user-images.githubusercontent.com/101814131/176965750-72f0bc49-d217-4a88-8f53-b949c11cb712.png)



10.Membuat View Selanjutnya adalam membuat view untuk tampilan web agar lebih menarik. Buat file baru dengan nama about.php pada direktori view (app/view/about.php) kemudian isi kodenya seperti berikut.
![image](https://user-images.githubusercontent.com/101814131/175824236-128542fe-07db-49e8-9e7a-0bdb0a045ea4.png)


Ubah method about pada class Controller Page menjadi seperti berikut:
![image](https://user-images.githubusercontent.com/101814131/175824243-4fa49476-baf0-47fd-974f-9958407cc922.png)


Kemudian lakukan refresh pada halaman tersebut.
![image](https://user-images.githubusercontent.com/101814131/176965831-36b11b2b-7ae9-4592-a48c-b64b528d54a4.png)





11.Membuat Layout Web dengan CSS Pada dasarnya layout web dengan css dapat diimplamentasikan dengan mudah pada codeigniter. Yang perlu diketahui adalah, pada Codeigniter 4 file yang menyimpan asset css dan javascript terletak pada direktori public. Buat file css pada direktori public dengan nama style.css (copy file dari praktikum lab4_layout. Kita akan gunakan layout yang pernah dibuat pada praktikum 4.
![image](https://user-images.githubusercontent.com/101814131/175824258-1b16ee88-2516-47c8-8a88-62c6f4b29889.png)


Kemudian buat folder template pada direktori view kemudian buat file header.php dan footer.php

File app/view/template/header.php
![image](https://user-images.githubusercontent.com/101814131/175824275-1aa15f23-e53f-487b-9d24-95dbb5a72495.png)


File app/view/template/footer.php
![image](https://user-images.githubusercontent.com/101814131/175824291-fdab4b66-1d6b-4820-afd8-748d88afbf6d.png)


File app/view/template/about.php
![image](https://user-images.githubusercontent.com/101814131/175824301-a1541ef7-8b9e-429e-bb2b-12dfd2fce14d.png)


Selanjutnya refresh tampilan pada alamat http://localhost:8080/about
![image](https://user-images.githubusercontent.com/101814131/176965941-3fae695b-15a8-43ea-a45b-f0458327a750.png)


PERTEMUAN 13
Membuat Database
![image](https://user-images.githubusercontent.com/101814131/175824311-c66265dc-a193-4eaa-a8c4-591c21fb0fab.png)


Membuat Tabel
![image](https://user-images.githubusercontent.com/101814131/175824331-ec5e4126-c24a-4b01-b121-ac4fbff70ed8.png)

Konfigurasi koneksi 
database Selanjutnya membuat konfigurasi untuk menghubungkan dengan database server. Konfigurasi dapat dilakukan dengan du acara, yaitu pada file app/config/database.php atau menggunakan file .env. Pada praktikum ini kita gunakan konfigurasi pada file .env
![image](https://user-images.githubusercontent.com/101814131/175824631-8e743c30-4ab9-4dab-b374-03b2141aa93d.png)

Membuat Model!

Selanjutnya adalah membuat Model untuk memproses data Artikel. Buat file baru pada direktori app/Models dengan nama ArtikelModel.php

![image](https://user-images.githubusercontent.com/101814131/175824699-ce7eaf2c-7c43-43ff-8ea0-e862e24859c1.png)


Membuat Controller

Buat Controller baru dengan nama Artikel.php pada direktori app/Controllers.
![image](https://user-images.githubusercontent.com/101814131/175824704-4d88dffb-a7a4-4e39-b814-46309fa6447d.png)


Membuat View

Buat direktori baru dengan nama artikel pada direktori app/views, kemudian buat file baru dengan nama index.php.
![image](https://user-images.githubusercontent.com/101814131/175824709-1a0c11fe-4dcf-4386-aaa3-6ce6dd626b03.png)


• Selanjutnya buka browser kembali, dengan mengakses url http://localhost:8080/artikel

![image](https://user-images.githubusercontent.com/101814131/175824729-61d33215-f93c-4026-8886-ed6b18c5abfd.png)


Membuat Menu Admin

Menu admin adalah untuk proses CRUD data artikel. Buat method baru pada Controller Artikel dengan nama admin_index().
![image](https://user-images.githubusercontent.com/101814131/175824827-8ea6bb14-5be9-4f2f-9728-664b29b5b0f0.png)


Selanjutnya buat view untuk tampilan admin dengan nama admin_index.php
![image](https://user-images.githubusercontent.com/101814131/175824844-c44de0a8-80ea-4c11-af22-81d9bd91bed4.png)
![image](https://user-images.githubusercontent.com/101814131/175824851-246c2527-171f-4e6e-b2b3-332d1724e9e9.png)


Tambahkan routing untuk menu admin seperti berikut:
![image](https://user-images.githubusercontent.com/101814131/175824862-e4e5e459-cfbb-4bdc-a7b3-53e6207d6be0.png)


Akses menu admin dengan url http://localhost:8080/admin/artikel
![image](https://user-images.githubusercontent.com/101814131/175824873-e491fd02-1e3b-4f35-8d8d-23efbf54cdd6.png)


Menambah Data Artikel

Tambahkan fungsi/method baru pada Controller Artikel dengan nama add().

![image](https://user-images.githubusercontent.com/101814131/175824885-a17eb5c2-e295-421d-a5e5-56c902573d15.png)


Mengubah Data

Tambahkan fungsi/method baru pada Controller Artikel dengan nama edit().
![image](https://user-images.githubusercontent.com/101814131/175824905-45ca8fad-201a-4d4b-b892-dd8f6c8f2420.png)
![image](https://user-images.githubusercontent.com/101814131/175824911-704b62a4-58dd-4365-9656-fd1f4e70acf3.png)


Menghapus Data
Tambahkan fungsi/method baru pada Controller Artikel dengan nama delete()
![image](https://user-images.githubusercontent.com/101814131/175824923-36594d61-0d53-4830-89c7-77d47893f160.png)


PERTEMUAN 14

Membuat tabel user untuk login pada database lab_ci4
![11](https://user-images.githubusercontent.com/101814131/175825458-acef27b7-b8ff-4214-9aed-25aff3996220.png)


Membuat Model User, selanjutnya adalah membuat Model untuk memproses data Login. Buat file baru pada direktori app/Models dengan nama UserModel.php
![image](https://user-images.githubusercontent.com/101814131/175825468-b71a70f0-758d-476d-85fc-efe3eace386a.png)


Membuat Controller User. Buat Controller baru dengan nama User.php pada direktori app/Controllers kemudian tambahkan method index() untuk menampilkan daftar user, dan method login() untuk proses login.
![image](https://user-images.githubusercontent.com/101814131/175825478-7fe13a54-efb6-42f0-b893-a6be51a2341b.png)
![image](https://user-images.githubusercontent.com/101814131/175825482-b2b91f9b-19c9-460c-9ae4-f9c3761cda18.png)


Membuat View Login, buat direktori baru dengan nama user pada direktori app/views, kemudian buat file baru dengan nama login.php.
![image](https://user-images.githubusercontent.com/101814131/175825486-26c48490-e203-4eef-8a58-8093ab54a3b7.png)
![image](https://user-images.githubusercontent.com/101814131/175825493-98d4781d-0c2c-4be5-ab39-e1aefd6ddfc3.png)


Membuat Database Seeder. Database seeder digunakan untuk membuat data dummy. Untuk keperluan ujicoba modul login, kita perlu memasukkan data user dan password kedaalam database. Untuk itu buat database seeder untuk tabel user. Buka CLI, kemudian tulis perintah berikut:
![image](https://user-images.githubusercontent.com/101814131/175825514-99444e29-f8e2-448c-a2c6-072fa9064532.png)


Selanjutnya, buka file UserSeeder.php yang berada di lokasi direktori /app/Database/Seeds/UserSeeder.php kemudian isi dengan kode berikut:

![image](https://user-images.githubusercontent.com/101814131/175825524-621b2de9-f174-458b-9947-01b10e86010a.png)


Selanjutnya buka kembali CLI dan ketik perintah berikut:
![image](https://user-images.githubusercontent.com/101814131/175825532-4ee276f3-f228-4d6a-be8c-bc9d97b14f07.png)


Uji Coba Login Selanjutnya buka url http://localhost:8080/user/login seperti berikut:
![image](https://user-images.githubusercontent.com/101814131/176966080-b60e1a86-5546-4e67-91a8-fe387674d596.png)



Menambahkan Auth Filter, selanjutnya membuat filer untuk halaman admin. Buat file baru dengan nama Auth.php pada direktori app/Filters.
![image](https://user-images.githubusercontent.com/101814131/175825545-b740cb9c-d3c6-4463-a39e-4fe44f171935.png)


Selanjutnya buka file app/Config/Filters.php tambahkan kode berikut:
![image](https://user-images.githubusercontent.com/101814131/175825552-2ebaddba-4ac7-4c59-9d0f-f80ba2d67063.png)


Selanjutnya buka file app/Config/Routes.php dan sesuaikan kodenya.
![image](https://user-images.githubusercontent.com/101814131/175825561-23b5be40-8fbb-4ef6-a45c-b38c554db300.png)


Percobaan Akses Menu Admin, buka url dengan alamat http://localhost:8080/admin/artikel ketika alamat tersebut diakses maka, akan dimuculkan halaman login.
![image](https://user-images.githubusercontent.com/101814131/176966150-ac7bd588-d2e6-4f0b-b628-236c58c7d365.png)



Fungsi Logout, tambahkan method logout pada Controller User seperti berikut:
![image](https://user-images.githubusercontent.com/101814131/175825573-6cd3a8c6-0c4e-4366-911f-d4b19d40483d.png)


Kemudian tambahkan navbar pada admin_header seperti berikut:
![image](https://user-images.githubusercontent.com/101814131/175825578-fd43f9f0-18eb-40f5-9f07-5b1922d7bafc.png)


Ketika kita klik navbar maka akan langsunh mengarah pada halaman login.

![image](https://user-images.githubusercontent.com/101814131/176966217-680ffc03-f250-42ff-b505-b992570529ea.png)


pertemuan ke 15

Untuk membuat pagination, buka Kembali Controller Artikel, kemudian modifikasi kode pada method admin_index seperti berikut.
![image](https://user-images.githubusercontent.com/101814131/176913156-436f33e0-fa68-4aea-8926-bc07d755c469.png)



Kemudian buka file views/artikel/admin_index.php dan tambahkan kode berikut dibawah deklarasi tabel data.
![image](https://user-images.githubusercontent.com/101814131/176913363-d64b2619-81eb-4e5e-a2a5-c8112a91ca50.png)


Selanjutnya buka kembali menu daftar artikel, tambahkan data lagi untuk melihat hasilnya.
![image](https://user-images.githubusercontent.com/101814131/176966267-e4aeee96-08cb-4616-81ad-894bc4cbfce8.png)



4.Membuat Pencarian, pencarian data digunakan untuk memfilter data. Untuk membuat pencarian data, buka kembali Controller Artikel, pada method admin_index ubah kodenya seperti berikut:

![image](https://user-images.githubusercontent.com/101814131/176913654-720c067c-32f0-4556-ae16-9f918dc8d517.png)


Kemudian buka kembali file views/artikel/admin_index.php dan tambahkan form pencarian sebelum deklarasi tabel seperti berikut:
![image](https://user-images.githubusercontent.com/101814131/176913703-66495c8d-b593-48af-8105-afcc50a28edf.png)


Dan pada link pager ubah seperti berikut.
![image](https://user-images.githubusercontent.com/101814131/176913727-8913d3c6-fbc9-45c9-8109-5da58e2554f7.png)


Selanjutnya ujicoba dengan membuka kembali halaman admin artikel, masukkan kata kunci tertentu pada form pencarian.

![image](https://user-images.githubusercontent.com/101814131/176966349-84207999-9742-4f03-8eea-23caf0376ec5.png)


Upload Gambar, menambahkan fungsi unggah gambar pada tambah artikel. Buka kembali Controller Artikel, sesuaikan kode pada method add seperti berikut:
![image](https://user-images.githubusercontent.com/101814131/176913859-bcb4ed0f-6b13-4898-83b2-29a65491d956.png)


Kemudian pada file views/artikel/form_add.php tambahkan field input file seperti berikut.
![image](https://user-images.githubusercontent.com/101814131/176913905-212f02da-52e5-42aa-8473-36575f5e74e0.png)


Dan sesuaikan tag form dengan menambahkan ecrypt type seperti berikut.
![image](https://user-images.githubusercontent.com/101814131/176913984-6443a0cd-54ed-4482-a8ba-ff61cc57c20d.png)


Ujicoba file upload dengan mengakses menu tambah artikel.
![image](https://user-images.githubusercontent.com/101814131/176966440-2d6f58f9-23cd-4ea1-b955-68af455b97f7.png)




