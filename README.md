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

# Source Code
1. Database
2. Entity
   - Karyawan
     ![image](https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/126893861/9a5f811b-f9ba-4526-b1ed-d88bd42faf4c)
     
     public class Karyawan  Ini adalah deklarasi kelas Karyawan. Semua program yang terkait karyawan akan ditempatkan di dalam kelas ini. String idKaryawan, EmployeeName;: Deklarasi atribut kelas (variabel anggota). idKaryawan dan namaKaryawan merupakan dua atribut yang digunakan untuk menyimpan informasi tentang  karyawan. Ini adalah tipe data String, artinya dapat menyimpan teks. static ArrayList<Karyawan> arrayKaryawan = new ArrayList<>(); Ini adalah deklarasi atribut statis. arrayKaryawan adalah variabel  bertipe ArrayList dan  digunakan untuk menyimpan daftar objek karyawan. Atribut static berarti  salinan variabel ini  digunakan oleh semua objek  kelas Karyawan. Artinya, semua objek karyawan mempunyai akses ke daftar karyawan yang sama. public Karyawan(String idKaryawan, String namaKaryawan)  Ini adalah konstruktor untuk kelas Karyawan. Konstruktor digunakan untuk membuat objek karyawan. Konstruktor ini menerima dua parameter, yaitu  idKaryawan dan namaKaryawan, yang  digunakan untuk menginisialisasi atribut karyawan  terkait. public String getIdKaryawan() Ini adalah metode yang digunakan untuk mengambil nilai atribut idKaryawan dari objek karyawan. public String getNamaKaryawan() Ini adalah metode yang digunakan untuk mengambil nilai atribut namaKaryawan dari objek karyawan.

     ![image](https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/126893861/ca11781e-160f-4463-aeb7-81ab7fe64005)
     
     public static void insertKaryawan(String id, String nama) throws SQLException Metode ini digunakan untuk memasukkan data karyawan baru ke dalam database. Parameter id dan nama digunakan untuk menginisialisasi objek Karyawan. Baris pertama membuat objek Karyawan baru dengan nilai ID dan nama yang ditentukan. Objek Karyawan baru ini kemudian ditambahkan ke array ArrayList arrayKaryawan, yang berisi daftar objek Karyawan. query SQL INSERT  dibuat menggunakan String format. Query ini menyisipkan data karyawan baru ke dalam tabel karyawan dengan mengambil nilai idKaryawan dan namaKaryawan dari objek karyawanBaru. Terakhir, gunakan metode executeUpdateQuery dari objek database  untuk menjalankan kueri SQL. public static ArrayList<Karyawan> readKaryawan() throws SQLException. Metode ini  membaca data karyawan dari database dan menyimpannya ke ArrayListKaryawan.  Pertama, arrayKaryawan.clear() menghapus isi array Karyawan sehingga daftar yang ada diganti dengan data yang baru dibaca. Selanjutnya, gunakan query SQL SELECT  untuk mengambil semua data dari tabel Karyawan. Hasil  query SQL dieksekusi  dari objek DB  menggunakan executeSelectQuery dan disimpan dalam objek ResultSet RS. Program kemudian mengeksekusi loop (while (rs.next())) untuk membaca baris dari hasil kueri. Setiap baris data, yaitu ID dan nama, diambil dari hasil query. Objek Karyawan baru kemudian dibuat menggunakan data ini dan ditambahkan ke arrayKaryawan ArrayList. Terakhir, metode ini mengembalikan arrayKaryawan yang  diisi dengan data karyawan dari database.
     
   - Pelanggan
  ![image](https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/126893861/ec5b52cc-038b-459c-8320-599542687cd5)

public class Pelanggan  Ini adalah deklarasi kelas Pelanggan. Semua program terkait pelanggan akan ditempatkan di  kelas ini. String idPelanggan, nama_pelanggan; Deklarasi atribut kelas. idPelanggan dan nama_pelanggan adalah dua atribut yang digunakan untuk menyimpan informasi tentang  pelanggan. Ini adalah tipe data String, artinya dapat menyimpan teks. static database.Database db = new database.Database(); Ini adalah deklarasi atribut statis. db adalah variabel bertipe database.Database yang dapat digunakan untuk mengelola koneksi database dan berinteraksi dengan database. Atribut statis berarti  salinan variabel ini  digunakan oleh semua objek  kelas Pelanggan. Dengan kata lain, semua objek pelanggan dapat mengakses objek database yang sama.  public Pelanggan(String idPelanggan, String nama_pelanggan)  Ini adalah konstruktor untuk kelas Pelanggan. Konstruktor digunakan untuk membuat objek pelanggan. Konstruktor ini menerima dua parameter yaitu  idPelanggan dan nama_pelanggan digunakan untuk menginisialisasi atribut pelanggan sesuai. public String getIdPelanggan() Ini adalah metode yang digunakan untuk mengambil nilai atribut idPelanggan dari objek pelanggan. public void setIdPelanggan(String idPelanggan) Ini adalah metode yang digunakan untuk menetapkan nilai atribut idPelanggan dari objek pelanggan. public String getNama_pelanggan() Ini adalah metode yang digunakan untuk mengambil nilai atribut nama_pelanggan dari objek pelanggan.  public void setNama_pelanggan(String nama_pelanggan) Ini adalah metode yang digunakan untuk menetapkan nilai atribut nama_pelanggan dari objek pelanggan. public static void createPelanggan(String id, String nama) throws SQLException. Cara ini digunakan untuk membuat pelanggan baru dan memasukkan data pelanggan ke dalam database. Pertama, objek Pelanggan baru dibuat dengan ID dan nama yang ditentukan. query SQL INSERT kemudian dibuat menggunakan String.format. Query ini menyisipkan data pelanggan baru ke dalam tabel pelanggan dengan mengambil nilai idPelanggan dan nama_pelanggan  dari objek newPelanggan.  Terakhir, gunakan metode executeUpdateQuery dari objek database  untuk menjalankan kueri SQL.

   - Transaksi
