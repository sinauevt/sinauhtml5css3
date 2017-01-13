## BELAJAR BOOTSTRAP 3 ##

### Apa itu Bootstrap ###

Bootstrap merupakan design framework yang responsif. Dapat digunakan untuk mendesain tampilan web agar terlihat lebih yahut dengan cara yang cukup instan dan sederhana. Bootstrap ini sangat terkenal lho akhir-akhir ini dan banyak dipakai para pembuat web untuk mempercantik tampilan antarmuka web mereka.

Pada jaman dahulu kala, untuk mendesain sebuah tampilan web sederhana sangatlah merepotkan, apalagi kalo gak punya template-nya. Harus bikin css yg cukup banyak, kalo belum punya ya ngopi sana-sini, belum lagi untuk bikin supaya bisa multi-web-browser support yang merepotkan (di google chrome tampilannya menawan tapi di IE kok jadi kayak gembel? pernah mengalami yang seperti itu? yes that is sucks). Tapi dengan adanya bootstrap pekerjaan yang seperti ini akan jauh lebih mudah.

Sampai saat ini bootstrap telah mencapai versi 3, lebih tepatya v.3.3.6. Ada perbedaan yang sangat signifikan bila kita telah menggunakan versi 2. Bila kita telah menggunakan library versi 2 pada suatu halaman web dan ingin beralih ke library versi 3 maka perlu mengganti code-code yang masih menggunakan versi 2 ke versi 3, dikarenakan pada rilis versi 3 tidak terdapat support untuk versi 2. Hmmm... cukup radikal yah.

> Yang saat ini sedang belajar Angularjs versi 1 pasti sedang mengalami dilema yang sama ketika akan mencoba Angularjs versi 2, karena perbedaan yang sangat radikal dari keduanya. Ini juga berimbas pada framework lain yang menggunakan Angularjs, yaitu IonicFramework.

Bootstrap sadar hal tersebut adalah sebuah kesalahan dan mereka berjanji ketika rilis selanjutnya yaitu versi 4, mereka akan menyertakan support untuk versi sebelumnya yaitu versi 3. Jadi pengguna dapat beralih secara berkala ke versi yang baru.

### Persiapan ###

#### Download Bootstrap ####

Sebelum memulai seperti biasa kita harus men-download perangkat atau library yang dibutuhkan terlebih dahulu. Bootstrap dapat di-download disitus resminya http://www.getbootstrap.com.

Setelah proses download selesai, ekstrak file tersebut. Kita akan mendapatkan satu set file distribusi bootstrap yang berisi tiga buah folder, yaitu css, fonts dan js.

bootstrap-3.3.6-dist <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;+---css <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;+---fonts <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;+---js <br>

#### Sample Project ####

Buat satu buah folder dengan nama belajarbootstrap. Copy tiga buah folder (css, fonts dan js) dari distribusi file bootstrap yang telah kita download dan ekstrak. Paste kedalam folder project yang telah kita buat.

Buka project yang telah kita buat didalam code editor (bisa menggunakan sublime, visual studio code, atom, brackets, dll). Buat satu buah file dan beri nama index.html didalam project.

```html
<!doctype html>
<html>
<head>
    <meta charset="utf-8">
    <title>Belajar Bootstrap</title>
</head>
<body>

</body>
</html>
```

Tambahkan line berikut `<meta name="viewport" content="width=device-width, initial-scale=1.0">` didalam tag head untuk membuat tampilan yang kita buat menjadi responsif.

Tambahkan bootstrap kedalam file dengan nenambahkan line berikut `<link rel="stylesheet" href="css/bootstrap.min.css">`.

Tambahkan link ke javascript library, kita akan tambahkan jquery dan javascript dari bootstrap. Mengapa jquery, karena library javascript bootstrap membutuhkan atau bergantung dengan jquery.

```html
<body>
<!-- javascript -->
<script src="js/jquery-latest.min.js"></script>
<script src="js/bootstrap.min.js"></script>
</body>
```

Kenapa ditambahinnya di body html dan nggak di head? Perbedaannya adalah semua yang ada di head akan diload terlebih dahulu secara lengkap sebelum kita dapat melihat halaman secara keseluruhan, yang akan membuat halaman web terasa lambat jika kita banyak menaruh link didalam head. Jadi idealnya informasi di halaman web akan diload terlebih dahulu baru kemudian functionality-nya. Dan karena Jquery adalah library yang berfungsi untuk functionality dari halaman web, maka kita dapat menaruhnya dibagian body dari html. Jadi information load first baru kemudian functionlity-nya.

Mari kita tambahkan isi dari body html-nya.

```html
<body>
<!-- row 1 -->
    <a href="#"><img src="img/logo.png" alt="Wisdom Pets. click for home."></a>

    <img src="img/animals.jpg" alt="">

<!-- row 2 -->
    <h1> We treat your pets like our own</h1>

    <p>At Wisdom Pet Medicine, we strive to blend the best in traditional   and alternative healing techniques to diagnose and treat companion   animals, including dogs, cats, birds, reptiles, rodents, and fish. </p>

<!-- row 3 -->
    <p><img src="img/gsd.jpg" alt=""></p>
    <h4>Thanks for helping our German Shepherd</h4>
    <p>During the summer, my German Shorthair Pointer, Tonto, began to have severe redness and itching on his belly and feet. Through diagnostic testing, we learned that Tonto is severely allergic to over a dozen kinds of grass pollens.</p>
    <p><a href="#">Read more >></a></p>
    <p><img src="img/kitten.jpg" alt=""></p>
    <h4>Our diabetic kitty is better</h4>
    <p>When Samantha, our sweet kitten, began sleeping all the time and urinating excessively, we brought her to see the specialists at Wisdom. After running a blood test, Dr. Winthrop confirmed what we all feared – Samantha was showing signs of diabetes. </p>
    <p><a href="#">Read more >></a></p>
	<p><img src="img/bulldog.jpg" alt=""></p>
    <h4>Our grape-loving dog</h4>
    <p>The staff at Wisdom worked tirelessly to determine why our three-year old bulldog, Roxie, started going into sudden kidney failure. They stabilized her and provided fluids until her kidneys were again functioning normal, but it was still a mystery as to what caused her health to decline so quickly. </p>
    <p><a href="#">Read more >></a></p>
    <p><img src="img/goldfish.jpg" alt=""></p>
    <h4>A dog antibiotic cured our fish</h4>
    <p>Wisdom Pet Medicine is the only clinic around that will even book pet fish for appointments. When our 13-year old goldfish, McAllister, turned from silvery white to an angry red, we called around, urgently trying to find a veterinarian who could help. Wisdom not only got us in the same day, but also was able to diagnose McAllister as having a severe case of septicemia. </p>
     <p><a href="#">Read more >></a></p>

<!-- row 4 -->
     <p>This not a real veterinary medicine site, and is not meant to diagnose or offer treatment. Please see your veterinarian for all matters related to your pet's health.</p>
	 <p>Wisdom Pet Medicine</p>

<!-- javascript -->
	<script src="http://code.jquery.com/jquery-latest.min.js"></script>
    <script src="js/bootstrap.min.js"></script>
</body>
```

