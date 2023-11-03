# Capstone-Project-Kelompok-5
1. Nama: Achmad Roffi Thoriq
   NIM : 2209116052
2. Nama: Nur Shafa Azizah
   NIM : 2209116057
# Toko Sembako
Dalam laporan proyek akhir mata kuliah pemrograman berorientasi objek kelompok kami mengangkat tema yaitu pengembangan aplikasi manajemen Toko Sembako. Proyek ini adalah tugas penting dalam perjalanan kami di semester 3. Proyek ini akan memberikan wawasan tentang tujuan proyek, langkah-langkah yang telah diambil, hasil yang dicapai, serta pemaparan detail tentang aplikasi yang telah kami rancang.

Tujuan dari proyek ini adalah untuk mengembangkan sebuah aplikasi manajemen yang akan membantu pemilik toko sembako dalam mengelola operasional sehari-hari mereka. Toko sembako adalah bisnis penting dalam masyarakat yang menyediakan kebutuhan pokok sehari-hari. Oleh karena itu, kami berupaya untuk menciptakan alat yang akan mempermudah pemilik toko dalam mencatat transaksi, mengelola data karyawan, pelanggan, dan barang. Proyek ini akan menjelaskan struktur hierarki kelas dalam aplikasi, serta memberikan gambaran singkat tentang alur kerja aplikasi dan bagaimana kami mengimplementasikan fitur-fitur seperti login, manajemen data, dan antarmuka pengguna (GUI) yang mudah digunakan.

Selama perjalanan proyek ini, kami telah menghadapi tantangan dan belajar banyak. Kami telah berusaha untuk mengaplikasikan pengetahuan kami ke dalam proyek yang bermanfaat ini. Kami berharap bahwa proyek ini akan memberikan gambaran yang jelas tentang konsep, desain, dan hasil yang telah kami capai dalam pengembangan aplikasi manajemen Toko Sembako. Terima kasih kepada semua pihak yang telah mendukung dan memberikan inspirasi selama proyek ini. Kami harap aplikasi ini akan membantu pemilik toko sembako dalam menjalankan bisnis mereka dengan lebih efisien dan memberikan layanan yang lebih baik kepada pelanggan.

# Flowchart
![Capstone](https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/127502125/86495276-1d81-4873-844f-d43041cc548b)


# Hirarki Kelas
![hirarki](https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/127502125/2fd44619-193d-4370-be45-09b993b05ac6)

Dalam hierarki kelas di atas, "Barang" adalah kelas utama yang memiliki dua subkelas, yaitu "Makanan" dan "Non-Makanan". Dengan memakai konsep inheritance (pewarisan) memungkinkan "Makanan" dan "Non-Makanan" untuk mewarisi atribut yang dimiliki oleh kelas "Barang" tanpa perlu mendefinisikannya ulang. Dengan kata lain, atribut dan metode yang terdefinisi di kelas "Barang" dapat digunakan oleh kedua subkelas tersebut, yang membuat kode menjadi lebih efisien dan mudah dikelola. Inheritance adalah salah satu prinsip fundamental dalam pemrograman berorientasi objek yang memungkinkan penggunaan kembali kode dan membantu dalam menciptakan hierarki kelas yang terstruktur.

<img width="190" alt="image" src="https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/127502125/b81126d2-8cd2-45da-969c-c2533cef2014">

Kelas-kelas yang ada pada program

# Penjelasan Codingan

1. Kelas Karyawan
   
![image](https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/126893861/9a5f811b-f9ba-4526-b1ed-d88bd42faf4c)

Kelas "Karyawan" adalah tempat semua informasi terkait karyawan disimpan. Dalam kelas ini, terdapat dua atribut (variabel anggota), yaitu "idKaryawan" dan "namaKaryawan," yang digunakan untuk menyimpan data karyawan. Kedua atribut ini berjenis String, sehingga dapat menyimpan teks. Terdapat juga atribut statis bernama "arrayKaryawan" yang berjenis ArrayList. Atribut ini digunakan untuk menyimpan daftar objek karyawan. Atribut statis berarti bahwa semua objek kelas Karyawan menggunakan salinan yang sama dari "arrayKaryawan," sehingga semua objek dapat mengakses daftar karyawan yang sama. Terdapat konstruktor dalam kelas ini, yaitu "Karyawan," yang digunakan untuk membuat objek karyawan. Konstruktor ini menerima dua parameter, yaitu "idKaryawan" dan "namaKaryawan," yang digunakan untuk menginisialisasi atribut karyawan terkait.

Kelas ini juga memiliki dua metode:
1. "getIdKaryawan()" digunakan untuk mendapatkan nilai dari atribut "idKaryawan" dari objek karyawan.
2. "getNamaKaryawan()" digunakan untuk mendapatkan nilai dari atribut "namaKaryawan" dari objek karyawan.

