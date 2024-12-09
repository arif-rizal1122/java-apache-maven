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
