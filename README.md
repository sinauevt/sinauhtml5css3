# Sinau HTML 5, CSS 3 & Javascript #

Untuk membuat aplikasi berbasis web kita membutuhkan seperangkat teknologi yang dapat berjalan di web browser. Mengapa web browser? ya karena aplikasi web memang jalannya di web browser.

Aplikasi web biasanya terdiri dari 2 bagian, yaitu frontend dan backend. Frontend adalah bagian dimana user melakukan interaksi dengan aplikasi (atau biasa disebut User Interface). Sedangkan backend adalah tempat pemrosesan atau logical process aplikasi berjalan dan juga tempat dimana data-data disimpan.

Dibagian frontend, teknologi yang terlibat disini adalah HTML, CSS dan Javascript.

Sedangkan backend ada banyak sekali teknologi yang dapat kita gunakan, seperti: Java, PHP, Ruby, Python, .NET, MySQL, MongoDB, dll.

Jadi lazimnya untuk membuat satu aplikasi web secara utuh paling tidak kita membutuhkan sedikitnya 5 hal: HTML, CSS, Javascript, Java dan MySQL (komposisi ini bisa diganti dengan yang lain tergantung dari teknologi apa yang akan kita gunakan).

Namun untuk pembahasan kali ini kita hanya akan fokus pada bagian frontend, yaitu HTML, CSS dan Javascript.

Untuk user interface saja mengapa banyak sekali yang harus dipelajari (HTML, CSS, Javascript)? Diibaratkan membangun sebuah rumah HTML adalah pondasi dasarnya atau diibaratkan sebuah rumah yang baru tersusun dari batu bata dan belum memiliki tembok. CSS adalah tampilan atau styling yang memperindah supaya menarik perhatian orang yang akan membeli rumah tersebut. CSS inilah yang akan menentukan apakah rumah tersebut berwarna biru, hijau atau yang lain, apakah rumah tersebut dihiasi dengan taman yang menarik, punya ventilasi yang cukup, ini semua diatur oleh CSS. Sedangkan Javascript mengatur behaviour, yang akan membuat rumah tersebut terasa canggih, misal kalau ada seseorang masuk ke dalam rumah akan ada alarm otomatis yang mengucapkan selamat datang, atau lampu taman yang akan hidup otomatis setiap jam 6 sore dan mati otomatis setiap jam 6 pagi.

Sepertinya menarik ya, mari kita lihat satu persatu.

## HTML ##

HTML adalah kepanjangan dari HyperText Markup Language, sebuah bahasa standar untuk membuat tampilan website. Website ini secara naturalnya jalan di web browser seperti: chrome, firefox, opera, safari, internet explorer, dll.

Jadi sebelum mulai ngoding html pastikan kita telah memiliki web browser, supaya bisa kita lihat hasil dari kodingan kita. Untuk tools editornya kita bisa menggunakan tools apa saja yang paling nyaman dan biasa kita gunakan, tidak ada kriteria khusus untuk tools ini, text editor biasa sebenarnya sudah cukup.

> Kalau ingin sesuatu yang beda silahkan coba tools editor yang ringan, banyak dipake dan free, seperti: **atom, bracket dan visualstudio code**.

Versi yang terbaru dari HTML adalah HTML5. Diversi yang terbaru ini terdapat tag-tag tambahan yang tidak didukung oleh versi sebelumnya. Apa sajakah itu?

| Fitur         | Deskripsi                                      |
|:--------------|:-----------------------------------------------|
| Audio & Video | Untuk meng-embed video & audio                 |
| Canvas        | Untuk keperluan grafis                         |
| Media Queries | Fitur CSS3 untuk mendeteksi ukuran layar       |
| New API       | Menyediakan akses ke berbagai resource digital |
| Geolocation   | Untuk mendeteksi lokasi                        |

HTML merupakan sebuah bahasa dimana syntax-syntaxnya menggunakan tag. Tag ini ditandai dengan simbol `<>`. Tag didalam HTML biasanya sepasang, ada tag pembuka dan ada tag penutup, tapi ada juga tag-tag tertentu yang tidak perlu tag penutup khusus. Bingung ya? Langsung saja kita coba.

```xml
<!DOCTYPE html>
<html>
    <head>
    	<title>Belajar HTML</title>
    </head>
    <body>
    	Hello world
    </body>
</html>
```

Bentuk dasar html kira-kira seperti contoh diatas. Diawali dengan tag html diakhiri dengan tag html juga ditengah-tengahnya ada head dan body.

Head merupakan tempat untuk menaruh hal-hal teknis, tapi biasanya 3 hal ini yang ditaruh di head: css, javascript, title.

Body tempat untuk meletakkan baris-baris kode yang sesungguhnya. Semua yang ada didalam body inilah yang mencerminkan komponen-komponen html apa saja yang akan ditampilkan ke browser.

> **Tag-tag html wajib diletakkan pada posisinya**. Seperti tag title yang posisinya berada didalam tag head. Kalau kita meletakkan misal tag title diluar tag head pasti akan kena error. Ini adalah aturan dasar dari html.

Berikut adalah daftar tag-tag umum yang sering digunakan.

| Tag              | Deskripsi                                    |
|:-----------------|:---------------------------------------------|
| `<html>`         | Tag pembuka dari dokumen html                |
| `<head>`         | Tempat meletakkan baris kode css atau script |
| `<title>`        | Judul halaman                                |
| `<body>`         | Konten dari halaman html                     |
| `<p>`            | Paragraf                                     |
| `<a href="url">` | Link                                         |
| `<h1>`           | Heading dengan ukuran paling besar           |
| `<img>`          | gambar                                       |

### Atribut ###

Tag HTML biasanya memiliki atribut sebagai pelengkap atau informasi tambahan. Sebagai contoh adalah sebagai berikut: `<a href="http://www.sinauacademy.com/"> Sinau </a>`. `<a>` merupakan tag, `href` merupakan atribut pelengkap dari tag `a` dimana berisi value berupa url tempat diarahkannya link tersebut, dan berisikan text berupa `Sinau`. Ketika dirender akan menampilkan tulisan `Sinau`, dimana ketika tulisan tersebut diklik akan mengarah ke alamat `http://www.sinauacademy.com/`.

### Nesting ###

Ketika membuat tampilan yang kompleks, kita dituntut untuk dapat mengkombinasikan antar elemen. Didalam mengkombinasikan ini terkadang kita melakukan nesting. Nesting merupakan menempatkan elemen didalam elemen yang lain sebagai sebuah kombinasi.

```xml
<p>Selamat datang <em>pengguna</em> disitus kami.</p>
```

### Karakter Khusus ###

Beberapa karakter tidak dapat langsung ditampilkan dihalaman HTML dan untuk menampilkannya membutuhkan encoding. Beberapa diantaranya adalah sebagai berikut.