### Bootstrap Grid System ###

#### Grid System ####

Bootstrap menganut paham grid system yang berjumlah 12. Grid system ini bersifat responsif dan dapat mengatur ulang tampilannya berdasarkan jenis layar yang dipakai pengguna. Grid system ini juga bisa digabungkan atau di merge satu dengan yang lain, asal jumlahnya dalam satu row tidak lebih dari 12. Jadi pastikan ketika mendesain tampilan jumlah kolom dalam satu row tidak lebih dari 12. Kira-kira bentuknya seperti dibawah ini.

<table cellspacing="0">
<tr>
  <td>span 1</td>
  <td>span 1</td>
  <td>span 1</td>
  <td>span 1</td>
  <td>span 1</td>
  <td>span 1</td>
  <td>span 1</td>
  <td>span 1</td>
  <td>span 1</td>
  <td>span 1</td>
  <td>span 1</td>
  <td>span 1</td>
</tr>
<tr>
  <td colspan="4">&nbsp;span 4</td>
  <td colspan="4">&nbsp;span 4</td>
  <td colspan="4">&nbsp;span 4</td>
</tr>
<tr>
  <td colspan="4">span 4</td>
  <td colspan="8">span 8</td>
</tr>
<tr>
  <td colspan="6">span 6</td>
  <td colspan="6">span 6</td>
</tr>
<tr>
  <td colspan="12">span 12</td>
</tr>
</table>

#### Grid Classes ####

Selain grid system yang berjumlah 12, didalamnya terdapat class-class yang berguna untuk mengatur tampilan berdasarkan besar-kecilnya layar pengguna. Class-class ini dapat dikombinasikan untuk membuat tampilan yang lebih fleksibel dan dinamis.

- xs (untuk smartphone)
- sm (untuk tablet)
- md (untuk desktop)
- lg (untuk large desktop)