![image](https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/126893861/ca11781e-160f-4463-aeb7-81ab7fe64005)

Metode "insertKaryawan" digunakan untuk memasukkan data karyawan baru ke dalam database. Parameter "id" dan "nama" digunakan untuk menginisialisasi objek Karyawan baru. Pertama, objek Karyawan baru dibuat dengan nilai ID dan nama yang diberikan, lalu ditambahkan ke ArrayList "arrayKaryawan." Selanjutnya, dibuat query SQL INSERT yang menyisipkan data karyawan baru ke dalam tabel "karyawan" dengan menggunakan nilai "idKaryawan" dan "namaKaryawan" dari objek karyawanBaru. Terakhir, query SQL dieksekusi dengan metode "executeUpdateQuery" dari objek database.

Metode "readKaryawan" digunakan untuk membaca data karyawan dari database dan menyimpannya dalam ArrayList "arrayKaryawan." Pertama, isi "arrayKaryawan" dibersihkan dengan "arrayKaryawan.clear()" agar dapat diganti dengan data yang baru dibaca. Kemudian, query SQL SELECT digunakan untuk mengambil semua data dari tabel "karyawan." Hasil query dieksekusi dari objek "DB" dan disimpan dalam objek ResultSet "RS." Program kemudian membaca baris hasil query satu per satu dengan loop "while (rs.next())." Setiap baris data, yaitu ID dan nama, diambil dari hasil query. Objek Karyawan baru dibuat dengan data ini dan ditambahkan ke ArrayList "arrayKaryawan." Terakhir, metode ini mengembalikan "arrayKaryawan" yang berisi data karyawan dari database.

2. Kelas Pelanggan

![image](https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/126893861/ec5b52cc-038b-459c-8320-599542687cd5)

Kelas "Pelanggan" adalah tempat untuk menyimpan informasi terkait pelanggan. Dalam kelas ini, terdapat dua atribut, yaitu "idPelanggan" dan "nama_pelanggan," yang digunakan untuk menyimpan data pelanggan. Kedua atribut ini berjenis String, sehingga dapat menyimpan teks.Terdapat juga atribut statis "db," yang adalah objek dari kelas "Database." Atribut ini digunakan untuk mengelola koneksi ke database dan berinteraksi dengan database. Atribut statis berarti bahwa semua objek kelas "Pelanggan" menggunakan salinan yang sama dari objek "db," sehingga semua objek dapat mengakses database yang sama. Kelas ini memiliki konstruktor "Pelanggan" yang digunakan untuk membuat objek pelanggan. Konstruktor ini menerima dua parameterr, yaitu "idPelanggan" dan "nama_pelanggan," yang digunakan untuk menginisialisasi atribut pelanggan sesuai dengan nilai yang diberikan.

3. Kelas Transaksi
     
![image](https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/126893861/2e7a9785-9191-41a8-b123-36caa658d566)

![image](https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/126893861/5fa11d83-b057-4794-9106-d5afed6fc28d)

Kelas "Transaksi" digunakan untuk menyimpan informasi tentang transaksi. Ini mencakup ID transaksi, ID karyawan terlibat, ID pelanggan terlibat, ID barang terlibat, dan tanggal transaksi. Kelas ini memiliki variabel anggota dan metode yang memungkinkan akses dan penyimpanan data transaksi. Adaa metode "insertTransaksi" yang memungkinkan penggunaan data transaksi untuk dimasukkan ke dalam database. Ini melibatkan pembuatan objek "Transaksi" dengan data yang diberikan, membuat pernyataan SQL untuk menyimpan data ini, dan menjalankannya menggunakan objek database. Keseluruhan, kelas "Transaksi" memfasilitasi manajemen data transaksi dan interaksi dengan database.

4. Kelas Barang
   
![image](https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/126893861/90d3ef0e-d700-4a79-9fe5-ed15b68f8551)

![image](https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/126893861/c7dd644d-f371-44c7-8980-c845b0403408)

![image](https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/126893861/2aa51a5f-2d40-408c-a473-9f58c37383c3)

Program ini menggunakan Getter dan Setter untuk mengakses dan mengubah nilai variabel anggota seperti idBarang, namaBarang, dan HargaBarang. Ini memungkinkan manajemen data barang dengan lebih mudah.

Metode "readBarang" digunakan untuk membaca data barang dari database dan mengembalikannya sebagai ArrayList. Metode ini membersihkan ArrayList yang ada, menjalankan query SQL untuk mengambil data barang dari database, dan kemudian membuat objek "Barang" untuk setiap baris hasil query. Objek-objek ini ditambahkan ke ArrayList "arrayBarang," dan hasilnya dikembalikan.