| Karakter | Deskripsi     | Entity     | Kode    |
|:---------|:--------------|:-----------|:--------|
| $        | Simbol dollar | `&dollar;` | `&#36;` |
| %        | Simbol persen | `&percnt;` | `&#37;` |
| &        | Simbol dan    | `&amp;`    | `&#38;` |

### Doctype ###

Doctype membantu browser untuk menentukan aturan mana yang digunakan untuk me-render tampilan. Di HTML versi 4 penulisan doctype sangatlah rumit, sedangkan di HTML 5 menjadi lebih sederhana.

```xml
<!DOCTYPE html>
```

Contoh lengkapnya seperti dibawah ini.

```xml
<!DOCTYPE html>
<html>
    <head>
    	<meta charset="utf-8"/>
    	<title>Belajar HTML</title>
    </head>
    <body>
    	<h1> ini adalah header </h1>
    	<p> ini adalah paragraf <p>
    </body>
</html>
```

### Elemen Text ###

Text yang kita tampilkan dapat kita manipulasi bentuknya. Dibawah ini adalah tag-tag untuk memanipulasi bentuk text yang akan ditampilkan.

| Elemen Text | Fungsi                         |
|:------------|:-------------------------------|
| `<b>`       | Cetak huruf tebal              |
| `<em>`      | Cetak huruf miring             |
| `<i>`       | Cetak huruf miring             |
| `<small>`   | Cetak huruf kecil              |
| `<strong>`  | Cetak huruf penting            |
| `<sub">`    | Subscript                      |
| `<sup>`     | Superscript                    |
| `<code>`    | Tampilkan kode komputer        |
| `<samp>`    | Sample output program komputer |
| `<del>`     | Pengganti strike di HTML 4     |
| `<abbr>`    | Pengganti acronym di HTML 4    |
| `<ul>`      | Pengganti dir di HTML 4        |

### Elemen Gambar ###

Gambar merupakan elemen yang sangat penting dari halaman HTML. Untuk menampilkan gambar kita dapat menggunakan tag `<img/>`.

```xml
<img src="sumbergambar.jpg" alt="text alternatif untuk penyandang disabilitas" title="judul gambar" />
```

Kita dapat mengatur lebar dan tinggi gambar dengan menambahkan atribut width dan height.

Ada 2 tag baru yang dapat digunakan yang berhubungan dengan gambar, yaitu `<figure>` untuk mengorganisasikan gambar dan `<figcaption>` untuk memberikan caption pada gambar.

```xml
  <figure>
    <figcaption>contoh menampilkan gambar</figcaption>
    <img src="startup.jpg" alt="startup" title="startup" height="300" width="600"/>
    <img src="The-Iceberg-Ilussion.jpg" alt="iceberg" title="iceberg"/>
  </figure>
```

### Canvas ###

Canvas nerupakan tag baru di HTML 5 dan digunakan sebagai container grafis. Kita dapat menggambar didalamnya menggunakan Javascript dan Canvas API. Canvas biasanya digunakan untuk membuat game 2D atau animasi.

```xml
<canvas id="cobaCanvas" width="500px" height="300px"></canvas>
```

### Media ###

Dulu untuk memainkan video dan audio, browser sangat bergantung pada plugin dan media player. Sekarang pada HTML 5 fitur audio dan video sudah didukung secara langsung dengan menggunakan tag `<audio>` dan `<video>`.

#### Video ####

Untuk memainkan video kita dapat menggunakan tag `<video>` seperti pada contoh dibawah.

```xml
<video src="sample.mp4" height="300" width="400"></video>
```

#### Atribut Video Control ####

Ada beberapa atribut yang dapat digunakan supaya user dapat mengontrol video yang sedang dijalankan.

| Atribut  | Fungsi                                                     |
|:---------|:-----------------------------------------------------------|
| poster   | Tampilkan gambar sebelum video dimainkan                   |
| autoplay | Mainkan video otomatis saat halaman diload                 |
| controls | Tampilkan video control untuk volume, play, pause dan stop |
| loop     | Mainkan video secara berulang                              |

#### Format Video ####

Banyak format video yang sudah didukung oleh web browser, diantaranya MP4, H.264, OGG dan WebM.

Ketika kita mendefinisikan secara spesifik format video apa yang dimainkan, kita juga harus memberikan secara spesifik **codec** apa yang akan digunakan.

Kita juga dapat memasang multiple format untuk memastikan bahwa video yang dimainkan didukung oleh browser pengguna. Karena tidak semua format didukung oleh semua browser.

```xml
<video height="300" width="400" poster="sample.jpg" autoplay="autoplay" controls="controls" loop="loop">
	<source src="sample.mp4" type="video/mp4"/>
    <source src="sample.ogg" type='video/ogg; codecs="theora, vorbis"'/>
</video>
```

#### Audio ####

Untuk memainkan audio kita dapat menggunakan tag `<audio>`.

```xml
<audio src="sample.mp3" controls="controls"></audio>
```

#### Atribut Video Control ####

Mirip dengan tag video, ada beberapa atribut yang dapat digunakan supaya user dapat mengontrol audio yang sedang dijalankan.

| Atribut  | Fungsi                                                     |
|:---------|:-----------------------------------------------------------|
| autoplay | Mainkan audio otomatis saat halaman diload                 |
| controls | Tampilkan audio control untuk volume, play, pause dan stop |
| loop     | Mainkan audio secara berulang                              |

#### Format Audio ####

Ada tiga format dasar yang didukung oleh browser termasuk diantaranya: MP3, OGG dan WAV. Sama halnya dengan video, tidak semua browser mendukung semua format audio.

Kita dapat memasang multiple format untuk memastikan audio yang dipasang didukung oleh browser pengguna.

```xml
<audio controls>
	<source src="sample.mp3" type="audio/mp3"/>
    <source src="sample.ogg" type="audio/ogg"/>
</audio>
```

### Tag-Tag HTML ###

#### Paragraf ####

HTML menyediakan tag khusus untuk membuat paragraf. Penulisannya menggunakan huruf p, sebagai berikut : `<p>`.

```html
<!DOCTYPE html>
<html>
<head>
  <title>title dari websiteku</title>
</head>
<body>
  <p>ini adalah paragraf pertama</p>
  <p>ini adalah paragraf kedua</p>
</body>
</html>
```

#### Break ####

Cara lain untuk memisahkan kedua paragraf adalah dengan menggunakan tag `<br>` (br singkatan dari break).

```html
<!DOCTYPE html>
<html>
<head>
  <title>title dari websiteku</title>
</head>
<body>
  ini adalah paragraf pertama
  <br />
  ini adalah paragraf kedua
</body>
</html>
```

#### Em dan Strong ####

Di dalam sebuah paragraf, kadang kita perlu untuk membuat penekanan pada kata-kata tertentu. Penekanan ini bisa dilakukan dengan menebalkan kata, atau dengan garis miring.

Tag emphasis (penekanan) terdiri dari 2 tag, `<em>` untuk emphasis, dan `<strong>` untuk strong emphasis.

