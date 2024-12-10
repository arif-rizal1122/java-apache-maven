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