Keterangan lebih lanjut mengenai grid system dan grid classes bisa dibaca [pada link berikut](http://www.w3schools.com/bootstrap/bootstrap_grid_system.asp).

##### Nyoba Grid #####

Dari sample yang kita buat tadi, kita akan coba memasang grid disana. Pertama-tama kita tambahkan `<div class="row"></div>` pada masing-masing row.

```html
<body>
<!-- row 1 -->
<header class="row">
    <a href="#"><img src="img/logo.png" alt="Wisdom Pets. click for home."></a>

    <img src="img/animals.jpg" alt="">
</header>
<!-- row 2 -->
<div class="row">
    <h1> We treat your pets like our own</h1>

    <p>At Wisdom Pet Medicine, we strive to blend the best in traditional   and alternative healing techniques to diagnose and treat companion   animals, including dogs, cats, birds, reptiles, rodents, and fish. </p>
</div>
<!-- row 3 -->
<div class="row">
    <p><img src="img/gsd.jpg" alt=""></p>
    <h4>Thanks for helping our German Shepherd</h4>
    <p>During the summer, my German Shorthair Pointer, Tonto, began to have severe redness and itching on his belly and feet. Through diagnostic testing, we learned that Tonto is severely allergic to over a dozen kinds of grass pollens.</p>
    <p><a href="#">Read more >></a></p>
    <p><img src="img/kitten.jpg" alt=""></p>
    <h4>Our diabetic kitty is better</h4>
    <p>When Samantha, our sweet kitten, began sleeping all the time and urinating excessively, we brought her to see the specialists at Wisdom. After running a blood test, Dr. Winthrop confirmed what we all feared – Samantha was showing signs of diabetes. </p>
    <p><a href="#">Read more >></a></p>
	<p><img src="img/bulldog.jpg" alt=""></p>
    <h4>Our grape-loving dog</h4>
    <p>The staff at Wisdom worked tirelessly to determine why our three-year old bulldog, Roxie, started going into sudden kidney failure. They stabilized her and provided fluids until her kidneys were again functioning normal, but it was still a mystery as to what caused her health to decline so quickly. </p>
    <p><a href="#">Read more >></a></p>
    <p><img src="img/goldfish.jpg" alt=""></p>
    <h4>A dog antibiotic cured our fish</h4>
    <p>Wisdom Pet Medicine is the only clinic around that will even book pet fish for appointments. When our 13-year old goldfish, McAllister, turned from silvery white to an angry red, we called around, urgently trying to find a veterinarian who could help. Wisdom not only got us in the same day, but also was able to diagnose McAllister as having a severe case of septicemia. </p>
     <p><a href="#">Read more >></a></p>
</div>
<!-- row 4 -->
<footer class="row">
     <p>This not a real veterinary medicine site, and is not meant to diagnose or offer treatment. Please see your veterinarian for all matters related to your pet's health.</p>
	 <p>Wisdom Pet Medicine</p>
</footer>

<!-- javascript -->
	<script src="js/jquery-latest.min.js"></script>
    <script src="js/bootstrap.min.js"></script>
</body>
```

Pada row ke-3 kita akan mengaplikasikan grid disini. Kita akan membuatnya menjadi empat buah kolom menggunakan class `md`, jadi untuk masing-masing kolom kita akan buat lebarnya menjadi tiga (ingat konsep 12 grid system bootstrap). Jadi kita tambahkan line `<div class="col-md-3">` pada masing-masing kolom.

```html
<!-- row 3 -->
<div class="row">
    <div class="col-md-3">
        <p><img src="img/gsd.jpg" alt=""></p>
        <h4>Thanks for helping our German Shepherd</h4>
        <p>During the summer, my German Shorthair Pointer, Tonto, began to have severe redness and itching on his belly and feet. Through diagnostic testing, we learned that Tonto is severely allergic to over a dozen kinds of grass pollens.</p>
        <p><a href="#">Read more >></a></p>
    </div>
    <div class="col-md-3">
        <p><img src="img/kitten.jpg" alt=""></p>
        <h4>Our diabetic kitty is better</h4>
        <p>When Samantha, our sweet kitten, began sleeping all the time and urinating excessively, we brought her to see the specialists at Wisdom. After running a blood test, Dr. Winthrop confirmed what we all feared – Samantha was showing signs of diabetes. </p>
        <p><a href="#">Read more >></a></p>
    </div>
    <div class="col-md-3">
        <p><img src="img/bulldog.jpg" alt=""></p>
        <h4>Our grape-loving dog</h4>
        <p>The staff at Wisdom worked tirelessly to determine why our three-year old bulldog, Roxie, started going into sudden kidney failure. They stabilized her and provided fluids until her kidneys were again functioning normal, but it was still a mystery as to what caused her health to decline so quickly. </p>
        <p><a href="#">Read more >></a></p>
    </div>
    <div class="col-md-3">
        <p><img src="img/goldfish.jpg" alt=""></p>
        <h4>A dog antibiotic cured our fish</h4>
        <p>Wisdom Pet Medicine is the only clinic around that will even book pet fish for appointments. When our 13-year old goldfish, McAllister, turned from silvery white to an angry red, we called around, urgently trying to find a veterinarian who could help. Wisdom not only got us in the same day, but also was able to diagnose McAllister as having a severe case of septicemia. </p>
        <p><a href="#">Read more >></a></p>
    </div>
</div>
```

Kalo kita liat di web browser tampilannya akan jadi lebih rapi dari pada sebelumnya. dan kalo browsernya dikecilkan lebarnya semakin kecil... semakin kecil..., maka tampilannya akan menyesuaikan dan akan berpindah posisi jika sudah tidak muat lagi.

Coba kita update lagi supaya saat layar mengecil masih dapat menampilkan dua kolom.

```html
<body>
<div class="container">
    <!-- row 1 -->
    <header class="row">
        <div class="col-lg-6 col-sm-5">
            <a href="#"><img src="img/logo.png" alt="Wisdom Pets. click for home."></a>
        </div>

        <div class="col-lg-6 col-sm-5">
            <img src="img/animals.jpg" alt="">
        </div>
    </header>
    <!-- row 2 -->
    <div class="row">
        <h1> We treat your pets like our own</h1>

        <p>At Wisdom Pet Medicine, we strive to blend the best in traditional   and alternative healing techniques to diagnose and treat companion   animals, including dogs, cats, birds, reptiles, rodents, and fish. </p>
    </div>
    <!-- row 3 -->
    <div class="row">
        <div class="col-md-3 col-xs-6">
            <p><img src="img/gsd.jpg" alt=""></p>
            <h4>Thanks for helping our German Shepherd</h4>
            <p>During the summer, my German Shorthair Pointer, Tonto, began to have severe redness and itching on his belly and feet. Through diagnostic testing, we learned that Tonto is severely allergic to over a dozen kinds of grass pollens.</p>
            <p><a href="#">Read more >></a></p>
        </div>
        <div class="col-md-3 col-xs-6">
            <p><img src="img/kitten.jpg" alt=""></p>
            <h4>Our diabetic kitty is better</h4>
            <p>When Samantha, our sweet kitten, began sleeping all the time and urinating excessively, we brought her to see the specialists at Wisdom. After running a blood test, Dr. Winthrop confirmed what we all feared – Samantha was showing signs of diabetes. </p>
            <p><a href="#">Read more >></a></p>
        </div>
        <div class="col-md-3 col-xs-6">
            <p><img src="img/bulldog.jpg" alt=""></p>
            <h4>Our grape-loving dog</h4>
            <p>The staff at Wisdom worked tirelessly to determine why our three-year old bulldog, Roxie, started going into sudden kidney failure. They stabilized her and provided fluids until her kidneys were again functioning normal, but it was still a mystery as to what caused her health to decline so quickly. </p>
            <p><a href="#">Read more >></a></p>
        </div>
        <div class="col-md-3 col-xs-6">
            <p><img src="img/goldfish.jpg" alt=""></p>
            <h4>A dog antibiotic cured our fish</h4>
            <p>Wisdom Pet Medicine is the only clinic around that will even book pet fish for appointments. When our 13-year old goldfish, McAllister, turned from silvery white to an angry red, we called around, urgently trying to find a veterinarian who could help. Wisdom not only got us in the same day, but also was able to diagnose McAllister as having a severe case of septicemia. </p>
            <p><a href="#">Read more >></a></p>
        </div>
    </div>
    <!-- row 4 -->
    <footer class="row">
        <p>This not a real veterinary medicine site, and is not meant to diagnose or offer treatment. Please see your veterinarian for all matters related to your pet's health.</p>
        <p>Wisdom Pet Medicine</p>
    </footer>
</div><!-- End container -->

<!-- javascript -->
	<script src="js/jquery-latest.min.js"></script>
    <script src="js/bootstrap.min.js"></script>
</body>
```

Mari kita lihat, kenapa `xs` yang ditambahkan jumlahnya lebih dari 12, bukannya maksimal 12. Nah, untuk kasus tertentu `xs` adalah pengecualian dan dapat menerima lebih dari 12 kolom.

Sample source code ada pada file cobagrid/cobakolom.html.

#### Offset ####

Offset digunakan untuk memberikan ruang antar kolom. Ketika kita mengaplikasikan offset maka space / ruang kosong akan diberikan pada kolom yang berada disebelah kiri.

##### Nyoba Offset #####

Untuk mengaplikasikan offset, misal kita telah memiliki sebuah kolom `<article class="col-lg-9 col-sm-8">` dan ingin membuat offset sebesar satu, maka kurangi satu pada kolom tersebut sehingga menjadi `<article class="col-lg-8 col-sm-7">`. Kemudian tambahkan offset didalamnya sehingga menjadi seperti berikut. `<article class="col-lg-8 col-lg-offset-1 col-sm-7 col-sm-offset-1">`.

Sample source code ada pada file cobagrid/cobaoffset.html.

#### Push dan Pull ####

Kadang adakalanya kita memiliki tampilan web yang terdiri dari artikel utama dan beberapa bagian yang bukan dari inti artikel. Seperti pada contoh dibawah ini.

```html
<div class="row">
    <aside class="col-lg-3 col-sm-4">
    	<h3>Keeping your pet's chompers clean and healthy</h3>
        <p>You know the importance of brushing your own teeth, but did you know that dogs and cats also need regular attention to their pearly whites? Poor dental hygiene in pets can lead to periodontal disease, a bacterial infection which causes bad breath, drooling, tooth decay, and tooth loss.</p>
    	<p>As always, if you have questions about your pet’s dental or health care, please <a href="#">contact Wisdom Pet Medicine</a> for advice.</p>
    </aside>
    <article class="col-lg-offset-1 col-sm-offset-1 col-lg-8 col-sm-7">
    	<h1>Services</h1>
    	<p><img src="../img/cockatiel.jpg" class="pull-right">Wisdom Pet Medicine is a state-of-the-art veterinary hospital,   featuring the latest in diagnostic and surgical equipment, and a staff   of seasoned veterinary specialists in the areas of general veterinary   medicine and surgery, oncology, dermatology, orthopedics, radiology,   ultrasound, and much more. We also have a 24-hour emergency clinic in   the event your pet needs urgent medical care after regular business   hours.</p>
    	<p>At Wisdom, we strive to be your pet&rsquo;s medical experts from youth   through the senior years. We build preventative health care plans for   each and every one of our patients, based on breed, age, and sex, so   that your pet receives the most appropriate care at crucial milestones   in his or her life. Our overarching goal is to give your pet the best   shot possible at a long and healthy life, by practicing simple   preventative care. We even provide an online Pet Portal where you can   view all your pet&rsquo;s diagnostic results, treatment plans, vaccination and   diagnostic schedules,  prescriptions, and any other health records.</p>
	</article>
</div>
```

##### Nyoba Push dan Pull #####

Jika tampilan web kita kecilkan maka artikel utama akan berada pada posisi bawah. Hal ini kadang tidak baik untuk search engine optimation atau mungkin klien lagi bad mood atau rese jadi minta yang aneh-aneh. Mungkin kita bisa coba cara berikut. Ubah posisi artikel utama dan gunakan push dan pull dari bootstrap untuk membereskan sisanya.

```html
<div class="row">
	<article class="col-lg-offset-1 col-sm-offset-1 col-lg-8 col-sm-7 col-lg-push-3 col-sm-push-4">
        <h1>Services</h1>
        <p><img src="../img/cockatiel.jpg" class="pull-right">Wisdom Pet Medicine is a state-of-the-art veterinary hospital,   featuring the latest in diagnostic and surgical equipment, and a staff   of seasoned veterinary specialists in the areas of general veterinary   medicine and surgery, oncology, dermatology, orthopedics, radiology, ultrasound, and much more. We also have a 24-hour emergency clinic in   the event your pet needs urgent medical care after regular business   hours.</p>
    	<p>At Wisdom, we strive to be your pet&rsquo;s medical experts from youth   through the senior years. We build preventative health care plans for   each and every one of our patients, based on breed, age, and sex, so   that your pet receives the most appropriate care at crucial milestones   in his or her life. Our overarching goal is to give your pet the best   shot possible at a long and healthy life, by practicing simple   preventative care. We even provide an online Pet Portal where you can   view all your pet&rsquo;s diagnostic results, treatment plans, vaccination and   diagnostic schedules,  prescriptions, and any other health records.</p>
    </article>
	<aside class="col-lg-3 col-sm-4 col-lg-pull-9 col-sm-pull-8">
        <h3>Keeping your pet's chompers clean and healthy</h3>
        <p>You know the importance of brushing your own teeth, but did you know that dogs and cats also need regular attention to their pearly whites? Poor dental hygiene in pets can lead to periodontal disease, a bacterial infection which causes bad breath, drooling, tooth decay, and tooth loss.</p>
    	<p>As always, if you have questions about your pet’s dental or health care, please <a href="#">contact Wisdom Pet Medicine</a> for advice.</p>
	</aside>
</div>
```

Sample source code ada pada file cobagrid/cobapushpull.html.

#### Nesting Column ####

Suatu ketika kita memiliki sebuah tampilan web seperti dibawah ini.

 ```html
 <!-- row 2 -->
<div class="row">
    	<article class="col-lg-offset-1 col-sm-offset-1 col-lg-8 col-sm-7 col-lg-push-3 col-sm-push-4">
            <h1>Services</h1>
            <p><img src="../img/cockatiel.jpg" class="pull-right">Wisdom Pet Medicine is a state-of-the-art veterinary hospital,   featuring the latest in diagnostic and surgical equipment, and a staff   of seasoned veterinary specialists in the areas of general veterinary   medicine and surgery, oncology, dermatology, orthopedics, radiology,   ultrasound, and much more. We also have a 24-hour emergency clinic in   the event your pet needs urgent medical care after regular business   hours.</p>
            <p>At Wisdom, we strive to be your pet&rsquo;s medical experts from youth   through the senior years. We build preventative health care plans for   each and every one of our patients, based on breed, age, and sex, so   that your pet receives the most appropriate care at crucial milestones   in his or her life. Our overarching goal is to give your pet the best   shot possible at a long and healthy life, by practicing simple   preventative care. We even provide an online Pet Portal where you can   view all your pet&rsquo;s diagnostic results, treatment plans, vaccination and   diagnostic schedules,  prescriptions, and any other health records.</p>
        </article>
        <aside class="col-lg-3 col-sm-4 col-lg-pull-9 col-sm-pull-8">
        	<h3>Keeping your pet's chompers clean and healthy</h3>
            <p>You know the importance of brushing your own teeth, but did you know that dogs and cats also need regular attention to their pearly whites? Poor dental hygiene in pets can lead to periodontal disease, a bacterial infection which causes bad breath, drooling, tooth decay, and tooth loss.</p>
            <p>As always, if you have questions about your pet’s dental or health care, please <a href="#">contact Wisdom Pet Medicine</a> for advice.</p>
         </aside>
    </div><!-- end row 2 -->

    <!-- row 3 -->
    <div class="row">
    	<div class="col-md-3 col-xs-6">
            <h4>Vaccinations</h4>
            <p>Dogs and cats are susceptible to a variety of illnesses that can be completely prevented by following the appropriate vaccination schedule.</p>
            <p><a href="#">Read more >></a></p>
        </div>
        <div class="col-md-3 col-xs-6">
            <h4>Checkups</h4>
            <p>Regular checkups are a key factor in pet wellness, and can often unearth problems that could lead to health issues down the road.  </p>
            <p><a href="#">Read more >></a></p>
        </div>
        <div class="col-md-3 col-xs-6">
            <h4>Senior Pets</h4>
            <p>Senior pets generally require more medical attention than their younger counterparts, just as senior humans do. So when is a pet considered “senior”? </p>
            <p><a href="#">Read more >></a></p>
        </div>
        <div class="col-md-3 col-xs-6">
            <h4>Diet Plans</h4>
            <p>Wisdom veterinarians have all had extensive training in pet nutrition and are your best resources when considering changing your pet’s diet. </p>
             <p><a href="#">Read more >></a></p>
         </div>
</div>
```

Pas kita pikir-pikir ulang lagi, hmmm... sepertinya lebih bagus kalo tulisan-tulisan yang berada di row 3 sejajar dengan services.

##### Nyoba Nesting Column #####

Untuk melakukan hal ini kita dapat menggunakan nesting. Nesting disupport penuh oleh bootstrap, jadi tidak perlu ada kekhawatiran saat memasang kolom didalam kolom. Mari kita coba.

Cut semua bagian row 3 dan paste ke baris paling bawah kolom article di row 2.

```html
<!-- row 2 -->
<div class="row">
    	<article class="col-lg-offset-1 col-sm-offset-1 col-lg-8 col-sm-7 col-lg-push-3 col-sm-push-4">
            <h1>Services</h1>
            <p><img src="../img/cockatiel.jpg" class="pull-right">Wisdom Pet Medicine is a state-of-the-art veterinary hospital,   featuring the latest in diagnostic and surgical equipment, and a staff   of seasoned veterinary specialists in the areas of general veterinary   medicine and surgery, oncology, dermatology, orthopedics, radiology,   ultrasound, and much more. We also have a 24-hour emergency clinic in   the event your pet needs urgent medical care after regular business   hours.</p>
            <p>At Wisdom, we strive to be your pet&rsquo;s medical experts from youth   through the senior years. We build preventative health care plans for   each and every one of our patients, based on breed, age, and sex, so   that your pet receives the most appropriate care at crucial milestones   in his or her life. Our overarching goal is to give your pet the best   shot possible at a long and healthy life, by practicing simple   preventative care. We even provide an online Pet Portal where you can   view all your pet&rsquo;s diagnostic results, treatment plans, vaccination and   diagnostic schedules,  prescriptions, and any other health records.</p>
            <!-- row 3 -->
            <div class="row">
                <div class="col-md-3 col-xs-6">
                    <h4>Vaccinations</h4>
                    <p>Dogs and cats are susceptible to a variety of illnesses that can be completely prevented by following the appropriate vaccination schedule.</p>
                    <p><a href="#">Read more >></a></p>
                </div>
                <div class="col-md-3 col-xs-6">
                    <h4>Checkups</h4>
                    <p>Regular checkups are a key factor in pet wellness, and can often unearth problems that could lead to health issues down the road.  </p>
                    <p><a href="#">Read more >></a></p>
                </div>
                <div class="col-md-3 col-xs-6">
                    <h4>Senior Pets</h4>
                    <p>Senior pets generally require more medical attention than their younger counterparts, just as senior humans do. So when is a pet considered “senior”? </p>
                    <p><a href="#">Read more >></a></p>
                </div>
                <div class="col-md-3 col-xs-6">
                    <h4>Diet Plans</h4>
                    <p>Wisdom veterinarians have all had extensive training in pet nutrition and are your best resources when considering changing your pet’s diet. </p>
                    <p><a href="#">Read more >></a></p>
                </div>
            </div>
        </article>
        <aside class="col-lg-3 col-sm-4 col-lg-pull-9 col-sm-pull-8">
        	<h3>Keeping your pet's chompers clean and healthy</h3>
            <p>You know the importance of brushing your own teeth, but did you know that dogs and cats also need regular attention to their pearly whites? Poor dental hygiene in pets can lead to periodontal disease, a bacterial infection which causes bad breath, drooling, tooth decay, and tooth loss.</p>
            <p>As always, if you have questions about your pet’s dental or health care, please <a href="#">contact Wisdom Pet Medicine</a> for advice.</p>
         </aside>
</div><!-- end row 2 -->
```

Sample source code ada pada file cobagrid/cobanestingcolumn.html.

#### JumboTron ####

Jumbotron adalah sebuah big box besar biasanya ditempatkan pada bagian header sebuah halaman web untuk mendapatkan atensi dari pengguna web.

##### Nyoba JumboTron #####

Bootstrap mensupport apa yang disebut sebagai jumbotron. Penggunaannya juga sangat mudah, cukup gunakan class jumbotron dan semua beres.

```html
<!-- row 2 -->
<div class="jumbotron">
	<img src="../img/jumbotron.jpg" alt="">
    <h1> We treat your pets like our own</h1>
    <p>At Wisdom Pet Medicine, we strive to blend the best in traditional   and alternative healing techniques to diagnose and treat companion   animals, including dogs, cats, birds, reptiles, rodents, and fish. </p>
</div>
```

Sample source code ada pada file cobagrid/cobajumbotron.html.

### Exercise ###

Saya memiliki sebuah tampilan html seperti dibawah ini. Buatlah html tersebut supaya lebih rapi.

```html
<!doctype html>
<html>
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="css/bootstrap.min.css">
    <title>Belajar Bootstrap</title>
</head>
<body>
<div class="container">
	<div class="container">
    	<div class="row">
            <article>
                <h1> Our Veterinarians Bring Extensive Experience</h1>
                <p>Wisdom Pet Medicine was founded by Dr. Darren Winthrop, Dr.    Elizabeth Chase, and Dr. Kimberly Sanders to bring the best in   traditional and  alternative medicine to the local community. The three   doctors met while pursuing  their veterinary education at Colorado State   University, one of the nation's  top-rated vet schools. After going   their own ways (for almost a decade), to  work for different veterinary   clinics across the country, the doctors decided  it was time to combine   their diverse knowledge and skills under one practice at  Wisdom Pet   Medicine.</p>
                <p>Staying up on the latest technology and procedures, empowers us to   diagnose  and treat more conditions in-house, rather than having to ship   your pet out to  a specialist's office. Our goal is to help keep your   love ones comfortable by  keeping them in friendly and familiar   surroundings for the duration of their  care. </p>
                <p>Our veterinary hospital provides general and specialty vet  medicine,   and serves as a major surgical center in the region. We're often    referred difficult cases from other vet clinics throughout the region,   state,  and country, and even treat cases from other countries. </p>
                <p>We all love animals and strive to make your pet's experience as   positive  as possible. This is why we have a pet play yard in the back   of our clinic  where we give our overnight visitors regular time away   from the stress of  confinement and treatment. </p>
                <p>We  are proud to say that most of our patients come in wagging their   tails happily  on return visits – a true indicator that we've made them   feel safe and secure.  We're honored that you've entrusted your pet's   care to us, and we'll stand by  our commitment to provide the absolute   best in veterinary medicine.</p>
          <div class="row">
         	<div>
            	<img src="img/winthrop.jpg" alt="Dr. Winthrop with his dog, Missy" title="Dr. Winthrop with his dog, Missy">
                <p>Dr. Winthrop is the guardian of Missy, a three-year old Llaso mix, who   he adopted at the shelter (he just couldn't resist those sad eyes). Dr.   Winthrop is passionate about spay and neuter and pet adoption, and works   tireless hours outside the clinic, performing free spay and neuter   surgeries for the shelter.</p>
            </div>
            <div>
            	<img src="img/chase.jpg" alt="Dr Chase with Kibbles" title="Dr Chase with Kibbles">
                <p>Dr. Chase spends much of her free time helping the local bunny rescue   organization find homes for bunnies, such as Kibbles. This cuddly    Dalmatian bunny is part of the large Chase household, which also   includes two dogs, three cats, and a turtle.</p>
            </div>
            <div>
            	<img src="img/sanders.jpg" alt="Dr. Sanders with Leroy" title="Dr. Sanders with Leroy">
                <p>Leroy walked into Dr. Sanders' front door when she was moving into a new   house. After searching for weeks for Leroy's guardians, she decided to   make Leroy a part of her pet family. Leroy has settled into his new   home, and especially enjoys playing with Dr. Sanders' other cats.</p>
            </div>
         </div>
             </article>
             <aside>
                <img src="img/sick-puppy.jpg">
                <h2> We specialize in: </h2>
                <ul>
                  <li>General Wellness Care</li>
                  <li>Preventative Care</li>
                  <li>Emergency Care</li>
                  <li>Vaccinations</li>
                  <li>Diagnostics</li>
                  <li>Orthopedics</li>
                  <li>Dermatology</li>
                  <li>Oncology</li>
                  <li>Radiology</li>
                  <li>Ultrasound</li>
                </ul>
            </aside>
         </div>
	</div>

<!-- javascript -->
	<script src="js/jquery-latest.min.js"></script>
    <script src="js/bootstrap.min.js"></script>
</body>
</html>
```


### Bootstrap CSS ###

Bootstrap menyediakan support untuk secara otomatis mendekorasi tag html tertentu. Jadi ketika kita menggunakan tag html tersebut, akan secara otomatis diubah dan diperindah oleh bootstrap tanpa susah-susah kita menambahkan manual CSS didalamnya.

#### Typography dan Blockquote ####

Kita memiliki tampilan html seperti dibawah ini.

```html
<div class="container">
    <!-- row 1 -->
    <header class="row">
    	<div class="col-lg-6 col-sm-5">
        	<a href="index.html"><img src="img/logo.png" alt="Wisdom Pets. click for home."></a>
        </div>
    	<div class="col-lg-6 col-sm-7">
        	<img src="img/animals.jpg" alt="">
        </div>
    </header>

    <!-- row 2 -->
    <div class="jumbotron">
    	<img src="img/jumbotron.jpg" alt="" class="pull-right">
        <h1> We treat your pets like our own</h1>
        <p>At Wisdom Pet Medicine, we strive to blend the best in traditional   and alternative healing techniques to diagnose and treat companion   animals, including dogs, cats, birds, reptiles, rodents, and fish. </p>
    </div>

    <!-- row 3 -->
    <div class="row">
    	<div class="col-md-3 col-xs-6">
            <p><img src="img/gsd.jpg" alt=""></p>
            <h4>Thanks for helping our German Shepherd</h4>
            <p>Tonto is severely allergic to over a dozen kinds of grass pollens. Thanks to Wisdom for the testing that tracked down his allergy!</p>
            <p><a href="#">Read more >></a></p>
        </div>
        <div class="col-md-3 col-xs-6">
            <p><img src="img/kitten.jpg" alt=""></p>
            <h4>Our diabetic kitty is better</h4>
            <p>When Samantha, our sweet kitten, began sleeping all the time and urinating excessively, we brought her to see the specialists at Wisdom. After running a blood test, Dr. Winthrop confirmed what we all feared – Samantha was showing signs of diabetes. </p>
            <p><a href="#">Read more >></a></p>
        </div>
        <div class="col-md-3 col-xs-6">
            <p><img src="img/bulldog.jpg" alt=""></p>
            <h4>Our grape-loving dog</h4>
            <p>The staff at Wisdom worked tirelessly to determine why our three-year old bulldog, Roxie, started going into sudden kidney failure. They stabilized her and provided fluids until her kidneys were again functioning normal, but it was still a mystery as to what caused her health to decline so quickly. </p>
            <p><a href="#">Read more >></a></p>
        </div>
        <div class="col-md-3 col-xs-6">
            <p><img src="img/goldfish.jpg" alt=""></p>
            <h4>A dog antibiotic cured our fish</h4>
            <p>Wisdom Pet Medicine is the only clinic around that will even book pet fish for appointments. When our 13-year old goldfish, McAllister, turned from silvery white to an angry red, we called around, urgently trying to find a veterinarian who could help. Wisdom not only got us in the same day, but also was able to diagnose McAllister as having a severe case of septicemia. </p>
             <p><a href="#">Read more >></a></p>
         </div>
    </div>

    <!-- row 4 -->
    <footer class="row">
         <p>This not a real veterinary medicine site, and is not meant to diagnose or offer treatment. Please see your veterinarian for all matters related to your pet's health.</p>
         <p>Wisdom Pet Medicine is a training brand owned by lynda.com.</p>
    </footer>

</div> <!-- end container -->
```

##### Nyoba Typography dan Blockquote #####

Pada bagian footer kita ingin menampilkan tulisan tersebut menjadi lebih kecil. Kita ganti tag `p` pada bagian tersebut dengan tag `small`. Dan pada bagian row 3 kita akan ganti tag `p` menggunakan tag `blockquote`.

Sample source code ada pada file cobastyle/cobatypo.html.

#### Hidden ####

Pada contoh kita yang sebelumnya, kita memiliki tampilan seperti dibawah ini.

```html
<div class="container">
    <!-- row 1 -->
    <header class="row">
    	<div class="col-lg-6 col-sm-5">
        	<a href="index.html"><img src="img/logo.png" alt="Wisdom Pets. click for home."></a>
        </div>
    	<div class="col-lg-6 col-sm-7">
        	<img src="img/animals.jpg" alt="">
        </div>
    </header>

    <!-- row 2 -->
    <div class="row">
    	<article class="col-lg-offset-1 col-sm-offset-1 col-lg-8 col-sm-7 col-lg-push-3 col-sm-push-4">
            <h1>Services</h1>
            <p><img src="img/cockatiel.jpg" class="pull-right">Wisdom Pet Medicine is a state-of-the-art veterinary hospital,   featuring the latest in diagnostic and surgical equipment, and a staff   of seasoned veterinary specialists in the areas of general veterinary   medicine and surgery, oncology, dermatology, orthopedics, radiology,   ultrasound, and much more. We also have a 24-hour emergency clinic in   the event your pet needs urgent medical care after regular business   hours.</p>
            <p>At Wisdom, we strive to be your pet&rsquo;s medical experts from youth   through the senior years. We build preventative health care plans for   each and every one of our patients, based on breed, age, and sex, so   that your pet receives the most appropriate care at crucial milestones   in his or her life. Our overarching goal is to give your pet the best   shot possible at a long and healthy life, by practicing simple   preventative care. We even provide an online Pet Portal where you can   view all your pet&rsquo;s diagnostic results, treatment plans, vaccination and   diagnostic schedules,  prescriptions, and any other health records.</p>
                        <!-- nested row 3 -->
            <div class="row">
                <div class="col-md-3 col-xs-6">
                    <h4>Vaccinations</h4>
                    <p>Dogs and cats are susceptible to a variety of illnesses that can be completely prevented.</p>
                    <p><a href="#">Read more >></a></p>
                </div>
                <div class="col-md-3 col-xs-6">
                    <h4>Checkups</h4>
                    <p>Regular checkups are a key factor in pet wellness, and can often unearth problems that could lead to health issues down the road.  </p>
                    <p><a href="#">Read more >></a></p>
                </div>
                <div class="col-md-3 col-xs-6">
                    <h4>Senior Pets</h4>
                    <p>Senior pets generally require more medical attention than their younger counterparts, just as senior humans do. So when is a pet considered “senior”? </p>
                    <p><a href="#">Read more >></a></p>
                </div>
                <div class="col-md-3 col-xs-6">
                    <h4>Diet Plans</h4>
                    <p>Wisdom veterinarians have all had extensive training in pet nutrition and are your best resources when considering changing your pet’s diet. </p>
                     <p><a href="#">Read more >></a></p>
                 </div>
            </div><!-- end nested row 3 -->
        </article>
        <aside class="col-lg-3 col-sm-4 col-lg-pull-9 col-sm-pull-8">
        	<h3>Keeping your pet's chompers clean and healthy</h3>
            <p>You know the importance of brushing your own teeth, but did you know that dogs and cats also need regular attention to their pearly whites? Poor dental hygiene in pets can lead to periodontal disease, a bacterial infection which causes bad breath, drooling, tooth decay, and tooth loss.</p>
            <p>As always, if you have questions about your pet’s dental or health care, please <a href="#">contact Wisdom Pet Medicine</a> for advice.</p>
         </aside>

        </div><!-- end row 2 -->

    <!-- row 4 -->
    <footer class="row">
         <p><small>This not a real veterinary medicine site, and is not meant to diagnose or offer treatment. Please see your veterinarian for all matters related to your pet's health.</small></p>
         <p><small>Wisdom Pet Medicine is a training brand owned by lynda.com.</small></p>
    </footer>

</div> <!-- end container -->
```

Pada saat tampilan dari html tersebut kita kecilkan, maka gambar kucing dipojok kanan atas akan turun kebawah.

##### Nyoba Hidden #####

Saat ukuran browser dikecilkan kita ingin supaya gambar kucing dipojok kanan atas tersebut tidak tampil / disembunyikan.

Caranya cukup mudah, tambahkan syntax berikut kedalam tag img `class="hidden-xs"`.

Sample source code ada pada file cobastyle/cobahidden.html.

#### Button ####

Pada tampilan html kita yang sebelumnya, ada bagian read more yang berupa link.

```html
<div class="container">
    <!-- row 1 -->
    <header class="row">
    	<div class="col-lg-6 col-sm-5">
        	<a href="index.html"><img src="../img/logo.png" alt="Wisdom Pets. click for home."></a>
        </div>
    	<div class="col-lg-6 col-sm-7">
        	<img src="../img/animals.jpg" alt="">
        </div>
    </header>

    <!-- row 2 -->
    <div class="jumbotron">
    	<img src="../img/jumbotron.jpg" alt="" class="pull-right">
        <h1> We treat your pets like our own</h1>
        <p>At Wisdom Pet Medicine, we strive to blend the best in traditional   and alternative healing techniques to diagnose and treat companion   animals, including dogs, cats, birds, reptiles, rodents, and fish. </p>
    </div>

    <!-- row 3 -->
    <div class="row">
    	<div class="col-md-3 col-xs-6">
            <p><img src="../img/gsd.jpg" alt=""></p>
            <h4>Thanks for helping our German Shepherd</h4>
            <blockquote>Tonto is severely allergic to over a dozen kinds of grass pollens. Thanks to Wisdom for the testing that tracked down his allergy!</blockquote>
            <p><a href="#">Read more >></a></p>
        </div>
        <div class="col-md-3 col-xs-6">
            <p><img src="../img/kitten.jpg" alt=""></p>
            <h4>Our diabetic kitty is better</h4>
            <p>When Samantha, our sweet kitten, began sleeping all the time and urinating excessively, we brought her to see the specialists at Wisdom. After running a blood test, Dr. Winthrop confirmed what we all feared – Samantha was showing signs of diabetes. </p>
            <p><a href="#">Read more >></a></p>
        </div>
        <div class="col-md-3 col-xs-6">
            <p><img src="../img/bulldog.jpg" alt=""></p>
            <h4>Our grape-loving dog</h4>
            <p>The staff at Wisdom worked tirelessly to determine why our three-year old bulldog, Roxie, started going into sudden kidney failure. They stabilized her and provided fluids until her kidneys were again functioning normal, but it was still a mystery as to what caused her health to decline so quickly. </p>
            <p><a href="#">Read more >></a></p>
        </div>
        <div class="col-md-3 col-xs-6">
            <p><img src="../img/goldfish.jpg" alt=""></p>
            <h4>A dog antibiotic cured our fish</h4>
            <p>Wisdom Pet Medicine is the only clinic around that will even book pet fish for appointments. When our 13-year old goldfish, McAllister, turned from silvery white to an angry red, we called around, urgently trying to find a veterinarian who could help. Wisdom not only got us in the same day, but also was able to diagnose McAllister as having a severe case of septicemia. </p>
             <p><a href="#">Read more >></a></p>
         </div>
    </div>

    <!-- row 4 -->
    <footer class="row">
         <p><small>This not a real veterinary medicine site, and is not meant to diagnose or offer treatment. Please see your veterinarian for all matters related to your pet's health.</small></p>
         <p><small>Wisdom Pet Medicine is a training brand owned by lynda.com.</small></p>
    </footer>

</div> <!-- end container -->
```

Kita ingin mengubah supaya link tersebut lebih enak dilihat.

##### Nyoba Button #####

Coba kita tambahkan syntax berikut pada masing-masing link read more tersebut `class="btn btn-primary"`.

Sample source code ada pada file cobastyle/cobabutton.html.

#### Image Responsive ####

Pada contoh kita yang sebelumnya ketika kita mengecilkan browser tampilan html akan menyesuaikan ukurannya. Akan tetapi hanya berpengaruh pada text saja.

##### Nyoba Image Responsive #####

Bagaimana caranya supaya gambar / image kita juga ikut menyesuaikan ketika browser diperkecil ukurannya.

Caranya mudah, cukup tambahkan `class="img-responsive"` disetiap gambar yang kita punya. Pada gambar jumbotron selain kita buat responsive kita buat supaya tampilan gambarnya berupa oval / lingkaran, caranya tambahkan style berikut `class="img-responsive img-circle"`

Sample source code ada pada file cobastyle/cobaimageresponsive.html.

#### Glyphicon ####

Buka kembali file html pada contoh yang sebelumnya.

```html
<div class="container">
    <!-- row 1 -->
    <header class="row">
    	<div class="col-lg-6 col-sm-5">
        	<a href="index.html"><img src="../img/logo.png" alt="Wisdom Pets. click for home."></a>
        </div>
    	<div class="col-lg-6 col-sm-7">
        	<img src="../img/animals.jpg" alt="" class="hidden-xs">
        </div>
    </header>

    <!-- row 2 -->
    <div class="row">
    	<article class="col-lg-offset-1 col-sm-offset-1 col-lg-8 col-sm-7 col-lg-push-3 col-sm-push-4">
            <h1>Services</h1>
            <p><img src="../img/cockatiel.jpg" class="pull-right">Wisdom Pet Medicine is a state-of-the-art veterinary hospital,   featuring the latest in diagnostic and surgical equipment, and a staff   of seasoned veterinary specialists in the areas of general veterinary   medicine and surgery, oncology, dermatology, orthopedics, radiology,   ultrasound, and much more. We also have a 24-hour emergency clinic in   the event your pet needs urgent medical care after regular business   hours.</p>
            <p>At Wisdom, we strive to be your pet&rsquo;s medical experts from youth   through the senior years. We build preventative health care plans for   each and every one of our patients, based on breed, age, and sex, so   that your pet receives the most appropriate care at crucial milestones   in his or her life. Our overarching goal is to give your pet the best   shot possible at a long and healthy life, by practicing simple   preventative care. We even provide an online Pet Portal where you can   view all your pet&rsquo;s diagnostic results, treatment plans, vaccination and   diagnostic schedules,  prescriptions, and any other health records.</p>
                        <!-- nested row 3 -->
            <div class="row">
                <div class="col-md-3 col-xs-6">
                    <h4>Vaccinations</h4>
                    <p>Dogs and cats are susceptible to a variety of illnesses that can be completely prevented.</p>
                    <p><a href="#">Read more >></a></p>
                </div>
                <div class="col-md-3 col-xs-6">
                    <h4>Checkups</h4>
                    <p>Regular checkups are a key factor in pet wellness, and can often unearth problems that could lead to health issues down the road.  </p>
                    <p><a href="#">Read more >></a></p>
                </div>
                <div class="col-md-3 col-xs-6">
                    <h4>Senior Pets</h4>
                    <p>Senior pets generally require more medical attention than their younger counterparts, just as senior humans do. So when is a pet considered “senior”? </p>
                    <p><a href="#">Read more >></a></p>
                </div>
                <div class="col-md-3 col-xs-6">
                    <h4>Diet Plans</h4>
                    <p>Wisdom veterinarians have all had extensive training in pet nutrition and are your best resources when considering changing your pet’s diet. </p>
                     <p><a href="#">Read more >></a></p>
                 </div>
            </div><!-- end nested row 3 -->
        </article>
        <aside class="col-lg-3 col-sm-4 col-lg-pull-9 col-sm-pull-8">
        	<h3>Keeping your pet's chompers clean and healthy</h3>
            <p>You know the importance of brushing your own teeth, but did you know that dogs and cats also need regular attention to their pearly whites? Poor dental hygiene in pets can lead to periodontal disease, a bacterial infection which causes bad breath, drooling, tooth decay, and tooth loss.</p>
            <p>As always, if you have questions about your pet’s dental or health care, please <a href="#">contact Wisdom Pet Medicine</a> for advice.</p>
         </aside>

        </div><!-- end row 2 -->

    <!-- row 4 -->
    <footer class="row">
         <p><small>This not a real veterinary medicine site, and is not meant to diagnose or offer treatment. Please see your veterinarian for all matters related to your pet's health.</small></p>
         <p><small>Wisdom Pet Medicine is a training brand owned by lynda.com.</small></p>
    </footer>

</div> <!-- end container -->
```

##### Nyoba Glyphicon #####

Kita ingin menambahkan icon pada bagian nested row didalam article. Karena bootstrap sudah menyediakan berbagai macam icon, kita bisa dapat langsung menggunakannya.

Caranya dengan menambahkan syntax berikut.

```html
<span class="glyphicon glyphicon-pushpin"></span>
<span class="glyphicon glyphicon-ok"></span>
<span class="glyphicon glyphicon-heart"></span>
<span class="glyphicon glyphicon-cutlery"></span>
```

Sample source code ada pada file cobastyle/cobaglyphicon.html.

