Pada umumnya web browser akan menampilkan `<em>` sebagai garis miring, dan `<strong>` dengan penebalan huruf.

```html
<!DOCTYPE html>
<html>
<head>
  <title>title dari websiteku</title>
</head>
<body>
  <p>ini adalah kalimat <em>pertama</em>, 
  sedangkan ini adalah kalimat <strong>kedua</strong></p>
</body>
</html>
```

#### Judul atau Heading ####

Tag heading di dalam HTML terdiri dari 6 tingkatan, yaitu `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, dan `<h6>`. Tag heading secara default akan ditampilkan oleh web browser dengan huruf tebal (bold). Tampilan dari tag header juga dibuat bertingkat. Tag header `<h1>` memiliki ukuran huruf paling besar, sedangkan `<h6>` terkecil.

```html
<!DOCTYPE html>
<html>
<head>
  <title>penggunaan tag heading</title>
</head>
<body>
  <h1>ini adalah judul dengan h1 </h1>
  <h2>ini adalah judul dengan h2 </h2>
  <h3>ini adalah judul dengan h3 </h3>
  <h4>ini adalah judul dengan h4 </h4>
  <h5>ini adalah judul dengan h5 </h5>
  <h6>ini adalah judul dengan h6 </h6>
</body>
</html>
```

Biasanya dalam sebuah halaman akan ada hanya 1 tag `<h1>`, dan beberapa tag `<h2>` dan `<h3>` dengan beberapa tag `<p>`. Berikut adalah contoh struktur artikel HTML sederhana dengan menggunakan tag `<p>` dan beberapa tag heading.

```html
<body>
  <h1>Judul Artikel</h1>
  <p>.....pembahasan artikel.....</p>
    <h2>Sub Judul Artikel 1</h2>
    <p>.....pembahasan sub artikel 1.....</p>
    <h2>Sub Judul Artikel 2</h2>
    <p>.....pembahasan sub artikel 2.1.....</p>
      <h2>Sub Sub Judul Artikel 2.1</h2>
      <p>.....pembahasan sub sub artikel 2.1.....</p>
</body>
```

Search Engine seperti Google akan memberikan nilai lebih untuk heading. Biasanya semakin tinggi tingkat heading, semakin tinggi pula penekanan search engine. Tag `<h1>` dianggap lebih bernilai dari pada `<h2>`. Tag `<h1>` umumnya digunakan untuk judul sebuah konten / artikel, sehingga dianggap dapat mewakili keseluruhan artikel.

#### List ####

Dalam HTML, tag list terdiri dari 2 jenis, ordered list (berurutan) dan unordered list (tidak berurutan). Ordered list akan ditampilkan dengan angka atau huruf, sedangkan unordered list dengan bulatan atau kotak.

Ordered list menggunakan tag `<ol>`, dan unordered list menggunakan tag `<ul>`, sedangkan untuk list sendiri menggunakan tag `<li>`.

```html
<!DOCTYPE html>
<html>
<head>
  <title>penggunaan tag list </title>
</head>
<body>
  <h1>daftar belanjaan</h1>
  <ol>
  <li>minyak goreng</li>
    <li>sabun mandi</li>
    <li>deterjen</li>
    <li>shampoo</li>
    <li>obat nyamuk</li>
  </ol>
</body>
</html>
```

```html
<!DOCTYPE html>
<html>
<head>
  <title>penggunaan tag list </title>
</head>
<body>
  <h1>daftar belanjaan</h1>
  <ul>
    <li>minyak goreng</li>
    <li>sabun mandi</li>
    <li>deterjen</li>
    <li>shampoo</li>
    <li>obat nyamuk</li>
  </ul>
</body>
</html>
```

#### Link ####

Link ditulis dengan `<a>` yang merupakan singkatan cari anchor (jangkar). Setiap tag `<a>` setidaknya memiliki sebuah atribut href. Dimana href berisi alamat yang dituju (href adalah singkatan dari hypertext reference).

```html
<!DOCTYPE html>
<html>
<head>
  <title>Penggunaan Tag Link </title>
</head>
<body>
  <h1>Belajar Tag Link</h1>
  <p>Saya sedang belajar HTML dari
  <a href="http://www.belajaraja.org">Belajar</a></p>
</body>
</html>
```

Atribut penting lainnya dari tag `<a>` adalah target. Atribut ini digunakan untuk menentukan apakah link yang dituju terbuka di jendela browser saat ini, atau terbuka di jendela baru.

Secara default, setiap link yang kita tulis akan terbuka pada jendela yang sama (menimpa halaman web saat ini). Tetapi apabila kita ingin halaman tersebut terbuka pada tab baru, gunakan atribut `target=”_blank”`.

#### Image atau Gambar ####

Tag Image digunakan untuk menampilkan gambar kedalam halaman web, menggunakan `<img>`. Tag img memiliki atribut src yang merupakan singkatan dari source, merupakan atribut yang berisi alamat dari gambar yang akan ditampilkan.

```html
<!DOCTYPE html>
<html>
<head>
   <title>Penggunaan Tag Image</title>
</head>
<body>
   <h1>Belajar Tag Gambar</h1>
   <img src="The-Iceberg-Ilussion.jpg" alt="gambar ilustrasi" />
</body>
</html>
```

Tag image juga memiliki atribut penting lainnya, yaitu alt.

Atribut alt adalah singkatan dari alternative description, dimana alt digunakan untuk keterangan dari gambar jika gambar tersebut gagal ditampilkan oleh browser. Atau jika web broser telah disetting untuk tidak menampilkan gambar.

Atribut lainnya membolehkan kita untuk menentukan besar dari gambar yang ditampilkan, yaitu width dan height.

`height="200" width="100"`.

#### Komentar ####

Untuk membuat komentar di HTML, kita menggunakan awalan <!–- dan penutup -–>.

```html
<!DOCTYPE html >
<html>
<head>
   <title>Belajar Tag Komentar (comment)</title>
</head>
<body>
   <!-- <p>Ini berada di dalam tag komentar,
           dan tidak akan tampil di browser</p> -->
   <p>Ini bukan komentar, dan akan tampil di browser</p>
</body>
</html>
```

#### Div ####

Tag div atau kepanjangan dari division, merupakan tag yang umum digunakan dan biasanya digunakan untuk membagi halaman menjadi beberapa bagian yang akan ditujukan untuk konten tertentu.

#### Table ####

Untuk menampilkan table kita dapat menggunakan tag `<table>` dengan kombinasi didalamnya.

```xml
<table broder="1">
	<tr>
    	<th>Bulan</th>
        <th>Nama</th>
    </tr>
    <tr>
    	<td>1</td>
        <td>Januari</td>
    </tr>
    <tr>
    	<td>2</td>
        <td>Februari</td>
    </tr>
