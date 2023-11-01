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
![Flowchart PBO fiks](https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/127502125/673d6bce-ee44-49bd-9a71-1953b7423396)


# Hirarki Kelas
![hirarki](https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/127502125/2fd44619-193d-4370-be45-09b993b05ac6)

Dalam hierarki kelas di atas, "Barang" adalah kelas utama yang memiliki dua subkelas, yaitu "Makanan" dan "Non-Makanan". Dengan memakai konsep inheritance (pewarisan) memungkinkan "Makanan" dan "Non-Makanan" untuk mewarisi atribut yang dimiliki oleh kelas "Barang" tanpa perlu mendefinisikannya ulang. Dengan kata lain, atribut dan metode yang terdefinisi di kelas "Barang" dapat digunakan oleh kedua subkelas tersebut, yang membuat kode menjadi lebih efisien dan mudah dikelola. Inheritance adalah salah satu prinsip fundamental dalam pemrograman berorientasi objek yang memungkinkan penggunaan kembali kode dan membantu dalam menciptakan hierarki kelas yang terstruktur.

# Source Code
1. Database
2. Entity
   - Karyawan
     ![image](https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/126893861/d9374800-45d5-4324-a5b5-140607995f02)
     public class Karyawan  Ini adalah deklarasi kelas Karyawan. Semua program yang terkait karyawan akan ditempatkan di dalam kelas ini. String idKaryawan, EmployeeName;: Deklarasi atribut kelas (variabel anggota). idKaryawan dan namaKaryawan merupakan dua atribut yang digunakan untuk menyimpan informasi tentang  karyawan. Ini adalah tipe data "String", artinya dapat menyimpan teks. static ArrayList<Karyawan> arrayKaryawan = new ArrayList<>();: Ini adalah deklarasi atribut statis. arrayKaryawan adalah variabel  bertipe ArrayList dan  digunakan untuk menyimpan daftar objek karyawan. Atribut static berarti  salinan variabel ini  digunakan oleh semua objek  kelas Karyawan. Artinya, semua objek karyawan mempunyai akses ke daftar karyawan yang sama. public Karyawan(String idKaryawan, String namaKaryawan)  Ini adalah konstruktor untuk kelas Karyawan. Konstruktor digunakan untuk membuat objek karyawan. Konstruktor ini menerima dua parameter, yaitu  idKaryawan dan namaKaryawan, yang  digunakan untuk menginisialisasi atribut karyawan  terkait. public String getIdKaryawan() Ini adalah metode yang digunakan untuk mengambil nilai atribut idKaryawan dari objek karyawan. public String getNamaKaryawan() Ini adalah metode yang digunakan untuk mengambil nilai atribut namaKaryawan dari objek karyawan.

     ![image](https://github.com/shafaaz11/Capstone-Project-Kelompok-5/assets/126893861/e8db294f-471f-4e51-ac31-5e96d66445bf)
     public static void insertKaryawan(String id, String nama) throws SQLException Metode ini digunakan untuk memasukkan data karyawan baru ke dalam database. Parameter id dan nama digunakan untuk menginisialisasi objek Karyawan. Baris pertama membuat objek Karyawan baru dengan nilai ID dan nama yang ditentukan. Objek Karyawan baru ini kemudian ditambahkan ke array ArrayList arrayKaryawan, yang berisi daftar objek Karyawan. query SQL INSERT  dibuat menggunakan String.format. Query ini menyisipkan data karyawan baru ke dalam tabel karyawan dengan mengambil nilai idKaryawan dan namaKaryawan dari objek karyawanBaru. Terakhir, gunakan metode executeUpdateQuery dari objek database  untuk menjalankan kueri SQL. public static ArrayList<Karyawan> readKaryawan() throws SQLException. Metode ini  membaca data karyawan dari database dan menyimpannya ke ArrayListKaryawan.  Pertama, arrayKaryawan.clear() menghapus isi array Karyawan sehingga daftar yang ada diganti dengan data yang baru dibaca. Selanjutnya, gunakan query SQL SELECT  untuk mengambil semua data dari tabel Karyawan. Hasil  query SQL dieksekusi  dari objek DB  menggunakan executeSelectQuery dan disimpan dalam objek ResultSet RS. Program kemudian mengeksekusi loop (while (rs.next())) untuk membaca baris dari hasil kueri. Setiap baris data, yaitu ID dan nama, diambil dari hasil query. Objek Karyawan baru kemudian dibuat menggunakan data ini dan ditambahkan ke arrayKaryawan ArrayList. Terakhir, metode ini mengembalikan arrayKaryawan yang  diisi dengan data karyawan dari database.


   - Pelanggan
   - Transaksi
   - Barang
   - Makanan
   - NonMakanan
3. View
   - Login
   - Register
   - Menu Karyawan
   - Menu Barang
   - Input Pelanggan
   - Transaksi
   - Struk
     
# Output
