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

### Mengorganisasikan Konten ###

Pada HTML 5 memperkenalkan beberapa tag baru untuk mengorganisasikan halaman. Diantaranya adalah header, footer, nav, section, aside, article, address, details, hgroup dan summary.

### Div ###

Tag div atau kepanjangan dari division, merupakan tag yang umum digunakan dan biasanya digunakan untuk membagi halaman menjadi beberapa bagian yang akan ditujukan untuk konten tertentu.

### Table ###

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

### List ###

Di HTML 5 list dibagi menjadi dua, yaitu ordered `<ol>` dan unordered `<ul>`. Ordered akan menampilkan list  menggunakan angka, sedangkan unordered akan menampilkan dalam bentuk bullet.

```xml
<ol>
	<li>Roti</li>
    <li>Kue</li>
</ol>
```

```xml
<ul>
	<li>Roti</li>
    <li>Kue</li>
</ul>
```

### Input dan Form ###

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


### CSS Framework ###

CSS framework merupakan library CSS yang telah dibuat untuk memudahkan dalam mendesain suatu halaman. Dengan menggunakan framework diharapkan akan membuat pekerjaan menjadi lebih mudah dan cepat.

Akhir-akhir ini sering kita dengar tentang responsive web design, artinya tampilan web yang responsif yang tetap nyaman saat dibuka di desktop, tablet maupun mobile device. Dan framework yang menawarkan responsive web design inilah yang sering dipakai oleh kebanyakan orang. Diantara yang cukup populer adalah [materializecss](http://materializecss.com) dan [bootstrap](http://getbootstrap.com).



## JavaScript ##

Javascript merupakan scripting language yang berjalan diatas browser. Bahasa Javascript ini sedikit banyak dipengaruhi oleh Java dan syntax bahasanya pun juga mirip dengan Java, akan tetapi Javascript tidak sama dengan Java. Java berjalan diatas runtime / JDK sedangkan Javascript tidak memerlukan compiler atau runtime.

Javascript biasanya sangat diperlukan dalam pembuatan tampilan web, karena dengan adanya Javascript akan membuat web kita menjadi lebih interaktif.

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

### Variable ###

Javascript merupakan sebuah bahasa dinamis seperti PHP artinya tidak mendefinisikan tipe data dari variable secara eksplisit.