![image](https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/126893861/2e7a9785-9191-41a8-b123-36caa658d566)

![image](https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/126893861/5fa11d83-b057-4794-9106-d5afed6fc28d)

Kelas Transaksi mendeklarasikan beberapa variabel anggota. String idTransaksi Menyimpan ID transaksi. String idKaryawan Menyimpan ID karyawan yang terlibat dalam transaksi. String idPelanggan Menyimpan ID pelanggan yang terlibat dalam transaksi.  string idBarang Menyimpan ID item yang terlibat dalam transaksi.  String tanggal Menyimpan tanggal transaksi. Ada variabel database statis  yang digunakan untuk mengakses objek  kelas Database.Database untuk  melakukan operasi lain yang terkait dengan penyimpanan data transaksi. Terdapat konstruktor yang menerima beberapa argument yaitu String idTransaksi,  String idKaryawan,  String idPelanggan, String idBarang, String tanggal Konstruktor ini digunakan untuk menginisialisasi objek Transaksi dengan nilai-nilai yang diinputkan oleh karyawa atau user. Metode getTanggal(), getIdTransaksi(), getIdKaryawan(), getIdPelanggan(), getIdBarang() Metod  instance ini yang digunakan untuk mengambil nilai variabel anggota seperti tanggal, idTransaksi, idKaryawan, idPelanggan, dan idBarang. Metode ini mengembalikan nilai yang disimpan ketika dipanggil. Metode insertTransaksi(String idTransaksi, String idKaryawan, String idPelanggan, String idBarang, String tanggal. Metod insertTransaksi(String idTransaksi, String idKaryawan, String idPelanggan, String idBarang, String tanggal) Metode ini merupakan metode statis yang memasukkan data transaksional ke dalam database. Ketika metode ini dipanggil,  objek kelas Transaksi baru dibuat dengan argumen yang ditentukan. Metode ini kemudian membuat string qq yang berisi deklarasi SQL untuk memasukkan data transaksi ke dalam tabel transaksi. deklarasi SQL ini menggunakan nilai yang diperoleh dari objek newTransaction yang  dibuat. Terakhir, metode ini menggunakan objek database yang dapat berupa objek  kelas database.Database untuk mengeksekusi deklarasi SQL dengan memanggil metode eksekusiUpdateQuery(qq). Metode ini terhubung ke database dan menjalankan perintah SQL yang memasukkan data transaksional. 

   - Barang
![image](https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/126893861/90d3ef0e-d700-4a79-9fe5-ed15b68f8551)
![image](https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/126893861/c7dd644d-f371-44c7-8980-c845b0403408)
![image](https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/126893861/2aa51a5f-2d40-408c-a473-9f58c37383c3)

Pada program ini menggunakan Getter yaitu getIdBarang(), getNamaBarang(), dan getHargaBarang() digunakan untuk mengambil nilai dari variabel anggota terkait (idBarang, namaBarang, dan HargaBarang) dan menggunakan setter  seperti setIdBarang(), setNamaBarang(), dan setHargaBarang() untuk mengatur nilai variabel anggotanya.  Kemudian Metod readBarang() Metode ini  membaca data item dari database dan mengembalikannya sebagai ArrayList.  Kode dalam metode ini membersihkan ArrayList dari arrayBarang dan menjalankan deklarasi SQL untuk mengambil data item dari tabel barang di database.  Loop hasil query, buat objek "Barang" untuk setiap baris data, dan tambahkan ke ArrayList arrayBarang. Setelah  membaca data, ArrayList dikembalikan. Kemudian Metode createBarang() berfungsi untuk membuat data barang baru dan menyimpannya ke database,  Membuat objek Barang baru dengan nilai yang ditentukan,  Menambahkan objek  Barang ke ArrayList arrayBarang, untuk membuat deklarasi SQL untuk menyisipkan data barang baru ke dalam tabel barang di database. Dan menJalankan deklarasi SQL untuk menyimpan data barang baru. Kemudian metode deleteBarang() Metode ini digunakan untuk menghapus data item dari ArrayList dan database berdasarkan ID, Loop arrayBarang ArrayList dan cari objek Barang dengan ID yang sesuai  Jika ID ditemukan, objek Barang dihapus dari ArrayList dan deklarasi SQL dijalankan untuk menghapus data barang dari tabel barang di database. Kemudian metode updateBarang()  Metode ini digunakan untuk memperbarui data barang berdasarkan ID dari ArrayList dan di basis data. Loop melalui ArrayList arrayBarang, mencari objek Barang dengan ID yang sesuai. Jika ID ditemukan, objek Barang diperbarui dengan nilai baru untuk nama dan harga barang. Kemudian, deklarasi SQL dijalankan untuk memperbarui data barang dalam tabel "barang" di basis data.

   - Makanan
   ![image](https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/126893861/f7a4b3f7-a0ed-4b2e-8a3a-036834ed8f19)

Pada program ini terdapat Metode readMakanan() Metode ini  membaca data makanan dari database dan mengembalikannya dalam bentuk ArrayList.  metode ini menghapus arrayMakanan  ArrayList  untuk membersihkan data apa pun yang mungkin ada sebelumnya. Metode ini kemudian mengeksekusi deklarasi SQL yang menggabungkan tabel Barang dan Makanan menggunakan INNER JOIN. Hasilnya mewarisi kolom dari kedua tabel. Loop hasil kueri membaca setiap baris data yang mencakup ID barang, nama barang, harga barang, tanggal kadaluarsa, dan asal produk.  Objek Makanan baru dibuat untuk setiap baris data dan  ditambahkan ke arrayMakanan. Setelah  membaca data, ArrayList  dikembalikan. Kemudian metode createMakanan()  Metode ini membuat  data makanan baru dan menyimpannya ke database.  Membuat objek makanan baru dengan nilai tertentu, seperti tanggal kedaluwarsa dan asal produk.  Objek Makanan baru ditambahkan ke ArrayList arrayMakanan. dan untuk memasukkan data makanan baru ke dalam tabel Makanan di database  Jalankan deklarasi SQL untuk menyimpan data makanan baru. 

![image](https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/126893861/017390bc-ffb2-4d28-baaa-d547c024d573)

Pada program ini terdapat metode deleteMakanan(String idBarang)  Metode ini digunakan untuk menghapus data makanan berdasarkan ID barang dari arrayListMakanan dan database.  Loop ArrayList ArrayMakanan dan cari objek Makanan dengan ID barang yang sesuai.  Jika ID barang ditemukan, objek Makanan akan dihapus dari arrayListMakanan.  Metode ini kemudian membuat deklarasi SQL yang menghapus data makanan dengan ID barang  dari tabel Makanan di database. Deklarasi SQL dijalankan untuk menghapus data makanan dari database. Kemudian ada metode updateMakanan(String idBarang, String tanggal, String asal) Metode ini digunakan untuk mengupdate data makanan berdasarkan array ArrayListMakanan dan ID barang di database.  Loop ArrayList arrayMakanan dan cari objek Makanan dengan ID barang yang sesuai.  Jika ID barang ditemukan, metode ini memperbarui nilai atribut tanggal kadaluarsa dan asal produk  dalam objek Makanan. Metode ini kemudian membuat deklarasi SQL yang memperbarui data makanan di tabel Makanan di database. Deklarasi SQL ini memperbarui tanggal kedaluwarsa produk dan asal  berdasarkan nilai  baru pada objek Makanan. 
     
   - NonMakanan
![image](https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/126893861/4d6fc7ae-1621-47fb-ad0f-5731e34cb4ee)

Pada program ini terdapat metode readNonMakanan Metode ini  membaca data non-makanan dari database dan mengembalikannya dalam bentuk ArrayList. metode ini menghapus arrayNonMakanan ArrayList  untuk membersihkan data apa pun yang mungkin ada sebelumnya. Metode ini kemudian mengeksekusi pernyataan SQL yang menggabungkan tabel barang dan non_makanan menggunakan INNER JOIN. Hasilnya mewarisi kolom dari kedua tabel. Loop  hasil kueri membaca setiap baris data yang mencakup ID barang, nama barang, harga barang, berat barang, dan ukuran barang. Untuk setiap baris data, objek NonMakanan baru dibuat dan  ditambahkan ke Daftar Array NonMakanan. Setelah itu data di baca ArrayList  dan  dikembalikan. Kemudian ada juga metode createNonMakanan() Metode ini  membuat  data non-makanan baru dan menyimpannya di database.  Membuat objek NonMakanan baru dengan nilai tertentu seperti berat barang dan ukuran barang .  Objek NonMakanan baru ditambahkan ke ArrayList arrayNonMakanan, Dengan demikian, kelas ini memungkinkan untuk melakukan operasi CRUD pada data non-makanan

     
3. View
   - Login
   - Register
   - Menu Karyawan
   - Menu Barang
   - Input Pelanggan
   - Transaksi
   - Struk
     
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