Metode "createBarang" digunakan untuk membuat data barang baru dan menyimpannya ke dalam database. Ini melibatkan pembuatan objek Barang baru dengan nilai yang diberikan, menambahkannya ke ArrayList "arrayBarang," dan menjalankan query SQL untuk menyimpan data barang baru.

Metode "deleteBarang" digunakan untuk menghapus data barang dari ArrayList dan database berdasarkan ID. Program loop melalui ArrayList "arrayBarang," mencari objek Barang dengan ID yang sesuai, menghapus objek tersebut dari ArrayList, dan menjalankan query SQL untuk menghapus data barang dari database.

Metode "updateBarang" digunakan untuk memperbarui data barang berdasarkan ID dalam ArrayList dan database. Program loop melalui ArrayList "arrayBarang," mencari objek Barang dengan ID yang sesuai, memperbarui nilai nama dan harga barang, dan menjalankan query SQL untuk memperbarui data barang dalam database. Semua ini memudahkan manajemen data barang.

5. Kelas Makanan

![image](https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/126893861/f7a4b3f7-a0ed-4b2e-8a3a-036834ed8f19)

Metode "readMakanan" membaca data makanan dari database dan mengembalikannya sebagai ArrayList. Metode membersihkan ArrayList "arrayMakanan," menjalankan query SQL dengan INNER JOIN antara tabel "Barang" dan "Makanan" untuk menggabungkan data, lalu membuat objek "Makanan" untuk setiap baris hasil query dan menambahkannya ke "arrayMakanan." Hasilnya adalah ArrayList yang berisi data makanan yang kemudian dikembalikan.

Metode "createMakanan" digunakan untuk membuat data makanan baru dan menyimpannya ke database. Ini melibatkan pembuatan objek "Makanan" baru dengan nilai tertentu, menambahkannya ke ArrayList "arrayMakanan," dan menjalankan query SQL untuk menyimpan data makanan baru ke dalam tabel "Makanan" di database. Dengan demikian, data makanan baru dapat dengan mudah ditambahkan dan dimanajemen dalam program ini.

![image](https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/126893861/017390bc-ffb2-4d28-baaa-d547c024d573)

Metode "deleteMakanan" digunakan untuk menghapus data makanan berdasarkan ID barang dari "arrayMakanan" dan database. Metode mencari objek Makanan dengan ID barang yang sesuai dalam "arrayMakanan," menghapusnya dari "arrayMakanan," dan menjalankan query SQL untuk menghapus data makanan dari tabel "Makanan" di database.

Metode "updateMakanan" digunakan untuk mengupdate data makanan berdasarkan ID barang dalam "arrayMakanan" dan di database. Metode mencari objek Makanan dengan ID barang yang sesuai dalam "arrayMakanan," memperbarui nilai atribut tanggal kadaluarsa dan asal produk, dan menjalankan query SQL untuk memperbarui data makanan di tabel "Makanan" di database berdasarkan nilai baru pada objek Makanan.
     
6. Kelas NonMakanan

![image](https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/126893861/4d6fc7ae-1621-47fb-ad0f-5731e34cb4ee)

Metode "readNonMakanan" digunakan untuk membaca data non-makanan dari database dan mengembalikkannya dalam bentuk ArrayList. Metode membersihkan ArrayList "arrayNonMakanan," menjalankan query SQL dengan INNER JOIN antara tabel "Barang" dan "non_makanan" untuk menggabungkan data, dan membuat objek "NonMakanan" untuk setiap baris hasil query. Objek-objek ini ditambahkan ke ArrayList "arrayNonMakanan," dan hasilnya dikembalikan.

Metode "createNonMakanan" digunakan untuk membuat data non-makanan baru dan menyimpannya ke database. Ini melibatkan pembuatan objek "NonMakanan" baru dengan nilai tertentu, seperti berat barang dan ukuran barang, menambahkannya ke ArrayList "arrayNonMakanan," dan menyimpan data non-makanan baru ke dalam database. Dengan demikian, kelas ini memungkinkan operasi CRUD pada data non-makanan.

     
# Output
1. Menu Login
   
   <img width="392" alt="image" src="https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/127502125/fda489da-704c-4178-b10d-3adad85f8bba">

   Ini adalah tampilan awal aplikasi yang kami buat yaitu menu login untuk karyawan, pada menu ini karyawan dapat login dengan menginputkan nama dan juga id mereka, jika karyawan belum memiliki akun, maka bisa memilih pilihan untuk register terlebih dahulu agar memiliki akun dan dapat login kembali

