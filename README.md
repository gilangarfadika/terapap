# Tutorial APAP

## Authors

- **Shabrina Nurmalitasari** - _2006596705_ - _A_

## Tutorial 1

### What I have learned today

### GitLab

1. Apa itu Issue Tracker? Apa saja masalah yang dapat diselesaikan dengan Issue Tracker?

   - Issue Tracker adalah fitur dalam platform seperti Gitlab yang berfungsi sebagai tempat untuk membagikan ide atau masalah dalam mengembangkan aplikasi. Ketika membuat issue, kita juga dapat mengkategorikan jenis issue, memberikan assignments, dan due date untuk memudahkan pengelolaan. Issue yang diterbitkan dapat dilihat progress-nya dan dikomentari oleh pengembang lain.

2. Apa perbedaan dari git merge dan git merge --squash?

   - git merge akan mempertahankan commit-commit yang terjadi pada branch yang ingin di-merge dan membuat suatu commit baru berupa 'merge commit' yang menandakan terjadinya merging. Sedangkan git merge --squash akan menyatukan semua commit yang terjadi pada branch yang ingin di-merge dan tidak ada pembuatan 'merge commit'.

3. Apa keunggulan menggunakan Version Control System seperti Git dalam pengembangan suatu aplikasi?
   - Version control system berguna untuk mengelola kode. Setiap perubahan dalam kode dapat tercatat dalam commits yang nantinya berfungsi untuk menelusuri atau mengembalikan kode ke suatu versi apabila terdapat kesalahan. Adanya fitur branch juga membantu tim untuk berkolaborasi, dimana anggota bisa mengembangkan suatu fitur atau menulis kode yang terpisah dari alur pekerjaan utama (branch utama).

### Spring

4. Apa itu library & dependency?

   - Library merupakan kumpulan kode yang dapat digunakan ulang dan umumnya memiliki fungsi untuk menyelesaikan masalah yang umum. Salah satu contoh library dalam spring adalah spring-boot-starter-web yang dapat digunakan untuk membuat aplikasi dengan metodologi Spring MVC. Dependency adalah hubungan antar kode, dimana suatu kode membutuhkan kode lain untuk menjalankan suatu fungsi. Contohnya suatu kode perlu mengakses database dengan menggunakan suatu library, maka kode tersebut dependen dengan library tersebut.

5. Apa itu Maven? Mengapa kita menggunakan Maven? Apakah ada alternatif dari Maven?
   - Definisi dari artikel GeeksforGeeks, Maven merupakan project management tools dan digunakan untuk membantu build project, download dependencies, dan project documentation seperti log/unit test reports. Maven sendiri bekerja dengan membaca pom.xml file untuk melakukan konfigurasi dependencies/plugins. Alternatif dari Maven antara lain adalah Gradle, Grunt, Gulp. <br/>
6. Jelaskan bagaimana alur ketika kita menjalankan http://localhost:8080/celsius-converter/90 sampai dengan muncul keluarannya di browser!

   - Pertama-tama url tersebut akan diproses oleh Controller yang akan menyocokkannya dengan paths dan mapping yang telah dispesifikasikan di dalam kelas. Dengan adanya anotasi @GetMapping dan path yang sesuai ('/celsius-converter'), maka fungsi yang dianotasikan tersebut berjalan dengan parameter String dan Model serta return berupa fungsi getCelsiusConverterPage.

   - Fungsi getCelsiusConverterPage bertugas untuk mengekstrak angka dari query parameter dan membuat objek model Celcius Converter (yang telah dibuat pada package model) yang nantinya akan diproses lebih lanjut pada view/html page. Apabila tidak teks tidak memiliki numerik, maka akan terbuat model 'message' dengan value suatu pesan.

   - Terakhir, pada bagian view atau html, kita dapat menggunakan model dan methodnya yang telah didefinisikan, seperti model celsiusConverter yang dipanggil method konversinya.

7. Selain untuk pengembangan web, apa saja yang bisa dikembangkan dengan Spring framework?

   - Spring bisa digunakan untuk membuat stand alone application seperti sebuah ERP Sistem (Emeritus, 2023), aplikasi mobile untuk belanja online dimana Spring digunakan untuk komponen server-side (Rappi, 2015).

8. Apa perbedaan dari @RequestParam dan @PathVariable? Kapan sebaiknya menggunakan @RequestParam atau @PathVariable?
   - Berdasarkan Java Revisited, @RequestParam akan mengambil query parameter sedangkan @PathVariable mengambil data langsung dari url. Sebaiknya gunakan @RequestParam ketika ingin ambil data dari query string sedangkan @PathVariable digunakan untuk data yang memang bagian dari url path.

### What I did not understand

- [] Concept of Inversion of Control
- [] Concept of Dependency Injection
- [] How a model object is created to be used in template

### References

https://docs.gitlab.com/ee/user/project/issues/
https://blog.mergify.com/what-is-the-difference-between-a-merge-commit-a-squash/
https://www.atlassian.com/git/tutorials/what-is-version-control
https://www.sonatype.com/launchpad/what-are-software-dependencies#:~:text=A%20software%20dependency%20is%20a,the%20other%20to%20work%20properly.
https://softwareengineering.stackexchange.com/questions/408739/what-is-the-difference-between-a-library-and-a-dependency#:~:text=Typically%2C%20a%20library%20is%20also,action%20or%20return%20some%20information.
https://www.geeksforgeeks.org/introduction-apache-maven-build-automation-tool-java-projects/
https://javarevisited.blogspot.com/2017/10/differences-between-requestparam-and-pathvariable-annotations-spring-mvc.html