</table>
```

#### Input dan Form ####

Form digunakan untuk men-submit data, seperti saat mendaftarkan email atau register baru pada sebuah web.

```xml
<form id="contact" method="post" action="">
	<label for="firstName">First Name</label>
    <input type="text" name="firstName"/> <br/>
    <label for="lastName">Last Name</label>
    <input type="text" name="lastName"/> <br/>
</form>
```

#### Macam-Macam Input ####

| Input Type | Deskripsi      |
|:-----------|:---------------|
| text       | text field     |
| password   | password field |
| submit     | button submit  |
| radio      | radio button   |
| checkbox   | checkbox field |
| date       | date field     |
| email      | email field    |
| search     | search field   |

#### Atribut Input ####

Ada beberapa atribut yang dapat digunakan didalam elemen input.

| Input Atribut | Deskripsi                                                  |
|:--------------|:-----------------------------------------------------------|
| autofocus     | untuk menunjuk fokus ke input tertentu saat halaman diload |
| required      | untuk menandai input yang mandatory                        |
| placeholder   | untuk memberi text pada input untuk memudahkan pengguna    |

```html
<!DOCTYPE html>
<html>
<head>
   <title>Belajar Membuat Form </title>
</head>
<body>
<form action=" formulir.html" method="get">

Nama: <input type="text" name="nama" value="Nama Kamu" />
<br />

Password: <input type="password" name="password" />
<br />

Jenis Kelamin : 
<input type="radio" name="jenis_kelamin" value="laki-laki" checked /> 
Laki - Laki
<input type="radio" name="jenis_kelamin" value="perempuan" /> 
Perempuan
<br />

Hobi: <input type="checkbox" name="hobi_baca" /> Membaca Buku
      <input type="checkbox" name="hobi_nulis" checked /> Menulis
      <input type="checkbox" name="hobi_mancing" /> Memancing
<br />

Asal Kota:
 <select name="asal_kota" >
     <option value="Kota Jakarta"> Jakarta</option>
     <option>Bandung</option>
    <option value="Kota Semarang" selected>Semarang</option>
 </select>
<br />

Komentar Anda:
<textarea name="komentar" rows="5" cols="20">
Silahkan katakan isi hati anda
</textarea>
<br />

<input type="submit" value="Mulai Proses!" >

</form>
</body>
</html>
```

## CSS ##

CSS kepanjangan dari Casecading Style Sheet, yaitu sebuah bahasa standar yang dapat dimengerti oleh semua web browser yang ditujukan khusus untuk memodifikasi tampilan HTML.

CSS terdiri dari 2 hal: selector dan declaration / deklarasi. Selector memberitahukan ke browser elemen mana yang akan dimodifikasi tampilannya. Contoh dibawah ini akan memodifikasi semua elemen html `p` atau paragraf.

```css
p {font-family: Arial, Helvetica, sans-serif; font-size: 1em;}
```

Deklarasi yang berada didalam tanda kurung kurawal merupakan instruksi format untuk dekorasi tampilan. Contoh diatas memberitahukan ke browser font apa yang digunakan dan berapa ukuran hurufnya. Format dari deklarasi terdiri dari 2 hal: property dan value. `font-family` dan `font-size` pada contoh diatas adalah property, sedangkan `Arial, Helvetica, sans-serif` dan `1em` merupakan value dari property.



### CSS Selector ###

Pada bagian ini kita akan membahas tentang selector. Masih ingatkan selector mengijinkan kita memberitahukan ke browser elemen mana yang akan kita modifikasi tampilannya.

Pada kasus-kasus tertentu kita ingin memodifikasi tampilan pada beberapa elemen sekaligus. Pada kasus yang berbeda mungkin hanya sebagian kecil saja elemen yang ingin kita modifikasi atau mungkin hanya satu elemen saja. Disinilah peran selector sangat membantu dalam hal ini.

Selector secara bahasa berarti pemilih atau yang memilihkan. Seperti artinya selector ini dapat memilihkan untuk kita bagian mana yang akan diperindah tampilannya.

Lalu berdasarkan apa memilihnya? Selector ini sangat fleksibel dalam memilih komponen HTML. Namun secara garis besar selector ini dapat memilih berdasarkan 5 kategori.

- Yang pertama adalah memilih berdasarkan komponen HTML. Contohnya seperti dibawah ini.

    ```css
    p {font-family: Arial, Helvetica, sans-serif; font-size: 1em;}
    ```

- Yang kedua adalah memilih berdasarkan class HTML tertentu. Misalnya kita memiliki tag HTML yang didalamnya memiliki nama class tertentu dan kita ingin hanya class tersebut saja yang akan kita modifikasi dengan CSS.

    ```xml
    <h2 class="subheading">Coba</h2>
    ```

    Selector CSS untuk kasus ini seperti dibawah ini.

    ```css
    .subheading {color: blue;}
```

- Yang ketiga adalah memilih berdasarkan id. Didalam HTML kita dapat memberikan sebuah nama kepada masing-masing komponen, nama ini haruslah unik dan tidak boleh sama disetiap komponennya.

    ```xml
    <div id="sidebar">...content...</div>
    ```

    Kita dapat memilih id tersebut dengan cara dibawah ini.

    ```css
    #sidebar {font-size: 80%;}
