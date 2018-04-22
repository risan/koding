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