2. Register

   <img width="392" alt="image" src="https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/127502125/d78c8aa4-39a1-4403-8b44-1444a6abffc0">

   Ini adalah tampilan jika karyawan belum memliki akun, maka karyawan disuruh untuk membuat akun terlebih dahulu dengan menginputkan nama dan id karyawan. Jika sudah maka bisa klik simpan agar data tersimpan dan kemudian login kembali dengan menggunakan akun yang telah dibuat tadi.
   
3. Menu Karyawan

   <img width="392" alt="image" src="https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/127502125/46205676-177b-4f9d-a161-43b786187f73">

   Ini adalah Menu untuk Karyawan jika berhasil login, pada menu karyawan ini memiliki dua fitur yaitu melayani transaksi dan mengelola barang

4. Transaksi (Input Pelanggan)

   <img width="392" alt="image" src="https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/127502125/692a8d32-2b49-41bb-9379-56c43ff94c0b">

   Ini adalah tampilan dari fitur transaksi, dimana sebelum menginputkan transaksi dari pelanggan karyawan disuruh untuk menginput nama dari pelanggan tersebut, dan mengklik tombol selanjutnya untuk dapat menginputkan transaksi

5. Transaksi (Pilih Barang)

   <img width="392" alt="image" src="https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/127502125/d3ead66d-52b7-45df-9347-e3a52aca789e">

   Setelah menginput nama pelanggan karyawan dapat memilih jenis barang yang akan dibeli oleh pelanggan dengan memilih id barang, kemudian klik tombol Masukkan agar transaksi dapat dicetak.

6. Struk Transaksi

   <img width="392" alt="image" src="https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/127502125/0b09295e-a683-4df2-a8fe-3ad295a6aa7c">

   Ini adalah tampilan dari struk transaksi yang dicetak. Menampilkan id transaksi agar karyawan tahu transaksi yang terinput ditoko, kemudian ada id karyawan dimana itu menjelaskan bahwa karyawan tersebut yang melayani transaksi, kemudian akan menampilkan nama dan harga barang yang dibeli oleh pelanggan sesuai dengan id barang yang dipilih sebelumnya.

7. Menu Barang

   <img width="489" alt="image" src="https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/127502125/66783d8a-59e1-4b90-88cf-9113c9fb755f">

   Ini adalah tampilan dari Menu Barang dimana karyawan dapat mengelola barang seperti menambahkan data barang, melihat data barang yang ada di toko, mengedit kebutuhan barang jika sewaktu waktu terdapat perubahan harga ataupun lainnya, dan dapat menghapus data barang apabila toko tidak menjual lagi barang tersebut. 
   
9. Menu Barang (Create)

   <img width="489" alt="image" src="https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/127502125/894fbb9e-ea86-490c-85c9-5247eb257c2a">

   Pada fitur tambah barang, karyawan dapat menambahkan jenis barang baru agar dapat terdata dalam pencatatan toko sembako

10. Menu Barang (Read)

    <img width="489" alt="image" src="https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/127502125/a3cc82e3-dd67-491f-baf7-76c905492b6d">
    
    <img width="489" alt="image" src="https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/127502125/5cbd541d-fa9a-4ba1-9504-85d0d3cd9498">
    
    Pada fitur lihat barang, karyawan dapat melihat barang barang yang tersedia ditoko dan dapat melihat detail dari barang barang tersebut. Pada fitur ini jenis barang dapat dibedakan menjadi dua jenis yaitu Makanan dan Non-Makanan, jadi jika karyawan ingin melihat barang dengan jenis Makanan maka dapat memilih yang Makanan kemudia klik read dan akan menampilkan barang barang yang berjeniskan Makanan, begitupun juga dengan barang yang berjenis Non-Makanan.

11. Menu Barang (Update)

    <img width="489" alt="image" src="https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/127502125/25eb3c1e-0a6a-4066-9c41-425a4a0ec4e0">
    
    Pada fitur update barang, karyawan dapat langsung memilih barang yang ingin diedit detailnya dengan mengklik barang tersebut.

    <img width="254" alt="image" src="https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/127502125/aec0a365-4ef7-4e5f-9ab9-ac419d9b9f8f">
    
    Kemudian karyawan dapat mengedit detail lainnya seperti pada Makanan, karyawan dapat mengisi tanggal kadaluarsa dengan tanggal terbaru karena mungkin saja barang makanan ini adalah stok baru dan harus di edit untuk tanggal kadaluarsanya.

12. Menu Barang (Delete)

    <img width="489" alt="image" src="https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/127502125/f0e26736-05c7-47f6-aaa0-6866af71208a">
    
    Pada fitur delete barang, karyawan dapat langsung memilih barang yang ingin dihapus dengan mengklik barang tersebut lalu pilih delete, maka barang akan langsung terhapus.