```

- Yang keempat adalah element-specific selector. Artinya memilih elemen tertentu yang memiliki class atau id tertentu yang spesifik.

    ```css
    /* pilih semua elemen h2 yang memiliki class subheading */
    h2.subheading {color: blue;}

    /* pilih semua elemen div yang memiliki id sidebar */
    div#sidebar {font-size: 80%;}
    ```

    Yang perlu diingat dari class dan id tersebut bersifat case sensitive dan tidak boleh ada spasi didalam penamaannya.

- Yang kelima adalah memilih berdasarkan turunan. Yaitu memilih elemen berdasarkan lokasi didalam suatu elemen. Membingungkan? Mari kita lihat saja contohnya.

    ```xml
    <html>
    <head></head>
    <body>
    	<div>
        	<p>bla..bla..bla..bla..</p>
            <p>ini adalah contoh <span>turunan</span></p>
            <section>
            	<h1>heading</h1>
                <p>konten</p>
            </section>
        </div>
    </body>
    </html>
    ```

    ```css
    /* apply style ke semua elemen p yang berada didalam div, tidak peduli seberapa dalam dia berada didalam div */
    div p {color: red;}

    /* apply style ke semua elemen span yang berada didalam elemen p yang berada didalam elemen div */
    div p span {color: blue;}
    ```

Kita juga dapat mengelompokkan selector yang memiliki kesamaan.

```css
h1 {font-weight: normal; color: blue;}
h2 {font-weight: normal; color: blue;}
.quote {font-weight: normal; color: blue;}
```

Dikelompokkan menjadi seperti dibawah ini.

```css
h1,h2,.quote {font-weight: normal; color: blue;}
```

### Font ###

Ada kalanya font yang kita gunakan tidak terdapat didalam perangkat pengguna. Untuk mengatasi keterbatasan ini kita dapat memasang defini font kita sendiri yang tidak akan bergantung pada keterbatasan pada perangkat pengguna.

```css
@font-face {
	font-family: "font-family-name";
    src: url(http://web/fonts/fontfile)
}
```

### Input CSS ke HTML ###

#### Metode Inline Style ####

Metode Inline Style adalah cara menginput kode CSS langsung ke dalam tag HTML dengan menggunakan atribut style.

```html
<!DOCTYPE html>
<html>
<head>
     <title>Contoh Inline Style CSS</title>
</head>
   <body>
      <h2 style="background-color:black; color:white" >
         Text ini akan bewarna putih dan background warna hitam
      </h2>
   </body>
</html>
```

Penggunaan tag CSS seperti ini walaupun praktis, namun tidak disarankan, karena kode CSS langsung tergabung dengan HTML, dan tidak memenuhi tujuan dibuatnya CSS agar desain terpisah dengan konten.

#### Metode Internal Style Sheets ####

Metode Internal Style Sheets, atau disebut juga Embedded Style Sheets digunakan untuk memisahkan kode CSS dari tag HTML namun tetap dalam satu halaman HTML. Atribut style yang sebelumnya berada di dalam tag, dikumpulkan pada pada sebuah tag `<style>`. Tag style ini harus berada pada bagian `<head>` dari halaman HTML.

```html
<!DOCTYPE html>
<html>
<head>
    <title>Contoh Inline Style CSS</title>
    <style type="text/css">
        h2 {
        background-color:black;
        color:white;
        }
    </style>
</head>
<body>
    <h2>
        Text ini akan bewarna putih dan background warna hitam
    </h2>
</body>
</html>
```

Contoh metode internal style sheets diatas sudah jauh lebih baik daripada inline style, karena kita sudah memisahkan CSS dari HTML. Seluruh kode CSS akan berada pada tag head dari HTML.

Namun kekurangan menggunakan  internal style sheets, jika kita memiliki beberapa halaman dengan style yang sama, maka kita harus membuat kode CSS pada masing-masing halaman tersebut. Hal ini dapat diatasi dengan menggunakan metode external style sheets.

#### Metode External Style Sheets ####

Metode External Style Sheets digunakan untuk ‘mengangkat’ kode CSS tersebut kedalam sebuah file tersendiri yang terpisah sepenuhnya dari halaman HTML. Setiap halaman yang membutuhkan kode CSS, tinggal ‘memanggil’ file CSS tersebut.

Masih menggunakan contoh yang sama dengan internal style sheets, tahap pertama kita akan pindahkan isi dari tag `<style>` ke sebuah halaman baru, dan savelah sebagai belajar.css.

```css
h2 {
background-color:black;
color:white;
}
```

Kembali kehalaman HTML, CSS menyediakan 2 cara untuk menginput Kode CSS tersebut ke halaman HTML, yang pertama adalah menggunakan `@import`.

```html
<!DOCTYPE html>
<html>
<head>
    <title>Contoh Inline Style CSS</title>
    <style type="text/css">
        @import url(belajar.css);
    </style>
</head>
<body>
    <h2>
        Text ini akan bewarna putih dan background warna hitam
    </h2>
</body>
</html>
```

Cara input kedua external style sheets, adalah menggunakan tag `<link>`.

```html
<!DOCTYPE html>
<html>
<head>
    <title>Contoh Inline Style CSS</title>
    <link rel="stylesheet" type="text/css" href="belajar.css">
</head>
<body>
    <h2>
        Text ini akan bewarna putih dan background warna hitam
    </h2>
</body>
</html>
```

### CSS Framework ###

CSS framework merupakan library CSS yang telah dibuat untuk memudahkan dalam mendesain suatu halaman. Dengan menggunakan framework diharapkan akan membuat pekerjaan menjadi lebih mudah dan cepat.

Akhir-akhir ini sering kita dengar tentang responsive web design, artinya tampilan web yang responsif yang tetap nyaman saat dibuka di desktop, tablet maupun mobile device. Dan framework yang menawarkan responsive web design inilah yang sering dipakai oleh kebanyakan orang. Diantara yang cukup populer adalah [materializecss](http://materializecss.com) dan [bootstrap](http://getbootstrap.com).

## JavaScript ##

Javascript merupakan scripting language yang berjalan diatas browser. Bahasa Javascript ini sedikit banyak dipengaruhi oleh Java dan syntax bahasanya pun juga mirip dengan Java, akan tetapi Javascript tidak sama dengan Java. Java berjalan diatas runtime / JDK sedangkan Javascript tidak memerlukan compiler atau runtime.

Javascript biasanya sangat diperlukan dalam pembuatan tampilan web, karena dengan adanya Javascript akan membuat web kita menjadi lebih interaktif.

JavaScript adalah bahasa pemrograman web yang bersifat Client Side Programming Language. Client Side Programming Language adalah tipe bahasa pemrograman yang pemrosesannya dilakukan oleh client. Aplikasi client yang dimaksud merujuk kepada web browser seperti Google Chrome dan Mozilla Firefox.

Jenis bahasa pemrograman Client Side berbeda dengan bahasa pemrograman Server Side seperti PHP, dimana untuk server side seluruh kode program dijalankan di sisi server.

### Hello World ###

```xml
<!DOCTYPE html>
<html>
<head>
  <title> Belajar JavaScript </title>
</head>
<body>
  Belajar Javascript
  <script src='belajarjavascript.js'></script>
</body>
</html>
```

```js
alert("Hello World");
```

```xml
<!DOCTYPE html>
<html>
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
<head>
<title>Belajar JavaScript</title>
</head>

<body>
<h1>Belajar JavaScript</h1>

<button onclick="alert('Hello World!!')">Klik Saya

</body>
</html>
```

### Menampilkan Output ###

Tidak seperti bahasa pemograman PHP yang memiliki perintah echo atau print untuk menampilkan hasil program ke dalam web browser, JavaScript tidak menyediakan perintah sederhana untuk menampilkan hasil program ke dalam web browser. Dalam JavaScript, kita membutuhkan beberapa langkah yang agak panjang jika ingin menampilkan hasil ke dalam web browser.

Pertama, kita harus membuat sebuah tag ‘container’, atau tag penampung untuk hasil program JavaScript. Tag container ini bisa berupa tag HTML apapun, seperti tag paragraf `<p>` atau tag `<div>`.

Kedua, kita harus mencari elemen ‘container’ ini dari JavaScript. JavaScript menyediakan beberapa cara untuk mengakses elemen dalam HTML. Salah satu caranya adalah dengan menggunakan fungsi (atau lebih tepatnya: method): `document.getElementById("id_continer")`. Fungsi getElementById akan mencari elemen HTML yang memiliki atribut id yang diinputkan di dalam tanda kurung.

Langkah ketiga, adalah menginputkan hasil program kedalam tag ‘container’ dengan menggunakan properti innerHTML.

```xml
<!DOCTYPE html>
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
<title>Belajar JavaScript</title>

<script>
window.onload = function()
{
   var hasil;
   hasil = 1+3+5+7+9;
   document.getElementById("tempat_hasil").innerHTML=hasil;
}
</script>

</head>

<body>
<h1>Belajar JavaScript</h1>
<div id="tempat_hasil">
</div>
</body>
</html>
```

Kita juga dapat menggunakan 'alert' untuk menampilkan output.

```xml
<!DOCTYPE html>
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
<title>Belajar JavaScript</title>

<script>
window.onload = function()
{
   var hasil;
   hasil = 1+3+5+7+9;
   alert(hasil);
}
</script>

</head>
<body>
<h1>Belajar JavaScript</h1>
</body>
</html>
```

Web browser yang modern biasanya menyediakan sebuah alat canggih yang disebut 'developer tools'. Alat ini berguna untuk mencari error pada javascript yang telah kita buat. Didalamnya juga terdapat sebuah console yang berguna untuk menampilkan log. Log ini bisa kita gunakan untuk menampilkan output.

```xml
<!DOCTYPE html>
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
<title>Belajar JavaScript</title>

<script>
window.onload = function()
{
   var hasil;
   hasil = 1+3+5+7+9;
   console.log(hasil);
}
</script>

</head>
<body>
<h1>Belajar JavaScript</h1>
</body>
</html>
```

### Core Javascript dan DOM ###

Core JavaScript atau JavaScript inti adalah istilah yang merujuk kepada ‘Bahasa Pemograman JavaScript‘. Pada bagian Core JavaScript inilah kita akan belajar tentang aturan pemograman yang umumnya dipelajari, seperti cara pendefenisian variabel, perbedaan tipe-tipe data, cara pembuatan array, cara penulisan struktur IF, serta cara pembuatan Objek.

Bagian Core JavaScript membahas tentang “bahasa” (atau syntax) dari JavaScript. Jika anda pernah menggunakan bahasa pemograman seperti C++ atau PHP, tidak akan terlalu sulit untuk mempelajari aturan penulisan dalam JavaScript.

Bagian kedua yang akan kita pelajari dalam menguasai Client-Side JavaScript adalah DOM (singkatan dari Document Object Model). DOM adalah API (Application Programming Interface) yang disediakan web browser kepada programmer.

Secara sederhananya, DOM adalah kumpulan aturan atau cara bagi programmer untuk ‘memanipulasi’ apapun yang tampil dalam halaman web. DOM tidak terikat dengan JavaScript, dan sepenuhnya bukan bagian dari JavaScript.

Tag atau element yang ada di dalam HTML diatur di dalam DOM. Dengan menggunakan JavaScript, kita bisa memanipulasi seluruh tag HTML ini. Salah satu contoh DOM yang telah kita gunakan adalah fungsi document.getElementById.

Fungsi document.get ElementById berfungsi untuk mencari sebuah tag HTML berdasarkan id. Selain document.getElementById, dalam DOM juga disediakan fungsi lain seperti document.getElementByName, document.getElementByClass, dan lain-lain.

### Aturan Penulisan Javascript ###

#### Case Sensitive ####

Di dalam JavaScript, penulisan huruf besar dan huruf kecil dibedakan, atau dalam istilah pemograman bersifat Case Sensitif. Hal ini berarti penulisan variabel , keyword, maupun nama fungsi di dalam JavaScript harus konsisten. Variabel nama, Nama, dan NAMA merupakan 3 variabel berbeda. Sedangkan untuk penulisan keyword while, harus ditulis dengan ‘while’, bukan ‘While’ atau ‘WHILE’.

#### Whitespace ####

Karakter-karakter spasi, enter, tab dan karakter lain yang ‘tidak kelihatan’ (sering dikenal dengan istilah whitespace) akan diabaikan pada saat pemrosesan JavaScript. Karakter-karakter ini bisa digunakan untuk ‘menjorokkan’ (indent) kode program agar lebih mudah dibaca.

#### Komentar ####

JavaScript mendukung 2 jenis cara penulisan komentar, yakni menggunakan karakater // untuk komentar dalam 1 baris, dan karakter pembuka komentar /* dan penutup */ untuk komentar yang mencakup beberapa baris.

#### Aturan Penulisan Identifier (Variabel dan Nama Fungsi) JavaScript ####

Di dalam JavaScript, identifier adalah sebutan untuk nama. Nama ini bisa terdiri dari nama variabel, atau nama dari fungsi. Aturan penulisan identifier dalam JavaScript adalah :
- Karakter pertama harus diawali dengan huruf, underscore (_) atau tanda dollar ($)
- Karakter kedua dan seterusnya bisa ditambahkan dengan huruf, angka, underscore (_) atau tanda dollar ($).

Dari aturan tersebut dapat dilihat bahwa kita tidak bisa menggunakan angka sebagai karakter pertama dari sebuah variabel atau nama fungsi.

#### Kata Kunci (Reserved Keyword) JavaScript ####

Seperti bahasa pemograman lain, JavaScript juga memiliki beberapa kata kunci atau keyword yang tidak bisa digunakan sebagai nama variabel atau nama dari sebuah fungsi. Istilah ini sering disebut sebagai reserved keyword.

Reserved keyword merupakan kata kunci yang digunakan JavaScript dalam menjalankan fungsinya. Diantaranya: extends, import, double, boolean, dll.

### Variable ###

Javascript merupakan sebuah bahasa dinamis seperti PHP artinya tidak mendefinisikan tipe data dari variable secara eksplisit.

Dalam bahasa pemograman, variabel adalah ‘penampung’ sebuah nilai. Tergantung dengan ‘nilai’ dari variabel tersebut, sebuah variabel di dalam JavaScript dapat bertipe Angka (Number), String, Boolean, atau yang lainnya.

Tidak seperti bahasa pemograman desktop seperti C++ dan Visual Basic, di dalam JavaScript kita tidak perlu mendeklarasikan jenis tipe data. Seluruh variabel di dalam JavaScript dapat berisi nilai apapun (tipe data apapun), dan dapat diubah menjadi tipe lain sepanjang program.

```xml
<!DOCTYPE html>
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
<title>Belajar JavaScript</title>

<script>
var nilai = "global";
function test() {
   var nilai = "lokal";
   var nilai_lokal = "belajar";
   tanpa_var = "no_scope"; //akan menjadi global variabel!!
   console.log(nilai);
   }
 
test(); // print: lokal
console.log(nilai); // print: global
console.log(tanpa_var); //print: no_scope (bisa diakses)
console.log(nilai_lokal); //error, karena nilai_lokal adalah lokal variabel
</script>

</head>
<body>
<h1>Belajar JavaScript</h1>
</body>
</html>
```

### Jenis dan Pengertian Tipe Data Dalam JavaScript ###

Tipe data dalam JavaScript dibedakan menjadi 2 kelompok, yakni tipe data dasar (primitif) dan tipe data objek.

Tipe data dasar terdiri dari tipe data angka, tipe data text (string), dan tipe data boolean.

Tipe data lain yang ada di dalam JavaScript adalah tipe data objek. Contoh tipe data objek adalah tipe data tanggal (date), array, dan fungsi.

Walaupun disebut tipe data dasar, tipe data angka, text (string), dan boolean di dalam JavaScript berprilaku ‘seolah-olah’ sebagai objek. Dimana setiap variabel yang berisikan tipe data, akan memiliki method (atau fungsi) yang ‘melekat’ kepada variabel tersebut.

Di dalam JavaScript, walaupun juga memiliki fungsi bawaan untuk membantu kita dalam membuat kode program, namun kebanyakan fungsi dasar ‘melekat’ kedalam variabel, atau di dalam istilah pemograman objek: setiap variabel akan memiliki ‘method’.

Cara pemanggilan method dari variabel di dalam JavaScript adalah dengan menambahkan tanda ‘titik’. Misalkan a variabel dengan tipe data string yang berisi sebuah kalimat. Untuk mencari panjang dari sting a, kita memanggil method dengan cara: a. length. Dan untuk menampilkan karakter dalam variabel a menjadi huruf besar, ditulis dengan a.toUpperCase().

```xml
<!DOCTYPE html>
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
<title>Belajar JavaScript</title>

<script>
   a = "Saya Sedang Belajar JavaScript";
   console.log(a.length);
   console.log(a.toUpperCase());
</script>
 
</head>
<body>
<h1>Belajar JavaScript</h1>
</body>
</html>
```

### Operator Aritmatika ###

Operasi yang sering digunakan untuk tipe data angka adalah operasi artimatika seperti penambahan (+), pengurangan (-), pembagian (/), perkalian (*), dan modulus atau sisa hasil bagi (%).

```xml
<!DOCTYPE html>
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
<title>Belajar JavaScript</title>

<script>
   var a = 12;
   var b = 4;
   var c = 2;
   console.log(a);       // hasil: 12
   console.log(b);       // hasil: 4
   console.log(c);       // hasil: 2
  
   var d = a + b;
   console.log(d);       // hasil: 16
   var e = b * 5;
   console.log(e);       // hasil: 20
   var f = a % 5;
   console.log(f);       // hasil: 2
   var g = 3 + 6 * 2;
   console.log(g);       // hasil: 15
   var h = c + b * a % 3;
   console.log(h);       // hasil: 2
   var i = 3 * 4 / 5 * 5;
   console.log(i);       // hasil: 12
   var j = (((3 * 4) / 5) * 5);
   console.log(j);       // hasil: 12
</script>

</head>
<body>
<h1>Belajar JavaScript</h1>
</body>
</html>
```

### Object Math ###

Untuk operasi angka (number) dan matematika yang lebih kompleks, JavaScript menyediakan objek Math yang terdiri dari berbagai kosntanta dan juga method (fungsi). Method yang tersedia misalnya untuk fungsi pemangkatan, akar kuadrat, logaritma, dan trigonometri.

Berikut adalah method yang disediakan oleh objek Math JavaScript, diurutkan berdasarkan abjad.
- Math.abs()
- Math.acos()
- Math.asin()
- Math.atan()
- Math.atan2()
- Math.ceil()
- Math.cos()
- Math.exp()
- Math.floor()
- Math.log()
- Math.max()
- Math.min()
- Math.pow()
- Math.random()
- Math.round()
- Math.sin()
- Math.sqrt()
- Math.tan()

```xml
<script>
Math.abs(-5)      // hasilnya: 5
Math.abs(5)       // hasilnya: 5
Math.abs(-22.78)  // hasilnya: 22.78

Math.ceil(1.99);    // hasilnya: 2
Math.ceil(1.01);    // hasilnya: 2
Math.ceil(1.0);     // hasilnya: 1
Math.ceil(-1.99);   // hasilnya: -1

Math.floor(1.99);    // hasilnya: 1
Math.floor(1.01);    // hasilnya: 1
Math.floor(1.0);     // hasilnya: 1
Math.floor(-1.01);   // hasilnya: -2

Math.max(1,2,3,4,5,6);     // hasilnya: 6
Math.max(10,20,30,90,5);   // hasilnya: 90
Math.max(50);              // hasilnya: 50

Math.min(1,2,3,4,5,6);       // hasilnya: 1
Math.mmin(10,20,30,90,5);    // hasilnya: 5
Math.max(50);                // hasilnya: 50

// pemangkatan
Math.pow(1,100);      // 1^100, hasilnya: 1
Math.pow(5,3);        // 5^3, hasilnya: 125
Math.pow(50);         // hasilnya: 50

Math.random();    // hasilnya: 0.2605599395465106
Math.random();    // hasilnya: 0.6355015402659774
Math.random();    // hasilnya: 0.5217791700270027

// pembulatan ke angka terdekat
Math.round(1.56);    // hasilnya: 2
Math.round(1.44);    // hasilnya: 1
Math.round(1.0);     // hasilnya: 1
Math.round(-1.6);    // hasilnya: -2
</script>
```

### String ###

Tipe data String di dalam JavaScript adalah tipe data yang terdiri dari kumpulan karakter yang berurutan. Atau di dalam penggunaan sehari-hari string adalah tipe data yang menampung nilai text atau kalimat.

Untuk membuat sebuah tipe data string, kita hanya tinggal menambahkan tanda kutip (bahasa inggris: ’quotes’) pada awal dan akhir dari text. JavaScript mendukung penggunaan tanda kutip satu ( ’ ) manupun tanda kutip ganda ( ’’ ). Didalam sumber bahasa inggris sering disebut sebagai single quote dan double quote.

```xml
<script>
var nama = "Hello";
var situs = 'belajar';
var pesan = 'dia berkata:"Hello!"';
var pesan2 = "Test";
</script>
```

Jika sebuah string diinput dengan menggunakan karakter awal tanda kutip satu, maka juga harus diakhiri dengan tanda kutip satu juga, walaupun di dalam kalimat tersebut terdapat tanda kutip dua, dan begitu juga sebaliknya.

Operasi yang sering dilakukan untuk tipe data String adalah operasi penyambungan string, atau dikenal dengan istilah ‘concatenate string’. Untuk operasi ini, JavaScript menggunakan operator tambah (+).

```xml
<script>
var a="Hello";
var b="World";
var situs = a + b;    // HelloWorld
</script>
```

JavaScript akan ‘mendeteksi’ operasi tipe data pada saat menggunakan operator +. Jika kedua tipe data adalah angka (number), maka operasi yang akan dilakukan adalah penjumlahan, namun jika salah satu atau kedua variabel bertipe String, akan dilakukan operasi penyambungan String.

```xml
<script>
var a="Hello";
var b="World";
var c="14";
var d=12;
var e=3;
 
console.log(a+b);     // HelloWorld
console.log(a+c);     // Hello14
console.log(c+d);     // 1412
console.log(d+e);     // 15
</script>
```

Di dalam JavaScript, string bisa dianggap sebagai array dari karakter, dan kita bisa mengambil nilai sebuah karakter dari String dengan mengaksesnya seperti array.

```xml
<script>
var situs = "hello";
console.log(situs[0]);    // h
console.log(situs[1]);    // e
console.log(situs[2]);    // l
console.log(situs[3]);    // l
console.log(situs[4]);    // o
</script>
```

Walaupun tipe data string bukan di defenisikan menjadi objek, namun JavaScript ‘memperlakukan’ tipe dasar String ini sebagai Objek String, sehingga memiliki property dan method yang dapat di gunakan.

Property dan method dari objek String semuanya mengembalikan nilai baru, dan tidak bisa mengubah nilai dalam variabel asal. Variabel asal String tetap bernilai seperti semula. Dalam pemograman sifat ini disebut dengan immutable variable.

Property Objek String JavaScript:
- string.length

Method Objek String JavaScript:
- string.charAt()
- string.charCodeAt()
- string.concat()
- string.indexOf()
- string.lastIndexOf()
- string.localeCompare()
- string.match()
- string.replace()
- string.search()
- string.slice()
- string.split()
- string.substr()
- string.substring()
- string.toLowerCase()
- string.toString()
- string.toUpperCase()
- string.trim()
- string.valueOf()

```xml
<script>
var kalimat = "Belajar JavaScript";
console.log(kalimat.toLocaleLowerCase());  // hasil: belajar javascript
console.log(kalimat.toLowerCase());        // hasil: belajar javascript

var kalimat2 = "bELAJAR JaVaScrIPT";
console.log(kalimat2.toLocaleLowerCase()); // hasil: belajar javascript
console.log(kalimat2.toLowerCase());       // hasil: belajar javascript

var kalimat = "Belajar JavaScript";
console.log(kalimat.toLocaleUpperCase());  // hasil: BELAJAR JAVASCRIPT
console.log(kalimat.toUpperCase());        // hasil: BELAJAR JAVASCRIPT

var kalimat2 = "bELAJAR JaVaScrIPT";
console.log(kalimat2.toLocaleUpperCase()); // hasil: BELAJAR JAVASCRIPT
console.log(kalimat2.toUpperCase());       // hasil: BELAJAR JAVASCRIPT
</script>
```

### Operator Perbandingan ###

Di dalam JavaScript (dan juga bahasa pemograman lain) operator perbandingan adalah operator yang digunakan untuk membandingkan sebuah nilai atau variabel dengan variabel lainnya. Hasil dari operasi perbandingan ini akan menghasilkan nilai boolean.

#### Operator sama dengan (==) ####

Operator sama dengan adalah operator yang akan membandingkan 2 buah nilai atau variabel dan menghasilkan nilai true jika variabel tersebut bernilai sama.

```xml
<script>
var a = true;
var benar = true;
console.log(a==benar); // true

var a = 12;
var b = 4;
console.log(a==b); // false

var a = 7;
var b = "7";
console.log(a==b); // true !
</script>
```

Perhatikan persamaan pada baris terakhir. Operasi == tidak melihat tipe data dari variabel yang akan dibandingkan, sehingga 7 (tipe data number) akan dianggap sama dengan “7” (tipe data string). Jika anda ingin membandingkan kedua variabel ini, dan memasukkan jenis tipe data sebagai salah satu penilaian sama atau tidaknya 2 buah variabel, maka harus menggunakan operator identikal (===).

#### Operator identik dengan (===) ####

Operator identikal === hampir sama dengan operator ==, yaitu membandingkan apakah 2 buah variabel atau hasil operasi program sama atau tidak. Perbedaannya, operator === lebih ‘ketat aturan’ daripada operator ==. Operasi 7 == “7” akan dianggap sama dan menghasilkan nilai true, namun operasi 7 === “7” akan dianggap false, karena tipe data kedua nilai ini berbeda.

```xml
<script>
var a = true;
var benar = true;
console.log(a===benar); // true

var a = 12;
var b = 4;
console.log(a===b); // false

var a = 7;
var b = "7";
console.log(a===b); // false !

var a = "7";
var b = "7";
console.log(a===b); // true
</script>
```

#### Operator tidak sama dengan (!=) ####

Operator != adalah kebalikan dari operator ==, dan akan menghasilkan nilai true jika hasil operasi 2 buah variabel yang dibandingkan tidak memiliki nilai yang sama.

```xml
<script>
var a = true;
var benar = true;
console.log(a!=benar); // false

var a = 12;
var b = 4;
console.log(a!=b); // true

var a = 7;
var b = "7";
console.log(a!=b); // false !
</script>
```

Perhatikan juga untuk persamaan baris terakhir, operator != tidak mempertimbangkan tipe data variabel, sama seperti operator ==. Jika anda ingin jenis tipe data juga merupakan kriteria perbandingan, maka gunakan operator !==.

#### Operator tidak identik dengan (!==) ####

Jika operator != tidak mempertimbangkan tipe data, maka operator !== hanya akan false jika operator yang dibandingkan memiliki nilai yang sama dan juga tipe data yang sama.

```xml
<script>
var a = true;
var benar = true;
console.log(a!==benar); // false

var a = 12;
var b = 4;
console.log(a!==b); // true

var a = 7;
var b = "7";
console.log(a!==b); // true !

var a = "7";
var b = "7";
console.log(a!==b); // false
</script>
```

#### Operator Perbandingan ####

```xml
<script>
var a = 3;
var b = 4;
console.log(a<b); // true
console.log(a<=b); // true

var a = 5;
var b = 5;
console.log(a<b); // false
console.log(a<=b); // true

var a = 3;
var b = 4;
console.log(a>b); // false
console.log(a>=b); // false

var a = 5;
var b = 5;
console.log(a>b); // false
console.log(a>=b); // true
</script>
```

#### Operasi Logika ####

```xml
<script>
var a = true;
var b = false;

var hasil1 = a && b;
console.log(hasil1); //false

var hasil2 = a && a;
console.log(hasil2); //true

var hasil3 = a || b;
console.log(hasil3); //true

var hasil4 = !a;
console.log(hasil4); //false
</script>
```

### Percabangan ###

```xml
<script>
var angka=12;
 
if (angka%2==0) 
{
   console.log("Angka = "+angka);
   console.log("Angka adalah bilangan genap");
}
else
{
   console.log("Angka = "+angka);
   console.log("Angka adalah bilangan ganjil");
}
</script>
```

```xml
<script>
var angka=5;

switch (angka) 
{
case 1:
       console.log("Angka Satu");
       break;
case 2:
       console.log("Angka Dua");
       break;
case 3:
       console.log("Angka Tiga");
       break;
case 4:
       console.log("Angka Empat");
       break;
default:
       console.log("Bukan angka 1 - 4");
       break;
}
</script>
```












