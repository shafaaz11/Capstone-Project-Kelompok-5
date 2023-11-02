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

   Pada 
