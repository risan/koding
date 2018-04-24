---
title: Tutorial PHP untuk Pemula
excerpt: Tutorial dasar PHP untuk pemula. Pelajari dasar-dasar pemrograman PHP mulai dari variable, tipe data, operator, percabangan, perulangan, fungsi, hingga Closure.
image_thumb: http://localhost:4000/img/php-small.png
image:
  path: http://localhost:4000/img/php.png
  width: 1200
  height: 800
---
PHP—akronim rekursif dari *PHP: Hypertext Preprocessor*)—merupakan bahasa pemrograman untuk web yang mulanya dikembangkan oleh Rasmus Lerdorf pada tahun 1994. PHP berjalan di sisi server (peladen) dan umumnya digunakan untuk membuat aplikasi berbasis web yang dinamis.

Meski sintaksis dan fiturnya kadang dikritik oleh programmer lain, PHP tetap populer dan mendominasi jagad internet. Perusahaan-perusahaan berbasis teknologi ternama mulai dari [Facebook](https://hhvm.com/), [Automattic](https://github.com/WordPress/WordPress) (Wordpress), [Slack](https://slack.engineering/taking-php-seriously-cf7a60065329), hingga [Wikipedia](https://en.wikipedia.org/wiki/Wikipedia:FAQ/Technical#What_software_is_used_to_run_Wikipedia?) masih setia dengan PHP yang sudah berumur lebih dari dua dekade ini. PHP pun kerap menjadi pilihan pertama untuk para pemula yang ingin belajar pemrograman.

Tutorial kali ini diperuntukan untuk pemula yang ingin belajar PHP serta dasar-dasar pemrograman. Apakah kamu siap menjadi pengembang PHP yang handal?

![I'm Ready](https://media.giphy.com/media/l1Aswx03WbLDf9kYw/giphy.gif)

Sepanjang tutorial ini kita akan menemui sejumlah kotak dengan emoji seperti berikut:

* ⚠️ **Peringatan**: Berisi peringatan penting seputar keamanan, performa, dan potensi *bug*.
* 💡 **Informasi**: Berisi informasi tambahan seputar topik yang tengah dibahas.
* 👍🏻 **Tips & Trick**: Berisi tips dan trik yang berguna dalam membantu pekerjaan *programming* sehari-hari.
* 🎨 **Clean Code**: Berisi panduan penulisan kode yang baik.
* 📘 **Dokumentasi**: Berisi tautan ke dokumentasi atau artikel lain yang membahas lebih dalam suatu topik.

## Daftar Isi

- [Hello World](#hello-world)
- [Menginstal PHP](#menginstal-php)
    - [Menginstal PHP di macOS](#menginstal-php-di-macos)
    - [Menginstal PHP di Ubuntu](#menginstal-php-di-ubuntu)
    - [Menginstal PHP di Windows](#menginstal-php-di-windows)
- [Memilih Text Editor](#memilih-text-editor)
- [Hello Again, World](#hello-again-world)
    - [PHP Interctive Shell](#php-interactive-shell)
    - [Menyimpan Kode PHP dalam File](#menyimpan-kode-php-dalam-file)
    - [Menjalankan file PHP dengan Command Line](#menjalankan-file-php-dengan-command-line)
    - [Menjalankan file PHP dengan Web Server](#menjalankan-file-php-dengan-web-server)
    - [Latihan Membuat File PHP](#latihan-membuat-file-php)
    - [Rangkuman Membuat File PHP](#rangkuman-membuat-file-php)
- [Pengetahuan Dasar Syntax PHP](#pengetahuan-dasar-syntax-php)
    - [Komentar dalam PHP](#komentar-dalam-php)
    - [PHP itu Case Insensitive, Tapi](#php-itu-case-insensitive-tapi)
    - [Latihan Dasar Syntax PHP](#latihan-dasar-syntax-php)
    - [Rangkuman Komentar dan Case Sensitivity dalam PHP](#rangkuman-komentar-dan-case-sensitivity-dalam-php)
- [Variable dalam PHP](#variable-dalam-php)
    - [Menuliskan Nama Variable](#menuliskan-nama-variable)
    - [Mencetak Nilai Variable](#mencetak-nilai-variable)
    - [Variable Scope](#variable-scope)
    - [Superglobals](#superglobals)
    - [Latihan Variable](#latihan-variable)
    - [Rangkuman Variable](#rangkuman-variable)
- [Konstanta dalam PHP](#konstanta-dalam-php)
    - [Cakupan Konstanta](#cakupan-konstanta)
    - [Tipe Data untuk Konstanta](#tipe-data-untuk-konstanta)
    - [Case-Sensitivity pada Konstanta](#case-sensitivity-pada-konstanta)
    - [Predefined & Magic Constants](#predefined--magic-constants)
    - [Latihan Konstanta](#latihan-konstanta)
    - [Rangkuman Konstanta](#rangkuman-konstanta)
- [Tipe Data dalam PHP](#tipe-data-dalam-php)
    - [Tipe Data Skalar](#tipe-data-skalar)
    - [Tipe Data Compound](#tipe-data-compound)
    - [Tipe Data Spesial](#tipe-data-spesial)
    - [Tipe Data Pseudo](#tipe-data-pseudo)
    - [Type Juggling](#type-juggling)
    - [Type Casting](#type-casting)
    - [Latihan Tipe Data](#latihan-tipe-data)
    - [Rangkuman Tipe Data](#rangkuman-tipe-data)
- [Operator](#operator)
    - [Operator Aritmetika](#operator-aritmetika)
    - [Operator Assignment](#operator-assignment)
    - [Operator Increment & Decrement](#operator-increment--decrement)
    - [Operator Bitwise](#operator-bitwise)
    - [Operator Perbandingan](#operator-perbandingan)
    - [Operator Logika](#operator-logika)
    - [Operator Ternary](#operator-ternary)
    - [Null Coalescing Operator](#null-coalescing-operator)
    - [Operator String](#operator-string)
    - [Operator Array](#operator-array)
    - [Operator Tipe](#operator-tipe)
    - [Error Control Operator](#error-control-operator)
    - [Execution Operator](#execution-operator)
    - [Prioritas Operator](#prioritas-operator)
    - [Latihan Menggunakan Operator](#latihan-menggunakan-operator)
    - [Rangkuman Operator dalam PHP](#rangkuman-operator-dalam-php)
- [Percabangan dengan if elseif dan else](#percabangan-dengan-if-elseif-dan-else)
    - [Keyword If](#keyword-if)
    - [Yoda Condition](#yoda-condition)
    - [Keyword Else](#keyword-else)
    - [Keyword Elseif](#keyword-elseif)
    - [Gaya Lain Penulisan If Elseif dan Else](#gaya-lain-penulisan-if-elseif-dan-else)
    - [Type Juggling diterapkan Pada Kondisi](#type-juggling-diterapkan-pada-kondisi)
    - [Latihan Percabangan dengan If Else dan Elseif](#latihan-percabangan-dengan-if-else-dan-elseif)
    - [Rangkuman If Elseif dan Else](#rangkuman-if-elseif-dan-else)
- [Percabangan dengan Switch](#percabangan-dengan-switch)
    - [Keyword Break dalam Switch](#keyword-break-dalam-switch)
    - [Keyword Default dalam Switch](#keyword-default-dalam-switch)
    - [Keterbatasan Switch](#keterbatasan-switch)
    - [Latihan Percabangan Switch](#latihan-percabangan-switch)
    - [Rangkuman Percabangan Switch](#rangkuman-percabangan-switch)
- [Perulangan dengan While](#perulangan-dengan-while)
    - [Infinite Loop pada Perulangan While](#infinite-loop-pada-perulangan-while)
    - [Keyword Break pada Perulangan While](#keyword-break-pada-perulangan-while)
    - [Keyword Continue pada Perulangan While](#keyword-continue-pada-perulangan-while)
    - [Gaya Lain Penulisan Perulangan While](#gaya-lain-penulisan-perulangan-while)
    - [Type Juggling pada Perulangan While](#type-juggling-pada-perulangan-while)
    - [Latihan Perulangan While](#latihan-perulangan-while)
    - [Rangkuman Perulangan While](#rangkuman-perulangan-while)
- [Perulangan Do-While](#perulangan-do-while)
    - [Infinite Loop pada Perulangan Do-While](#infinite-loop-pada-perulangan-do-while)
    - [Keyword Break pada Perulangan Do-While](#keyword-break-pada-perulangan-do-while)
    - [Keyword Continue pada Perulangan Do-While](#keyword-continue-pada-perulangan-do-while)
    - [Latihan Perulangan Do-While](#latihan-perulangan-do-while)
    - [Rangkuman Perulangan Do-While](#rangkuman-perulangan-do-while)
- [Perulangan dengan for](#perulangan-dengan-for)
    - [Keyword Break pada Perulangan For](#keyword-break-pada-perulangan-for)
    - [Keyword Continue pada Perulangan For](#keyword-continue-pada-perulangan-for)
    - [Gaya Lain Penulisan Perulangan For](#gaya-lain-penulisan-perulangan-for)
    - [Tiga Ekspresi dalam Perulangan For Bersifat Opsional](#tiga-ekspresi-dalam-perulangan-for-bersifat-opsional)
    - [Latihan Perulangan For](#latihan-perulangan-for)
    - [Rangkuman Perulangan For](#rangkuman-perulangan-for)
- [Fungsi dalam PHP](#fungsi-dalam-php)
    - [Memanggil Fungsi](#memanggil-fungsi)
    - [Aturan Penulisan Fungsi](#aturan-penulisan-fungsi)
    - [Konsep Code Reuse](#konsep-code-reuse)
    - [Fungsi dengan Parameter](#fungsi-dengan-parameter)
    - [Fungsi Variadic](#fungsi-variadic)
    - [Nilai Default Argumen pada Fungsi](#nilai-default-argumen-pada-fungsi)
    - [Passing by Value vs Passing by Reference](#passing-by-value-vs-passing-by-reference)
    - [Fungsi dengan Nilai Kembalian](#fungsi-dengan-nilai-kembalian)
    - [Deklarasi Tipe Data pada Parameter Fungsi](#deklarasi-tipe-data-pada-parameter-fungsi)
    - [Konversi Tipe Data pada Pemberian Argumen](#konversi-tipe-data-pada-pemberian-argumen)
    - [Deklarasi Tipe Data pada Kembalian Fungsi](#deklarasi-tipe-data-pada-kembalian-fungsi)
    - [Konversi Tipe Data pada Kembalian Fungsi](#konversi-tipe-data-pada-kembalian-fungsi)
    - [Latihan Fungsi](#latihan-fungsi)
    - [Rangkuman Fungsi](#rangkuman-fungsi)
- [Anonymous Function, Lambda, dan Closure](#anonymous-function-lambda-dan-closure)
    - [Anonymous Function](#anonymous-function)
    - [Anonymous Function dengan Argumen](#anonymous-function-dengan-argumen)
    - [Kegunaan Anonymous Function](#kegunaan-anonymous-function)
    - [Lambda](#lambda)
    - [Closure](#closure)
    - [Latihan Closure](#latihan-closure)
    - [Rangkuman Closure](#rangkuman-closure)
- [Menyertakan Kode dari File Lain](#menyertakan-kode-dari-file-lain)
    - [Menggunakan include_once](#menggunakan-include_once)
    - [Menggunakan require](#menggunakan-require)
    - [Menggunakan require_once](#menggunakan-require_once)
    - [Rangkuman Menyertakan Kode dari File Lain](#rangkuman-menyertakan-kode-dari-file-lain)
- [Bekerja dengan String](#bekerja-dengan-string)
    - [Menghitung Jumlah Karakter dalam String](#menghitung-jumlah-karakter-dalam-string)
    - [Mengubah String ke Huruf Kecil atau Besar](#mengubah-string-ke-huruf-kecil-atau-besar)
    - [Menghapus Spasi dari Awal dan Akhir String](#menghapus-spasi-dari-awal-dan-akhir-string)
    - [Mengulang String](#mengulang-string)
    - [Mengambil Bagian dari String](#mengambil-bagian-dari-string)
    - [Mencari String](#mencari-string)
    - [Mengganti Bagian dari String](#mengganti-bagian-dari-string)
    - [Membuat String dengan Format Tertentu](#membuat-string-dengan-format-tertentu)
    - [Memecah String ke Dalam Array](#memecah-string-ke-dalam-array)
    - [Menggabungkan Array Menjadi String](#menggabungkan-array-menjadi-string)
    - [Mengubah Baris Baru menjadi Tag br](#mengubah-baris-baru-menjadi-tag-br)
    - [Membalikan Sebuah String](#membalikan-sebuah-string)
- [Bekerja dengan Array](#bekerja-dengan-array)
    - [Key dan Value dalam Array](#key-dan-value-dalam-array)
    - [Mengecek Apakah Key Tersedia dalam Array](#mengecek-apakah-key-tersedia-dalam-array)
    - [Mengakses Elemen Array](#mengakses-elemen-array)
    - [Array Multidimensi](#array-multidimensi)
    - [Menghitung Jumlah Elemen dalam Array](#menghitung-jumlah-elemen-dalam-array)
    - [Perulangan dengan Array](#perulangan-dengan-array)
    - [Menambahkan Elemen pada Array](#menambahkan-elemen-pada-array)
    - [Mengubah Elemen Array](#mengubah-elemen-array)
    - [Menghapus Elemen Array](#menghapus-elemen-array)
    - [Menggabungkan Array](#menggabungkan-array)
    - [Menggunakan array_map](#menggunakan-array_map)
    - [Menggunakan array_filter](#menggunakan-array_filter)
    - [Menggunakan array_reduce](#menggunakan-array_reduce)
- [Penutup](#penutup)

## Hello World

![Hello World]({{ "/img/2018-03-08-tutorial-php-untuk-pemula/hello-world-meme.jpg" | absolute_url }})

Langkah pertama, mari kita membuat program "Hello World" dalam PHP. Buka alamat website berikut: [repl.it/languages/php](https://repl.it/languages/php). Situs ini memungkinkan kita untuk menulis dan menjalankan program PHP secara *online* (daring). Tidak hanya PHP, situs ini juga mendukung sejumlah bahasa pemrograman lainnya: Java, Ruby, Python, hingga Haskell.

Tikan baris kode PHP berikut pada *input* (masukan) di sebelah kiri:

```php
echo 'Hello World!';
```

Selanjutnya, klik tombol dengan simbol "play" di bagian atas untuk menjalankan kode tersebut. *Output* (keluaran) dari program akan muncul di sebelah kanan layar. Jika berhasil, kita akan mendapatkan *output* teks berupa `Hello World!`.

![Output program Hello World]({{ "/img/2018-03-08-tutorial-php-untuk-pemula/01-output-repl.png" | absolute_url }})

`echo` merupakan *keyword* dalam PHP untuk mencetak *string*. *String* adalah serangkaian karakter—dapat berupa huruf, angka, juga simbol. Dalam PHP, *string* harus diapit oleh tanda kutip tunggal (`'`) ataupun kutip ganda (`"`). Perbedaan keduanya akan dibahas lebih lanjut pada [bagian selanjutnya](#string). Penggunaan *string* tanpa kutip akan membuahkan *syntax error*.

```php
// Contoh string dengan kutip tunggal.
echo 'Aku string dengan kutip tunggal!';

// Contoh string dengan kutip ganda.
echo "Aku string dengan kutip ganda!";

// Tanpa kutip akan menghasilkan syntax error.
echo Aku pasti error;
```

> ⚠️ **Jangan lupa titik koma!**
>
> PHP mengharuskan setiap *statement* (baris instruksi) diakhiri dengan titik koma (`;`). Tanpa titik koma, program "Hello World" yang kita buat akan menghasilkan *syntax error*.

```php
// Tanpa diakhiri titik koma.
echo 'Hello World!'

// Error yang didapat:
syntax error, unexpected 'string' (T_STRING), expecting ',' or ';'
```

## Menginstal PHP

Sebelum mempelajari PHP lebih lanjut, mari kita menginstal PHP di komputer.

![You are still using PHP 5]({{ "/img/2018-03-08-tutorial-php-untuk-pemula/php-5-meme.jpg" | absolute_url }})

### Menginstal PHP di macOS

Beruntung macOS sudah menyertakan PHP di dalam sistem operasinya. Untuk mengecek instalasi PHP, buka aplikasi **iTerm** atau **Terminal**. Tikan perintah berikut di dalam terminal untuk mengecek versi PHP yang sudah terpasang:

```shell
$ php -v
```

Perintah di atas akan mencetak `output` berupa versi PHP yang terpasang:

```shell
PHP 7.2.4 (cli) (built: Mar 29 2018 15:19:46) ( NTS )
Copyright (c) 1997-2018 The PHP Group
Zend Engine v3.2.0, Copyright (c) 1998-2018 Zend Technologies
    with Zend OPcache v7.2.4, Copyright (c) 1999-2018, by Zend Technologies
```

#### Menginstal Homebrew

Biasanya versi PHP bawaan macOS sedikit tertinggal. Untuk menginstal versi teranyar, salah satu cara yang paling mudah adalah dengan menggunakan [Homebrew](https://brew.sh/). Homebrew ini merupakan *package manager* untuk macOS—layaknya dpkg pada Debian atau RPM pada Redhat.

Pertama, kita perlu menginstal aplikasi **Command Line Tools** dari Apple. Jalankan perintah berikut pada terminal:

```shell
$ xcode-select --install
```

Selanjutnya, tikan perintah berikut untuk menginstal Homebrew:

```shell
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

Setelah sukses menginstal Homebrew, kita bisa menggunakan perintah-perintah berikut:

```shell
# Untuk mengecek masalah pada instalasi Homebrew.
$ brew doctor

# Mencetak bantuan Homebrew.
$ brew help

# Memperbarui instalasi Homebrew dan daftar formulanya.
$ brew update
```

Sementara untuk mengorganisir formula (istilah *package* dalam Homebrew), kita bisa menjalankan peritah-perintah berikut:

```shell
# Untuk mencari formula.
$ brew search <teks pencarian>

# Untuk menginstal formula.
$ brew install <nama formula>

# Untuk menghapus instalasi formula.
$ brew uninstall <nama formula>

# Untuk memperbarui formula.
$ brew upgrade <name formula>

# Memperbarui semua formula yang sudah terpasang.
$ brew upgrade

# Mencetak semua formula yang sudah terpasang.
$ brew list
```

#### Memperbarui Homebrew

Untuk kamu yang sudah menginstal Homebrew sebelumnya, jangan lupa untuk menjalankan perintah berikut untuk memperbarui instalasi Homebrew beserta daftar formulanya:

```shell
$ brew update
```

#### Menginstal PHP dengan Homebrew

Jalankan perintah berikut di terminal untuk menginstal PHP:

```shell
$ brew install php
```

Setelah instalasi tuntas, *restart* terminal atau buka tab baru. Jalankan perintah berikut untuk memverifikasi versi PHP yang terpasang:

```shell
$ php -v
```

Pada saat artikel ini ditulis formula `php` akan menginstall PHP versi `7.2.4`.

> 💡 Saat tutorial ini ditulis, formula-formula pada `homebrew-php` tengah dalam proses penyatuan ke dalam *repository* utama [`homebrew-core`](https://github.com/Homebrew/homebrew-core). Dengan penyatuan ini kita tidak perlu lagi men-`tap` [`homebrew-php`](https://github.com/Homebrew/homebrew-php) untuk menginstall PHP. Ikuti diskusinya lebih lanjut [di sini](https://github.com/Homebrew/homebrew-php/issues/4721).

### Menginstal PHP di Ubuntu

Instalasi PHP pada Ubuntu dan distro Linux lainnya sangatlah mudah. *Package* PHP umumnya sudah tersedia pada *repository* bawaan. Pun begitu, versi PHP yang tersedia biasanya sedikit tertinggal.

Untuk mendapatkan PHP versi teranyar, kita bisa menambahkan PPA (Personal Package Archive) dari `ondrej/php`. Buka terminal dan jalankan perintah berikut:

```shell
$ sudo add-apt-repository ppa:ondrej/php
```

Setelah PPA ini berhasil ditambahkan, jangan lupa untuk memperbarui daftar *package* pada komputer dengan menjalankan perintah berikut:

```shell
$ sudo apt-get update
```

Gunakan perintah `apt-cache search` untuk mencari versi PHP yang diinginkan:

```shell
$ sudo apt-cache search php7.2
```

Jalankan perintah berikut untuk menginstall PHP versi 7.2:

```shell
$ sudo apt-get install php7.2 -y
```

Untuk memverifikasi versi PHP yang terpasang, jalankan perintah berikut di terminal:

```shell
$ php -v
```

### Menginstal PHP di Windows

Sayangnya penulis tidak berpengalaman dengan sistem operasi Windows. Untungnya ada sejumlah *bundle* aplikasi yang mudah untuk dipasang dan umumnya menyertakan paket komplit mulai dari PHP, web *server*, hingga *database*. Berikut beberapa pilihan populer:

#### XAMPP

[XAMPP](https://www.apachefriends.org) merupakan salah satu *bundle* aplikasi yang populer untuk bekerja dengan PHP di Windows. Selain PHP, dalam *bundle*-nya ia turut menyertakan Apache sebagai web server dan MariaDB (*fork* dari MySQL yang dikembangkan komunitas) untuk *database*-nya. XAMPP juga menyertakan phpMyAdmin untuk mempermudah kerja dengan database.

> 📘 Cek tutorial [Cara Menggunakan XAMPP untuk Menjalankan PHP & MySQL](https://www.niagahoster.co.id/blog/cara-menggunakan-xampp/) dari Niagahoster.

#### Laragon

![Website Laragon]({{ "/img/2018-03-08-tutorial-php-untuk-pemula/02-laragon-website.png" | absolute_url }})

Dibandingkan dengan XAMPP, [Laragon](https://www.laragon.org) relatif lebih modern dan menawarkan banyak fitur. Untuk web *server*, Laragon menyertakan Apache dan Nginx. Untuk *database*-nya, Laragon mengandalkan MySQL. Selain itu Laragon menyediakan beragam *tools* esensial: Git, Composer, Node.js hingga Yarn. Dengan Laragon kita juga dapat dengan mudah membuat proyek berbasis Wordpress, Symfony, Laravel hingga Drupal. Fitur lainnya yang menggiurkan adalah kemampuannya untuk membuat *virtual host* secara otomatis.

Cek [dokumentasi resmi Laragon](https://www.laragon.org/docs/install.html) untuk mempelajari cara menginstal dan ragam fitur yang ditawarkan.

#### Aplikasi Alternatif Lainnya

Selain dua *bundle* aplikasi di atas, masih banyak alternatif lainnya yang bisa kamu coba:

- [MAMP](https://www.mamp.info/) - *bundle* aplikasi PHP, Apache, Nginx, MySQL dan Python.
- [WampServer](http://www.wampserver.com/) - *bundle* aplikasi PHP, Apache dan MySql.
- [PHP for Windows](https://windows.php.net/download/) - jika kamu ingin menginstal PHP langsung dari *binaries* nya.

## Memilih Text Editor

![Website Laragon]({{ "/img/2018-03-08-tutorial-php-untuk-pemula/vim-tweet.png" | absolute_url }})

Yang kita butuhkan selanjutnya adalah *text editor* (editor teks) yang mumpuni. Ada banyak pilihan *text editor* di luar sana. Berikut adalah dua *text editor* yang cocok untuk pemula:

### Sublime Text

[Sublime Text](https://www.sublimetext.com/) merupakan salah satu *text editor* yang sangat populer. Ia tersohor karena ringan dan cepat, bahkan saat membuka file dengan ukuran yang sangat besar. Meski tak sepenuhnya gratis, ia memberikan waktu *trial* selamanya. Sayangnya, karena dikembangkan seorang diri, pembaruan aplikasinya sangat jarang.

![Sublime Text]({{ "/img/2018-03-08-tutorial-php-untuk-pemula/03-sublime-text-website.png" | absolute_url }})

### Visual Studio Code

[Visual Studio Code](https://code.visualstudio.com/) atau VSCode merupakan *text editor* *open source* dari Microsoft yang akhir-akhir ini popularitasnya kian menanjak. Ia dikembangkan berdasarkan *text editor* [Atom](https://atom.io/) besutan Github. VSCode menawarkan fitur yang mutakhir untuk sebuah *text editor*: *auto-completion* dengan *IntelliSense*, *debugger*, integrasi Git, serta *built-in* terminal yang sangat responsif.

Dukungan komunitasnya juga sangat besar. Pengembangan *text editor*-nya sangat aktif serta banyak *extension* yang tersedia untuk mempermudah pekerjaan *coding* sehari-hari.

![Visual Studio Code]({{ "/img/2018-03-08-tutorial-php-untuk-pemula/04-vscode-website.png" | absolute_url }})

## Hello Again, World

Pada bagian sebelumnya, kita telah berhasil menjalankan kode PHP di situs [repl.it](https://repl.it). Dengan PHP yang sudah terpasang, mari kita belajar menjalankan kode PHP di komputer kita sendiri.

### PHP Interactive Shell

REPL sebenarnya merupakan akronim dari: Read–Eval–Print Loop. Ia berupa *interactive shell* dimana kita bisa memasukan kode yang akan langsung dieksekusi dan ditampilkan hasilnya di dalam *shell* itu sendiri. Banyak bahasa pemrograman yang menyediakan fitur seperti REPL ini, termasuk PHP.

Untuk menjalankan *interactive shell* dari PHP, buka terminal dan jalankan perintah berikut:

```shell
$ php -a
```

Jika perintah di atas berhasil, kita akan mendapati kursor berada di sebelah kanan teks `php >`. Tanda `php >` ini berarti `shell` siap untuk menerima masukan kode.

```shell
$ php -a
Interactive shell

php >
```

> 📘 **Tidak berhasil di Windows?**
>
> Bila perintah di atas tidak berjalan di Windows, ada kemungkinan lokasi dari aplikasi PHP yang terpasang tidak tidak terdaftar di *environtment variables*. Sayangnya penulis tidak familiar dengan sistem operasi yang satu ini. Sila baca tulisan dari web Petani Kode berikut: [Cara Menjalankan PHP Melalui CMD](https://www.petanikode.com/php-cmd/).

Tikan kode "Hello World" yang kita buat sebelumnya. Namun kali ini ganti teksnya dengan `Hello Again, World!`. Tekan `enter` untuk menjalankan kode. Jika berhasil kita akan mendapati teks tersebut tercetak di layar terminal:

```shell
php > echo 'Hello again, World!';
Hello again, World!
```

> 👍🏻 **Tab completion pada interactive shell**
>
> Jika hanya ada satu kemungkinan untuk *auto-completion*, menekan tombol *tab* satu kali akan otomatis melengkapi kode kita. Jika ada beberapa kemungkinan, tekan tombol `tab` dua kali untuk mencetak semua kemungkinan *auto-completion*.

### Menyimpan Kode PHP dalam File

Sekarang kita belajar menyimpan kode PHP di dalam *file*. Buka *text editor* yang telah kita pasang. Dengan *text editor*, buatlah sebuah *file* baru dan tikan kode PHP berikut:

```php
<?php
// 01_hello.php

echo 'Hello again, World!';

?>
```

Simpan *file* tersebut di lokasi yang mudah dicari; misalnya dalam direktori `belajar-php` di `Document`. Beri nama *file* tersebut: `01_hello.php`. Pastikan *file* tersimpan dengan ekstensi `.php`.

#### PHP Tags

Berbeda saat di dalam *interactive shell*, kode PHP dalam sebuah file harus diapit di antara tag pembuka `<?php` dan tag penutup `?>`. Ini karena di dalam PHP, kita diperbolehkan untuk menyisipkan jenis dokumen lain; dokumen HTML misalnya. Tag pembuka dan penutup ini akan memberitahu *parser* di mana kode PHP di mulai dan berakhir.

```php
<?php

echo 'Hello from PHP 🐘';

?>

<h1>Hello from HTML 👋</h1>

<?php

echo 'Hello again from PHP 🐘';

?>
```

Bila kode PHP di antara kedua tag hanya terdiri dari satu baris *statement*, kita bisa menempatkan tag pembuka dan penutup di baris yang sama seperti ini:

```php
<?php echo 'Hello from PHP 🐘'; ?>

<h1>Hello from HTML 👋</h1>

<?php echo 'Hello again from PHP 🐘'; ?>
```

> 📘 Baca lebih lanjut di dokumentasi: [PHP Tags](https://secure.php.net/manual/en/language.basic-syntax.phptags.php).

> ⚠️ **Mencampurkan kode PHP dan HTML adalah praktik yang buruk**
>
> Seperti contoh di atas, mencampurkan kode PHP dan HTML dianggap praktik yang tidak baik. Ia bisa menjadi indikasi kurangnya [*separation of concerns*](https://en.wikipedia.org/wiki/Separation_of_concerns). Serta merupakan salah satu celah keamanan yang bisa dieksploitasi—misalnya saat meng-`echo` data masukan dari pengguna lantas kita lalai men-*sanitize* input & tidak meng-*escape* output.
>
> Untuk saat ini, kita kesampingkan dulu. Karena topik ini relatif lebih sulit untuk pemula.

#### Lupakan Tag Penutup

Jika file tersebut hanya ada kode PHP di dalamnya, kita tidak perlu menuliskan tag penutup `?>`. Dan umumnya, ini yang dipraktikan sejumlah *developer* PHP. Mari kita hilangkan tag penutup dari file `01_hello.php` kita:

```php
<?php
// 01_hello.php

echo 'Hello again, World!';
```

Jangan lupa simpan perubahan di atas. Tugas kita sekarang adalah menjalankan file PHP tersebut!

![Hey, don't even worry about it](https://media.giphy.com/media/374pcIBVEGb6g/giphy.gif)

> 💡 **Tag pembuka tidak akan disertakan pada contoh kode**
>
> Pada contoh-contoh kode berikutnya, kita sengaja tidak akan menyertakan tag pembuka `<?php` agar lebih ringkas. Jadi jika kamu menyalin contoh kode, jangan lupa untuk menambahkan kode pembuka.

### Menjalankan file PHP dengan Command Line

Salah satu cara untuk menjalankan file PHP adalah dengan melalui *command line* atau terminal. Buka terminal dan masuk ke dalam direktori tempat kamu menyimpan file `01_hello.php`.

```shell
$ cd ~/Documents/belajar-php
```

`cd` (akronim dari *change directory*) adalah perintah untuk merubah lokasi dari direktori kerja pada terminal. Arahkan pada direktori tempat kita menyimpan file `01_hello.php`. Penulis menggunakan sistem operasi macOS dan menyimpan file PHP tersebut di dalam direktori `belajar-php` pada `Documents`. Jika kamu menggunakan Windows dan menyimpannya pada `My Documents`, secara `default` lokasi `My Documents` berada di:

```shell
$ cd C:\Users\<nama user>\Documents\belajar-php
```

Setelah berada di dalam direktori `belajar-php`, tikan perintah berikut di terminal untuk menjalankan file `01_hello.php`:

```shell
$ php 01_hello.php
```

Jika berhasil, kita akan mendapatkan teks `Hello again, World!` tercetak di layar. Sebenarnya kita juga bisa menggunakan *absolute path* tanpa harus `cd` ke direktory `belajar-php`:

```shell
$ php ~/Documents/belajar-php/01_hello.php
```

> 📘 Baca lebih lanjut di dokumentasi: [Executing PHP files](https://secure.php.net/manual/en/features.commandline.usage.php).

### Menjalankan file PHP dengan Web Server

Cara kedua untuk menjalankan file PHP adalah dengan web server. Cara inilah yang paling umum digunakan.

![Diagram client-server]({{ "/img/2018-03-08-tutorial-php-untuk-pemula/05-client-server-diagram.png" | absolute_url }})

Bila disederhanakan, alurnya seperti ini:

1. *Client* memasukan alamat dari sebuah web pada peramban atau *browser*. Lalu *browser* mengirimkan *request* untuk sebuah laman web atau dokumen ini ke *server*.
2. *Request* dari *client* diterima web *server*. Apabila dokumen yang diminta berupa file statis (seperti file HTML, gambar, CSS, atau Javascript), umumnya web *server* dapat melayani permintaan dokumen tersebut secara langsung. Web *server* kemudian akan mengirimkan respon kepada *client* berupa dokumen yang diminta.
3. Namun bila dokumen yang diminta tersebut adalah file PHP, web *server* akan meneruskan file tersebut ke PHP *interpreter* untuk diproses terlebih dahulu.
4. Hasil keluaran dari file PHP inilah yang kemudian akan dikirimkan ke *client* oleh web *server*. Keluarannya dapat berupa teks, laman HTML, XML, JSON, hingga dokumen berupa PDF atau JPEG.

Ada banyak pilihan web *server* yang bisa kita gunakan. Sejak versi 5.4, PHP sendiri sudah menyertakan web *server* bawaan yang siap digunakan untuk kepentingan *development*. Untuk mempermudah, dalam tutorial ini kita cukup menggunakan web *server* bawaan PHP.

> ⚠️ **Web server bawaan PHP bukan untuk production!**
>
> Web *server* bawaan PHP ini berjalan dalam *single-threaded process* sehingga hanya mampu mengolah satu *request* dalam satu waktu. Web *server* bawaan ini hanya diperuntukan untuk kepentingan *development*. Untuk *production* gunakanlah web *server* yang performanya sudah teruji seperti Nginx atau Apache.

Buka kembali terminal, dan arahkan lokasi dari direktori kerja ke direktori tempat kita menyimpan file `01_hello.php`:

```shell
$ cd ~/Documents/belajar-php
```

Kemudian tikan perintah berikut untuk menjalankan web server bawaan PHP:

```shell
$ php -S localhost:8000
```

Bila berhasil, web server akan berjalan pada alamat `localhost` dan *port* `8000`. Keluaran seperti berikut akan tercetak pada layar terminal:

```shell
PHP 7.2.4 Development Server started at Sat Apr 20 19:01:12 2018
Listening on http://localhost:8000
Document root is /Users/risan/Documents/belajar-php
Press Ctrl-C to quit.
```

Buka *browser* dan masukan alamat [localhost:8000/01_hello.php](http://localhost:8000/01_hello.php). Kita akan mendapati teks `Hello again, World!` tercetak pada layar *browser*.

![Tampilan pada browser]({{ "/img/2018-03-08-tutorial-php-untuk-pemula/06-hello-again-world.png" | absolute_url }})

> 📘 Baca lebih lanjut di dokumentasi: [Built-in web server](https://secure.php.net/manual/en/features.commandline.webserver.php).

Dengan `echo`, kita juga bisa mencetak tag HTML. Ubah *file* `01_hello.php` seperti kode berikut dan coba jalankan kembali di *browser*. Teks `Hello again, World!` akan tercetak besar sekarang.

```php
<?php
// 01_hello.php

echo '<h1>Hello again, World!</h1>';
```

Dalam jaringan komputer, `localhost` berarti "komputer ini"—komputer yang tengah kita pakai. Secara *default*, `localhost` akan di-*resolve* ke dalam IP `127.0.0.1`. Dalam skema ini komputer kita menjadi *client* sekaligus *server*-nya.

Nomor `port` yang digunakan pun tidak harus `8000`, bisa `3000`, `4000` atau `9000`. Selama nomor *port* yang digunakan `>= 1024` dan tidak sedang digunakan oleh aplikasi lain.

> 💡 **Default Port untuk HTTP & HTTPS**
>
> Mungkin kamu bertanya-tanya: mengapa saat membuka laman facebook, kita tidak perlu mencantumkan nomor *port*? Cukup: `https://www.facebook.com`. Mengapa kita perlu mencantumkan nomor *port* pada contoh di atas?
>
> Ini karena web server Facebook dan situs-situs lainya menggunakan *port default* yang disediakan untuk HTTP & HTTPS. HTTP merupakan protokol yang menjadi fondasi komunikasi data pada jaringan internet. Layanan HTTP ini menggunakan *port* 80 sementara HTTPS menggunakan *port* 443.
>
> Apabila web server kita menggunakan *port* diluar `80` atau `443`, maka kita perlu mencantumkan nomor *port* yang digunakan; seperti pada contoh di atas: `localhost:8000`. Kamu bisa saja mengakses Facebook dengan mencantumkan *port*-nya: [`www.facebook.com:443`](https://www.facebook.com:443).

🎉 Selamat kamu telah berhasil menjalankan file PHP dengan web server!

![Congratulations](https://media.giphy.com/media/9sVS967nejlqU/giphy.gif)

### Latihan Membuat File PHP

Untuk latihan, buatlah *file* baru dengan nama `02_hello_php_html.php`. Tikan kode berikut:

```php
<?php echo 'Hello from PHP 🐘'; ?>

<h1>Hello from HTML 👋</h1>

<?php

echo '<h1>Hello from PHP again 🐘<h1>';
echo '<img src="https://images.unsplash.com/photo-1519354754184-e1d9c46182c0?w=500&q=80">';
```

Perhatikan kembali bagaimana kita menyisipkan dokumen HTML ke dalam file PHP. Juga cermati *tag* penutup php yang tidak disertakan di bagian akhir *file*.

Jangan lupa simpan *file* `02_hello_php_html.php` di atas dan coba jalankan pada *browser*, kita akan mendapatkan tampilan seperti berikut:

![Output latihan 1]({{ "/img/2018-03-08-tutorial-php-untuk-pemula/07-exercise-1.png" | absolute_url }})

### Rangkuman Membuat File PHP

Dari subbab ini kita bisa menyimpulkan beberapa poin:

1. Kita bisa mencampurkan *file* PHP dengan dokumen lain (HTML misalnya).
2. Mencampurkan *file* PHP dengan dokumen HTML dianggap sebagai praktik yang buruk.
3. File PHP tidak butuh tag penutup (`?>`), kecuali kita ingin menyisipkan dokumen lain setelahnya.
4. Kita bisa mencetak tag HTML dalam kode PHP.
5. *Server* bawaan PHP hanya untuk kepentingan pengembangan, jangan gunakan untuk *production*!

## Pengetahuan Dasar Syntax PHP

### Komentar dalam PHP

*Comment* atau komentar adalah bagian yang tidak diikutsertakan dalam eksekusi sebuah program. Ia bertujuan sebagai catatan atau pengingat untuk pengembang.

Umumnya ia digunakan untuk:

* Menjelaskan alur program yang rumit.
* Justifikasi atau alasan mengapa kita menerapkan suatu algoritma atau solusi tertentu.
* Sebagai dokumentasi untuk sebuah kelas atau fungsi (akan kita bahas nanti).

Dalam PHP sendiri, komentar bisa satu baris ataupun lebih. Untuk komentar satu baris yang pendek, gunakan dua garis miring: `//`

```php
// Bisa dalam baris tersendiri.
echo 'Hello, World 🌏';

echo 'Hello, Tatooine 👽'; // Atau sebaris dengan kode.
```

Untuk komentar satu baris, PHP juga mendukung komentar *ala shell-style* dengan tanda pagar: `#`. Pun begitu umumnya *developer* PHP jarang menggunakannya.

```php
# Komentar ala shell-style.
echo 'Hello, Alderaan 👋';

echo 'Hello, Dagobah 🤺'; # Jarang digunakan developer PHP.
```

Bila komentarnya cukup panjang, kita bisa menuliskannya dalam beberapa baris; mengapitnya dengan tanda `/*` dan `*/`:

```php
/* Contoh komentar multi-baris.
Gunakan jika kamu harus menuliskan komentar yang panjang. */
echo 'Hello, Naboo 👸🏻';
```

Komentar multi-baris ini umumnya digunakan untuk mendokumentasikan suatu kelas atau metode seperti berikut:

```php
/**
 * Get the version number of the application.
 *
 * @return string
 */
public function version()
{
    return static::VERSION;
}
```

> 🎨 **Hati-hati dalam menuliskan komentar!**
>
> Meski berguna sebagai catatan atau pengingat, komentar pada kode bisa jadi sebuah indikasi kurangnya tingkat *readibility* (keterbacaan) dari kode yang kita tulis. Kode yang baik harus mudah dibaca dan mudah dipahami tujuannya, meski tanpa komentar.
>
> Baca lebih lanjut di buku [Clean Code](https://www.amazon.com/Clean-Code-Handbook-Software-Craftsmanship/dp/0132350882) karya Robert C. Buku ini sangat direkomendasikan untuk para *programmer*. Salah satu bahasannya adalah tentang penggunaan komentar.

![Comment is not necessary](https://media.giphy.com/media/3YKNXZynJMGg8/giphy.gif)

### PHP itu Case Insensitive, Tapi

Hampir semua penulisan *syntax* pada PHP itu *case insensitive*—huruf kecil atau huruf besar tidak berpengaruh. Mulai dari *keywords* (seperti `echo`, `if`, `for`, dan lainnya), nama-nama fungsi, hingga nama-nama kelas; semuanya *case insensitive*. Perhatikan ragam penulisan kode-kode berikut (tak perlu khawatir jika kodenya tidak dimengerti).

```php
echo 'Hello, World!';
EcHo 'Hello, World!'; // Hasilnya sama-sama valid.

echo strtoupper('Huruf Besar'); // Fungsi merubah ke huruf besar.
echo StrToUPPer('Huruf Besar'); // Nama fungsi case insensitive.

$dateTime1 = new DateTime(); // Kelas untuk tanggal dan waktu.
$dateTime2 = new dATeTiMe(); // Nama kelas pun case insensitive.

echo $dateTime1->getTimestamp(); // Metode untuk mendapatkan unix timestamp.
echo $dateTime2->GetTiMEsTAmp(); // Nama metode pun case insensitve.
```

Tapi lain halnya dengan *variable*. *Variable* pada PHP itu *case sensitive*—di mana besar kecilnya huruf berpengaruh.

```php
$message = 'Hello, World!';

echo $message; // Berhasil mencetak output tanpa pesan error.
echo $mEssAge; // Akan membuahkan pesan error.
```

> 🎨 **Konsistensi dalam penulisan kode itu penting**
>
> Meski hampir semua *syntax* dalam PHP itu *case insensitive*. Konsistensi penulisan besar-kecilnya huruf juga penting. Untuk *keywords* seperti `echo` juga fungsi-fungsi bawaan seperti `strtoupper()`, selalu gunakan huruf kecil. Untuk nama-nama kelas, gunakan *studly caps* seperti `DateTime`. Sementara untuk nama *method*, gunakan *camel case* seperti `getTimestamp()`.
>
> Komunitas PHP sendiri memiliki standard penulisan kode yang dituangkan dalam panduan: [PSR-1](https://www.php-fig.org/psr/psr-1/) dan [PSR-2](https://www.php-fig.org/psr/psr-2/).

### Latihan Dasar Syntax PHP

Sebagai latihan buatlah *file* baru dengan nama `03_basic_syntax.php` lalu tikan kode berikut:

```php
<?php
// 03_comments_and_case_sensitivity.php

// This is a one-line comment.
echo 'Hello, World 🌏'; // Comment can be inline right after the code.

# This is shell-style comment example.
# The following code proves that PHP keyword is case insensitive.
ECHO 'HELLO SUN 🌞';

/*
This is a multiple-lines comment example.
PHP is case-insensitive except for a variable name!
Thus $message and $MESSAGE are two different variables.
*/
$message = 'hello lower case!';
$MESSAGE = 'HELLO UPPER CASE!';

echo $message;
echo $MESSAGE;
```

Perhatikan kembali tiga cara penulisan komentar di atas. Cermati juga bahwa PHP *case-sensitive* untuk penamaan *variable* saja.

### Rangkuman Komentar dan Case Sensitivity dalam PHP

Dari subbab ini kita bisa menyimpulkan poin-poin berikut:

1. Komentar tidak diikutsertakan dalam eksekusi kode.
2. Dalam PHP ada tiga cara untuk menuliskan komentar: dengan tanda `//`, *shell-style* dengan tanda `#`, serta `/*...*/` untuk komentar multi-baris.
3. Hati-hati dalam menuliskan kode, karena ia bisa menjadi indikasi rendahnya tingkat *readibility* dari kode yang kita tuliskan.
4. PHP itu *case-insenstive*, kecuali untuk penulisan nama *variable*.
5. Meski PHP *case-insensitive*, konsistensi dalam penulisan kode itu sangat penting. Selalu gunakan huruf kecil untuk *keyword* atau fungsi-fungsi bawaan PHP, gunakan *studly caps* untuk nama kelas dan *camel case* untuk nama metode.

## Variable dalam PHP

*Variable* berfungsi untuk menampung sebuah infomasi atau data. Data yang ditampung bisa beragam macamnya: *string*, angka, larik dan lainnya (akan kita bahas di bab selanjutnya). Dalam PHP tidak ada *syntax* khusus untuk mendeklarasikan sebuah *variable*, kita cukup mengawali nama *variable* dengan tanda dolar (`$`).

```php
$name = 'Luke Skywalker'; // Variable menampung data string berupa nama.

$price = 15000.5; // Variable menampung data angka berupa harga.

$phpIsAwesome = true; // Variable menampung data boolean.

$oddNumbers = [1, 9, 7]; // Variable menampung larik angka-angka ganjil.
```

Dan sesuai dengan namanya, nilai dari *variable* bisa diubah:

```php
$name = 'Anakin Skywalker';

$name = 'Luke Skywalker'; // Nilai variable bisa diubah.

$name = 11; // Bahkan bisa diubah dengan tipe data lainnya.
```

> 🎨 **Tulislah kode dalam Bahasa Inggris**
>
> Usahakan untuk selalu menggunakan Bahasa Inggris dalam menulis kode; mulai dari nama *variable*, nama kelas, hingga komentar. *Keyword* serta fungsi-fungsi bawaan PHP pun ditulis dalam Bahasa Inggris. Dengan begitu kode yang kita buat akan terbaca lebih natural karena menggunakan satu bahasa yang sama. Istilah-istilah teknikal pun umumnya lebih mudah dipahami jika ditulis dalam Bahasa Inggris.
>
> Contoh kode-kode pada tutorial ini pun akan menggunakan Bahasa Inggris.

### Menuliskan Nama Variable

Untuk penamaan *variable* sendiri, kita bisa menggunakan huruf, angka atau *underscore* (`_`). Namun nama *variable* tidak boleh didahului oleh angka.

```php
// Nama variable valid dengan huruf, angka & underscore.
$R2_D2_Voice = 'beep beep';

// Nama variable boleh diawali dengan underscore.
$_yoda = 'Do or do not. There is no try';

// Nama variable hanya boleh didahului huruf atau underscore.
// Akan membuahkan syntax error 😜
$1direction = 'story of my life';
```

#### ⚠️ Nama variable case sensitive

Perlu diingat bahwa nama *variable* dalam PHP bersifat *case sensitive*—dimana besar-kecilnya huruf berpengaruh. Dengan begitu `$name`, `$NAME` atau `$Name` adalah tiga buah *variable* yang berbeda.

```php
$name = 'Anakin Skywalker';

// Menghasilkan error: Notice: Undefined variable: NAME
echo $NAME;

// Menghasilkan error juga.
echo $Name;
```

#### 💡 *Camel Case* vs *Snake Case*

Umumnya *developer* PHP menulisankan nama *variable* dengan gaya *camel case* atau *snake case*:

```php
// Contoh camel case.
$shipName = 'Milenium Falcon';

// Contoh snake case.
$ship_name = 'Milenium Falcon';
```

*Framework* atau kerangka kerja PHP yang populer seperti [Symfony](https://symfony.com) dan [Laravel](https://laravel.com), menerapkan gaya `camelCase` di dalam *code base*-nya. Sementara *framework* [CodeIgniter](https://codeigniter.com/) juga *platform* blog [Wordpress](https://wordpress.org) menggunakan gaya `snake_case`.

Penulis sendiri, diluar CodeIgniter dan Wordpress, selalu menerapkan gaya penulisan `camelCase`—meniru panduan [PSR-1](https://www.php-fig.org/psr/psr-1/) dalam aturan penulisan nama *method*.

#### ️⚠️ Gunakan nama variable yang deskriptif

Sebagai *programmer*, waktu yang kita habiskan untuk membaca kode jauh lebih besar daripada menuliskan kode itu sendiri. Oleh karenanya gunakan nama *variable* yang singkat namun tetap deskriptif dan mudah dipahami. Nama *variable* yang panjang namun mudah dipahami kegunaanya, justru jauh lebih baik daripada nama *variable* yang singkat tapi membingungkan.

![Gunakan nama variable yang deskriptif]({{ "/img/2018-03-08-tutorial-php-untuk-pemula/terrible-variable-names-meme.jpg" | absolute_url }})

Perhatikan kode berikut:

```php
$price = 1000;
$x = 4; // Quantity.
$disc = 50; // Discount percentage.

$total = $price * $x;
// Total with discount.
$total = $total - ($total * ($disc / 100));
```

Tanpa komentar, akan sulit bagi kita memahami konteks kode di atas. Apa itu `$x`? Apa itu `$disc`? Kita bisa perbaiki tingkat *readibility* dari kode di atas hanya dengan memberikan nama *variable* yang deskriptif.

```php
$pricePerItem = 1000;
$quantity = 4;
$discountPercentage = 50;

$subTotal = $pricePerItem * $quantity;
$total = $subTotal - ($subTotal * ($discountPercentage / 100));
```

Dengan pemberian nama yang deskriptif konteks kode di atas menjadi jelas: menghitung total pembayaran beserta diskon yang diterapkan. Kita bahkan tidak perlu menambahkan komentar untuk menjelaskan konteks kode di atas. Ingat, komentar bisa jadi indikasi jika kode yang kita tulis rendah tingkat *readibility*-nya.

### Mencetak Nilai Variable

Contoh kode-kode *variable* di atas, tidak akan mencetak apapun bila dijalankan. Untuk mencetak nilai *variable*, kita bisa gunakan `echo` tanpa kutip tunggal:

```php
$name = 'Luke Skywalker';

echo $name;
```

#### Kutip Tunggal vs Kutip Ganda

Kutip tunggal akan mencetak *string* apa adanya. Sementara kutip ganda mampu mencetak nilai *variable* yang diapitnya.

```php
$name = 'Luke';

echo '$name, I am your father'; // Mencetak: $name, I am your father

echo "$name, I am your father"; // Mecetak: Luke, I am your father
```

Dengan kutip ganda, kita juga bisa mengapit *variable* dengan tanda kurung kurawal: `{` dan `}`. Dengan begitu kita bisa memisahkan *variable* dengan karakter biasa:

```php
$jediName = 'Luke';
$lightsaberColor = 'blue';

// Mencetak: Luke's lightsaber is blue
echo "{$jediName}'s lightsaber is {$lightsaberColor}";
```

Selain itu, dengan kutip ganda kita bisa mencetak [*escaped characters*](https://secure.php.net/manual/en/language.types.string.php#language.types.string.syntax.double) dengan mendahuluinya dengan garis miring (`\`):

```php
$ship = 'Milenium Falcon';
$rentPrice = 15000;

// \n => menyisipkan baris baru
// \$ => mencetak tanda dolar
echo "Ship: $ship\nRent Price: \$$rentPrice";
```

Apabila dijalankan lewat *Command Line* kita akan mendapatkan keluaran seperti berikut:

```shell
Ship: Milenium Falcon
Rent Price: $15000
```

> 💡 Apabila dijalankan lewat web *server*, baris baru (`\n`) yang disisipkan tidak akan tampak pada *browser*. Ini terjadi karena *browser* memperlakukan respon dari web server sebagai dokumen HTML—dimana baris baru harus direpresentasikan dengan tag `<br>`.

### Variable Scope

*Variable scope* berarti cakupan dari sebuah *variable*. *Scope* dari suatu *variable* akan bergantung pada lokasi dimana ia dideklarasikan. *Scope* juga mempengaruhi di bagian mana saja *variable* tersebut bisa diakses. Dalam PHP sendiri *variable scope* bisa dikelompokan ke dalam dua kategori: *local scope* dan *global scope*.

#### Local Scope

*Variable* yang dideklarasikan di dalam sebuah fungsi atau metode akan bersifat *local*. *Variable* tersebut tidak akan bisa diakses dari luar fungsi atau metode dimana ia dideklarasikan.

```php
function printCatImage()
{
    // $catImageUrl berada dalam local scope
    // sehingga hanya bisa diakses dalam fungsi printCatImage() saja.
    $catImageUrl = 'http://thecatapi.com/api/images/get?format=src&type=gif';

    echo "<img src='$catImageUrl'>";
}

// Mengakses $catImageUrl di luar fungsi printCatImage() akan membuahkan error
// Undefined variable: catImageUrl
echo $catImageUrl;
```

#### Global Scope

Sementara variable yang dideklarasikan di luar sebuah fungsi atau metode, tergolong dalam *global scope*. Secara *default*, ia pun hanya bisa diakses dari luar sebuah fungsi atau metode.

```php
// $catEmojis berada di global scope
// Secara default hanya bisa diakses dari luar fungsi atau metode.
$catEmojis = '😸😹😻😽';

function printCatEmojis()
{
    // Akan menghasilkan error karena $catEmojis hanya tersedia di global
    // scope, tapi tidak dalam local scope dari printCatEmojis().
    echo $catEmojis;
}

// Memanggil fungsi printCatEmojis() yang akan menghasilkan error.
printCatEmojis();
```

Kita bisa mengakses *variable global* dari dalam *local* scope dengan menggunakan *keyword* `global`:

```php
$catEmojis = '😸😹😻😽';

function printCatEmojis()
{
    // Gunakan keword global untuk mengakses variable global dari dalam local scope.
    global $catEmojis;

    echo $catEmojis;
}

// Akan mencetak emoji kucing: 😸😹😻😽
printCatEmojis();
```

Cara lainnya untuk mengakses *variable* *global* dari dalam *local* scope adalah dengan menggunakan *predefined variable* `$GLOBALS`:

```php
$catEmojis = '😸😹😻😽';

function printCatEmojis()
{
    // Menggunakan predefined variable $GLOBALS.
    echo $GLOBALS['catEmojis'];
}

// Akan mencetak emoji kucing: 😸😹😻😽
printCatEmojis();
```

![Jangan mengandalkan global variable]({{ "/img/2018-03-08-tutorial-php-untuk-pemula/global-variables-meme.jpg" | absolute_url }})

> ⚠️ **Jangan mengandalkan global variable**
>
> Menggunakan *global variable* di dalam sebuah fungsi atau metode merupakan praktik yang buruk. Kode di dalam fungsi tersebut menjadi bergantung pada kondisi di luar cakupanya. Bayangkan jika ada fungsi lain yang mengubah nilai dari `$catEmojis` di atas, hasil keluaran dari fungsi `printCatEmojis()` menjadi tidak *reliable*. *Programmer* juga dipaksa untuk memahami konteks aplikasi secara keseluruhan saat ingin memodifikasi `printCatEmojis()`.

### Superglobals

*Superglobals* adalah sejumlah *variable* standard bawaan PHP yang dapat diakses di dalam semua *scope*.

* [`$GLOBALS`](https://secure.php.net/manual/en/reserved.variables.globals.php): berisi *variable* yang dideklarasikan dalam *global scope*.
* [`$_SERVERS`](https://secure.php.net/manual/en/reserved.variables.server.php): berisi informasi mengenai *server* dan *environment* dimana file PHP tersebut dieksekusi.
* [`$_GET`](https://secure.php.net/manual/en/reserved.variables.get.php): berisi parameter URL.
* [`$_POST`](https://secure.php.net/manual/en/reserved.variables.post.php): berisi parameter yang dikirim dengan metode HTTP POST.
* [`$_FILES`](https://secure.php.net/manual/en/reserved.variables.files.php): berisi *file-file* yang diunggah dengan metode HTTP POST.
* [`$_REQUEST`](https://secure.php.net/manual/en/reserved.variables.request.php): berisi data-data dari HTTP *request*, gabungan data dari `$_GET`, `$_POST` dan `$_COOKIES`.
* [`$_SESSION`](https://secure.php.net/manual/en/reserved.variables.session.php): berisi semua *variable session*.
* [`$_ENV`](https://secure.php.net/manual/en/reserved.variables.environment.php): berisi *environment variable*.
* [`$_COOKIES`](https://secure.php.net/manual/en/reserved.variables.cookies.php): berisi *variable-variable* untuk HTTP *cookies*.

Untuk saat ini kita tidak perlu memusingkan sejumlah *superglobals* di atas.

### Latihan Variable

Sebagai latihan, buatlah *file* baru dengan nama `04_variables.php`. Coba tikan dan pahami kode berikut:

```php
<?php

function printR2D2()
{
    $name = 'R2-D2';
    global $R2_D2_Price;

    echo "🤖 $name voice: {$GLOBALS['R2_D2_Voice']} price: \$$R2_D2_Price<br>";
}

$R2_D2_Voice = 'Grrr Grrr Grrr...';
$R2_D2_Price = 100;
printR2D2(); // 🤖 R2-D2 voice: Grrr Grrr Grrr... price: $100

$R2_D2_Voice = 'Beep boop baap...';
$R2_D2_Price = 2500.75;
printR2D2(); // 🤖 R2-D2 voice: Beep boop baap... price: $2500.75
```

Perhatikan karakter apa saja yang valid untuk sebuah nama *variable* di dalam PHP. Cermati juga bagaimana dua cakupan *variable* dalam PHP bekerja.

### Rangkuman Variable

Dari subbab ini kita bisa simpulkan beberapa hal:

1. *Variable* digunakan untuk menyimpan sebuah informasi atau data.
2. Nama dari sebuah *variable* hanya boleh terdiri dari huruf, angka dan *underscore*. Pun begitu nama *variable* tidak boleh didahului dengan angka.
3. Berikanlah nama *variable* yang deskriptif. Lebih baik nama *variable* yang panjang tapi mudah dipahami tujuannya daripada nama *variable* yang pendek namun sulit dipahami fungsinya.
4. Dalam PHP ada dua jenis cakupkan *variable*: *local scope* dan *global scope*. *Variable* yang dideklarasikan di dalam sebuah fungsi atau metode memiliki *local scope*. Sebaliknya *variable* di luar fungsi atau metode tergolong ke dalam *global scope*.
5. Untuk mengakses *variable global* di dalam sebuah fungsi atau metode, kita bisa menggunakan *keyword* `global` atau dengan memanfaatkan *variable* `$_GLOBALS`.
6. Mengandalkan *variable global* di dalam sebuah fungsi atau metode dianggap sebagai praktik yang buruk. Praktik ini membuat kode di dalamnya bergantung pada kondisi di luar cakupannya.

## Konstanta dalam PHP

Bahasa PHP juga menyediakan *constant* atau konstanta. Berbeda dengan *variable*, nilai dari konstanta tidak bisa diubah. Dalam PHP, konstanta dideklarasikan dengan menggunakan perintah `define`. Aturan penamaannya pun sama seperti *variable*:

* Nama konstanta bisa terdiri dari: huruf, angka, atau *underscore*.
* Nama konstanta boleh diawali dengan huruf atau *underscore*, tapi tidak boleh didahului oleh angka.

```php
define('MESSAGE', 'Help me, Obi-Wan Kenobi.');
echo MESSAGE;

define('r2_d2_weight', 100);
echo r2_d2_weight;

define('_POOP', '💩');
echo _POOP;
```

Selain menggunakan `define`, kita juga bisa mendeklarasikan konstanta dengan *keyword*: `const`.

```php
const MESSAGE = 'Help me, Obi-Wan Kenobi.';

echo MESSAGE;
```

> 🎨 **Gunakan huruf besar dan snake-case untuk konstanta**
>
> Meski diperbolehkan untuk  menggunakan huruf kecil, banyak *developer* PHP yang sepakat untuk selalu menggunakan huruf besar dengan gaya *snake case* untuk penamaan konstanta (contoh: `DATABASE_NAME`). Ini sejalan dengan aturan [PSR-1](https://www.php-fig.org/psr/psr-1/#41-constants) tentang penulisan nama konstanta di dalam sebuah kelas.

### Cakupan Konstanta

Konstanta memiliki cakupan seperti [*Superglobals*](#superglobals), ia dapat diakses dari *global* dan *local scope*.

```php
define('CAT_EMOJIS', '😸😹😻😽');;

function printCatEmojis()
{
    echo CAT_EMOJIS;
}

printCatEmojis();
```

### Tipe Data untuk Konstanta

Pada PHP versi 5, nilai dari konstanta yang dideklarasikan dengan perintah `define` harus bertipe [skalar](#tipe-data-skalar) (`boolean`, `integer`, `float`, dan `string`) atau [`NULL`](#null). Semenjak PHP versi 7, kita juga bisa menggunakan tipe data [*array*](#array).

```php
define('IS_AWESOME', true);
define('MAXIMUM_POWER', 100);
define('PI', 3.14);
define('DATABASE_NAME', 'death_star');

// PHP versi 7.
define('JEDI', ['Yoda', 'Windu', 'Kenobi']);
```

Sementara untuk *keyword* *const*, kita bisa menggunakan tipe data *array* sejak PHP versi 5.6:

```php
const IS_AWESOME = true;
const MAXIMUM_POWER = 100;
const PI = 3.14;
const DATABASE_NAME = 'death_star';

// Sejak PHP versi 5.6
const JEDI = ['Yoda', 'Windu', 'Kenobi'];
```

### Case-Sensitivity pada Konstanta

Secara *default*, konstanta yang dideklarasikan dengan perintah `define` bersifat *case-sensitive*. `PI` dan `pi` pada contoh kode berikut merupakan dua konstanta yang berbeda:

```php
define('PI', 3.14);
define('pi', 3.14159);

echo PI; // 3.14
echo pi; // 3.14159
```

Pun begitu, kita bisa mengatur agar konstanta yang dideklarasikan bersifat *case-insensitive* dengan memberikan nilai `true` sebagai argumen ketiga dari `define`:

```php
define('PI', 3.14, true);

echo PI; // 3.14
echo pi; // 3.14
```

Sementara konstanta yang dideklarasikan dengan *keyword* *const* selalu bersifat *case-sensitive*.

```php
const PI = 3.14;

echo PI; // 3.14
echo pi; // Pesan kesalahan: Notice: Use of undefined constant pi
```

### Predefined & Magic Constants

PHP dan beragam ekstensinya menyediakan sejumlah konstanta yang bisa kita gunakan. Berikut beberapa contoh konstanta yang disediakan oleh *core* PHP:

| Constant      | Deskripsi                                      |
| ------------- |----------------------------------------------- |
| `PHP_VERSION` | Versi PHP yang digunakan                       |
| `PHP_OS`      | Sistem operasi yang ditargetkan oleh PHP       |
| `PHP_SAPI`    | *Server* API yang digunakan                    |
| `PHP_INT_MAX` | Nilai maksimum dari *integer*                  |
| `E_ERROR`     | Untuk *fatal run-time error*                   |
| `E_WARNING`   | Untuk *run-time warning*                       |
| `E_PARSE`     | Untuk *compile-time parse error*               |
| `E_ALL`       | Untuk mengaktifkan semua *error* dan *warning* |
| `true`        | Cek subbab [`boolean`](#boolean)               |
| `false`       | Cek subbab [`boolean`](#boolean)               |
| `null`        | Cek subbab [`null`](#null)                     |

Cek daftar konstanta yang disediakan oleh *core* PHP di dokumentasi: [Core Predefined Constants](https://secure.php.net/manual/en/reserved.constants.php#reserved.constants.core).

> 💡 Dalam PHP, nilai `true`, `false`, dan `null` merupakan konstanta dan penulisannya *case-insenstive* (`true` dan `TRUE` adalah konstanta yang sama).

PHP juga memiliki beberapa *magic constant*—konstanta yang nilainya berganti tergantung dimana ia digunakan.

| Constant       | Deskripsi                                        |
| -------------- |------------------------------------------------- |
| `__DIR__`      | Lokasi direktori dari *file* PHP yang dieksekusi |
| `__FILE__`     | Lokasi dari *file* PHP yang dieksekusi           |
| `__FUNCTION__` | Nama fungsi dimana fungsi dipanggil              |
| `__CLASS__`    | Nama kelas dimana konstanta dipanggil            |

Cek daftar *magic constant* lainnya di dokumentasi PHP: [Magic Constants](https://secure.php.net/manual/en/language.constants.predefined.php).

### Latihan Konstanta

Sebagai latihan buat *file* baru dengan nama `05_constants.php`. Tikan kode berikut dan perhatikan bagaimana kita bisa mendeklarasikan konstanta dalam PHP:

```php
<?php

define('IS_ACTIVE', true);
define('MAXIMUM_FAILED_ATTEMPTS', 3);
define('PI', 3.14159);
define('GOOGLE_URL', 'https://google.com');
define('COLORS', ['red', 'green', 'blue']);

const FAILED_STATUS = false;
const MINIMUM_BALANCE = -10;
const MINIMUM_PURCHASE = 25.5;
const DUCKDUCKGO_URL = 'https://duckduckgo.com';
const EVEN_NUMBERS = [2, 4, 6, 8];

echo PHP_VERSION; // 7.2.4
echo __FILE__; // /path/to/05_constants.php
```

### Rangkuman Konstanta

Berikut beberapa poin yang bisa kita simpulkan dari subbab ini:

* Berbeda dengan *variable*, nilai dari konstanta tidak bisa diubah.
* Dalam PHP konstanta bisa dideklarasikan dengan perintah `define` atau *keyword* `const`.
* Nama konstanta dapat terdiri dari huruf, angka, atay *underscore*. Pun begitu nama konstanta tidak boleh diawali dengan angka.
* Dianjurkan untuk menggunakan huruf besar dengan gaya *snake case* untuk penulisan konstanta.
* Konstanta memiliki cakupan seperti [*superglobals*](#superglobals), ia bisa diakses dari *global scope* ataupun *local scope*.
* Secara *default* nama konstanta bersifat *case-sensitive*, namun kita bisa mengubahnya menjadi *case-insensitive* dengan memberikan nilai `true` sebagai argumen ketiga dari perintah `define`.
* `true`, `false`, dan `null` merupakan salah satu konstanta yang disediakan *core* PHP.
