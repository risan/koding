

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
