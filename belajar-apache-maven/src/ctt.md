# MAVEN LIFECYCLE

1. Maven bekerja dalam konsep lifecycle
2. Untuk menjalankan lifecycle, kita bisa menggunakan perintah : mvn namalifecycle
3. Lifecycle akan menjalankan banyak plugin, entah bawaan maven, atau bisa kita tambahkan plugin lain jika mau


¥ CONTOH LIFECYCLE
1. clean, menghapus folder target (tempat menyimpan hasil kompilasi)
2. compile, untuk melakukan kompilasi source code project
3. test-compile, untuk melakukan kompilasi source code project
4. test, untuk menjalankan unit test
5. package, untuk membuat distribution file aplikasi
6. install, untuk menginstalll project ke local repository, sehigga bisa digunakan di project lain di local
7. deploy,  deploy project ke remote repository di server

# BUILD PROJECT

1. Saat kita membuat project biasanya akan ada 2 jenis kode yang kita buat, kode program nya, dan kode testing nya
2. Maven mendukung hal tersebut

¥ Menjalankan Kompilasi Program
mvn compile

¥ Menjalankan Unit Test
mvn test

¥ Mem-package Project
mvn package


# DEPENDENCY

1. Proyek  aplikasi jarang sekali berdiri sendiri, biasanya membutuhkan dukungan dari pihak lain, seperti tool atau library
2. Tanpa build tool seperti Apache Maven, untuk menambahkan library dari luar, kita harus melakukannya secara manual
3. Apache Maven mendukung dependency management, dimana kita tidak perlu me-manage secara manual proses penambahkan dependency (tool atau library) ke dalam proyek aplikasi kita

¥ Dependency Scope
1. Saat kita menambahkan dependency ke project Maven, kita harus menentukan scope dependency tersebut, ada banyak scope yang ada di Maven, namun sebenarnya hanya beberapa saja yang sering kita gunakan, seperti
2. compile, ini adalah  scope default. Compile artinya dependency tersebut akan digunakan untuk build project, test project dan menjalankan project.
3. test, ini adalah scope untuk test project, hanya akan di include di bagian test project

¥ Mencari Dependency
1. https://search.maven.org/
2. https://mvnrepository.com/

# Multi Module Project

¥ Multi Module Project
1. Saat aplikasi kita sudah sangat besar, kadang ada baiknya kita buat aplikasi dalam bentuk modular
2. Misal kita pisahkan module model, controller, view, service, repository, dan lain-lain
3. Untungnya, Maven mendukung pembuatan project multi module

¥ Membuat Module Baru
1. Untuk membuat module baru, di dalam project yang sudah ada, kita hanya tinggal membuat folder baru, lalu menambahkan setting pom.xml di folder tersebut
2. Module harus memiliki parent, dimana parent nya adalah project diatas folder tersebut
3. Selanjutnya, di parent nya pun, module harus di include



# Dependency Management

Saat project kita sudah besar, kadang kita sering menggunakan banyak dependency
Masalah dengan banyaknya dependency adalah, jika kita salah menggunakan dependency yang sama namun versinya berbeda-beda
Maven mendukung fitur dependency management, dimana kita bisa memasukkan daftar dependency di parent module beserta versinya, lalu menambahkan dependency tersebut di module tanpa harus menggunakan versinya
Secara otomatis versi dependency akan sama dengan yang ada di dependency management di parent module

