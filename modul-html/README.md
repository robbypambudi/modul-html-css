# Daftar Isi

- [Daftar Isi](#daftar-isi)
- [Persiapan](#persiapan)
- [HTML](#html)
  - [Dokumen HTML](#dokumen-html)
  - [Elemen, Tag, Attribut](#elemen-tag-attribut)
    - [Elemen](#elemen)
    - [Tag](#tag)
    - [Atribut](#atribut)
  - [Cara Kerja HTML](#cara-kerja-html)
  - [Struktur HTML](#struktur-html)
  - [Layout Dasar](#layout-dasar)
  - [Judul dan Paragraf](#judul-dan-paragraf)
    - [Tag Judul](#tag-judul)
    - [Tag Paragraf](#tag-paragraf)
    - [Tag Tautan](#tag-tautan)
    - [Tag Gambar](#tag-gambar)
    - [Tag Daftar (List)](#tag-daftar-list)
    - [Tag Table](#tag-table)
    - [Tag Form & Input](#tag-form--input)
    - [Tag div & span](#tag-div--span)

# Persiapan

Sebelum memulai materi, terdapat beberapa hal yang perlu dipersiapkan:

1. Web Browser <br/>
   Contoh: Google Chrome (recommended), Mozilla Firefox, Microsoft Edge, atau Safari.
2. Text Editor <br/>
   Contoh: [Visual Studio Code](https://code.visualstudio.com/download) (recommended), Sublime Text, Atom, [Notepad++](https://notepad-plus-plus.org/downloads/v8.4.5/), atau Notepad.

# HTML

HTML atau Hypertext Markup Language adalah bahasa markup standar yang digunakan untuk membuat halaman website. HTML mendeskripsikan struktur dari halaman website yang akan ditampilkan pada web browser seperti Chrome, Edge, Safari dll.

## Dokumen HTML

Dalam menulis HTML, kode HTML akan disimpan dalam suatu file yang memiliki **.html** atau **.htm** di akhir nama file. Contoh : index<strong>.html</strong> atau index<strong>.htm</strong>

## Elemen, Tag, Attribut

Sebelum masuk lebih jauh, kita akan melihat tiga istilah utama yang harus diketahui ketika menulis HTML. Ketiga istilah tersebut adalah **elemen**, **tag**, dan **atribut**.

### Elemen

Elemen HTML merupakan komponen/bagian yang menetapkan peran sebuah objek dalam dokumen, termasuk struktur dan konten dari objek tersebut.

Contoh:

```html
<h1>Ini adalah judul utama.</h1>
<p>Ini adalah paragraf.</p>
```

Berdasarkan contoh kode diatas elemen `h1` digunakan untuk membuat tulisan yang berperan sebagai judul utama atau heading 1. Sedangkan elemen `p` digunakan untuk membuat tulisan yang berperan sebagai paragraf.

### Tag

Sebuah elemen biasanya dinyatakan dengan tag. Tag pembuka menandakan awal dari sebuah elemen, dan tag penutup menandakan akhir dari sebuah elemen. Tag pembuka dinyatakan dengan nama elemen yang diapit simbol kurang dari (<) dan lebih dari (>), contohnya `<h1>`. Tag penutup dituliskan dengan menambahkan garis miring (/) setelah simbol kurang dari (<). Misalnya, tag penutup untuk elemen `h1` adalah `</h1>`.

### Atribut

Atribut merupakan informasi tambahan yang dapat kita berikan pada sebuah elemen. Setiap elemen memiliki atribut yang berbeda-beda, namun terdapat beberapa atribut standar yang dapat digunakan oleh semua elemen.

Atribut khusus elemen merupakan atribut yang hanya dapat digunakan pada elemen tersebut. Sebagai contoh, pada elemen `img` yang digunakan untuk menampilkan gambar, terdapat atribut `src` untuk menentukan sumber gambar yang akan ditampilkan. Atribut ini tentunya tidak akan berguna untuk elemen `p`, yang hanya menampilkan teks.

Atribut standar yang dimiliki oleh semua elemen sendiri merupakan atribut yang umumnya dapat diimplementasikan oleh semua elemen, misalnya atribut `id` untuk identifikasi elemen, atau atribut `class` untuk melakukan penggolongan elemen.

Kode di bawah menunjukkan contoh elemen `a` yang digunakan dengan atribut wajib elemen tersebut yakni `href`:

```html
<a href="http://www.google.com">Ini adalah sebuah link yang akan membuka google</a>
```

Kode di atas memberikan contoh atribut `href` yang dimiliki oleh elemen `a`. Atribut ini berguna untuk menentukan link yang akan dituju ketika dibuka dari sebuah elemen (nama “href” sendiri merupakan kepanjangan dari hyperlink reference). Sedangkan kode berikut menunjukkan contoh elemen `img` yang digunakan dengan atribut khusus elemen tersebut yakni `src`:

```html
<img src="gambar.jpg" width="104" height="142">
```

Atribut-atribut yang dimiliki oleh tiap-tiap elemen akan dibahas lebih lanjut pada pembahasan masing-masing elemen.

## Cara Kerja HTML

Aturan pertama dalam penulisan kode HTML adalah mengapit teks dengan **tag**. Elemen HTML didefinisikan dengan tag pembuka, suatu konten, dan tag penutup, seperti yang sudah dijelaskan sebelumnya sebagai berikut:

```html
<namaelemen>Konten diketikkan disini</namaelemen>
```

> Catatan: <br>Namun terdapat beberapa elemen HTML yang tidak memiliki konten salah satunya `<br>`. Elemen tersebut dapat disebut sebagai elemen yang kosong. Oleh karena itu elemen kosong tidak memiliki tag penutup (`</namaelemen>`).

## Struktur HTML

Ada beberapa aturan dalam membuat dokumen HTML. Semua dokumen HTML harus dimulai dengan penjelasan tipe dokumen, dalam hal ini kita harus menyertakan `<!DOCTYPE html>` sebelum tag HTML lainnya. Selain itu dalam HTML, elemen `<head>` dan `<body>` wajib berada di dalam elemen `<html>` sebagai berikut:

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <title>Judul Halaman</title>
    <link rel="stylesheet" href="stylesheet.css" />
  </head>
  <body>
    <h1>Ini adalah judul utama.</h1>
    <p>Ini adalah paragraf.</p>
  </body>
</html>
```

Berdasarkan contoh struktur HTML diatas, perlu diketahui:

1. `<!DOCTYPE html>` <br/>
   Ini akan menentukan versi HTML secara otomatis sehingga versi HTML situs web yang dibuat merupakan versi yang terbaru.
2. `<head>` <br/>
   Berisi informasi dokumen atau settingan dokumen HTML yang tidak terlihat ketika membuka halaman. Ada tiga elemen yang harus diletakkan di dalam `<head>` yaitu:
   - Pengkodean karakter (encoding) <br/>
     `<meta charset="utf-8">` untuk memastikan situs web menggunakan pengkodean karakter yang konsisten. UTF-8 adalah pengkodean karakter yang direkomendasikan untuk HTML5.
   - Judul situs web <br/>
     `<title>Judul Halaman</title>` judul yang muncul pada tab / bagian atas browser.
   - Hubungan dengan file CSS <br/>
     `<link rel="stylesheet" href="stylesheet.css">` agar HTML dapat terhubung dengan file CSS yang diinginkan, kita perlu menghubungkannya menggunakan elemen ini.
3. `<body>` <br/>
   Berisi konten yang terlihat di browser

## Layout Dasar

Layout atau tata letak adalah salah satu bagian paling penting dalam membuat situs web. Dengan menentukan terlebih dahulu layout dari suatu web yang ingin kita buat, dapat memudahkan kita dalam penataan elemen-elemen yang dibutuhkan.

![image1](https://user-images.githubusercontent.com/68275535/130474382-c674fb7f-72ef-4161-99f5-d7eed63104dd.png)

**Elemen Header**

Seperti namanya, header merupakan elemen yang berisi judul dan penjelasan lain situs web. Biasanya elemen ini diisikan dengan logo website, menu-menu umum (seperti login dan logout), maupun nama halaman yang sedang ditampilkan.

**Elemen Navigation**

Elemen navigasi, yang memberikan akses navigasi ke halaman-halaman lain dalam web.

**Elemen Sidebar**

Elemen ini merupakan hal-hal yang menjadi pendukung konten, dapat berupa pembantu navigasi konten seperti daftar isi, ataupun berbagai hal lain seperti daftar konten lain, iklan, atau menu tambahan. Sidebar dapat berada di kiri atau kanan konten, atau bahkan di kiri dan kanan konten, sesuai dengan kreatifitas perancangnya.

**Elemen Content**

Elemen ini merupakan isi utama dari situs web. Pengguna biasanya datang ke web untuk melihat teks yang berada pada bagian ini.

**Elemen Footer**

Bagian penutup dari website, yang dapat berisi informasi lain tentang website, seperti lisensi penggunaan, link ke halaman lain, ataupun link ke website lain.

Nah lalu bagaimana kita dapat membuat layout seperti contoh di atas? Kita dapat menggunakan tag `<div>` maupun tag yang telah tersedia seperti `<header>`, `<footer>`, dll.

## Judul dan Paragraf

### Tag Judul

Tag judul digunakan untuk memformat elemen judul. Tag ini bervariasi mulai dari `<h1>` hingga `<h6>`. Yang mana semakin besar angka semakin kecil ukuran textnya.

```html
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>
```

### Tag Paragraf

Paragraf digunakan untuk menulis teks biasa. Sebuah paragraf selalu dimulai pada baris baru, dan pada paragraf tersebut terdapat margin/jarak pada bagian atas dan bawahnya. Untuk membuat paragraf dapat menggunakan tag `<p>`.

```html
<p>Paragraf pertama</p>
<p>Paragraf kedua</p>
```

### Tag Tautan

Kita dapat dengan mudah membuat tautan dengan menggunakan tag `<a>`. Teks yang berada di dalam tag tersebut akan ditampilkan pada browser sebagai teks tautan/teks yang dapat di-klik.

```html
<a href="https://www.google.com">Buka Google</a>
```

Setiap tautan memiliki link tujuan, maka dari itu agar tautan berfungsi kita harus menentukan URL tujuan dengan menambahkan atribut `href`. Seperti kode yang telah dijabarkan di atas, di mana isi dari atribut `href` bernilai alamat URL `https://www.google.com`.

### Tag Gambar

Tag `<img>` digunakan untuk menampilkan gambar. Kita dapat menetapkan gambar dengan menentukan sumber gambar di atribut `src`. Sumber gambar tersebut dapat kita arahkan ke penyimpanan lokal (folder yang ada di komputer) ataupun gambar yang ada di internet dengan menggunakan URL/link gambar tersebut.

```html
<img src="./folder gambar/foto.jpg" alt="Foto formal" height="60px" width="40px" />
```

Pada contoh tersebut kita mengisi atribut `src` dengan file yang berada di dalam folder gambar bernama `foto.jpg`. Adapula atribut lain seperti `alt` digunakan sebagai deskripsi alternatif dari gambar yang mana deskripsi ini akan ditampilkan apabila sumber gambar tidak dapat terbuka. Atribut `height` dan `width` digunakan untuk menentukan ukuran dari gambar, dalam contoh ini kita menggunakan satuan pixel sebagai ukuran gambar.

### Tag Daftar (List)

Terdapat 3 macam daftar yang dapat kita gunakan dalam HTML, yakni:

1. Unordered List (`ul`) <br/>
   Merupakan daftar yang tidak memiliki nomor urut. Penggunaan unordered list akan menghasilkan daftar dengan awalan suatu simbol, secara bawaan  simbol yang digunakan yakni simbol lingkaran (●). Untuk mengisi listnya kita dapat mengapit konten dengan tag `<li>`.

   ```html
   <h2>Contoh unordered list</h2>
   <ul>
     <li>Kopi</li>
     <li>Teh</li>
     <li>Susu</li>
   </ul>
   ```

   Ilustrasi:

   ![image1](https://user-images.githubusercontent.com/33245436/191101791-ade86151-457d-44a7-8a9a-72ba6824c098.png)
   
2. Ordered List (`ol`) <br/>
   Merupakan daftar yang yang memiliki nomor urut dengan awalan angka. Untuk mengisi listnya kita menggunakan tag `<li>`.

   ```html
   <h2>Contoh ordered list</h2>
   <ol>
     <li>Kopi</li>
     <li>Teh</li>
     <li>Susu</li>
   </ol>
   ```

   Ilustrasi:

   ![image2](https://user-images.githubusercontent.com/33245436/191101927-e885a3c6-ae4b-4756-ba4a-198d50496917.png)

3. Description List (`dl`) <br/>
   Merupakan daftar yang digunakan jika ingin menambahkan deskripsi untuk tiap daftar. Dengan menggunakan tag `<dt>` untuk mendefinisikan nama bagian dan tag `<dd>` untuk mendefinisikan deskripsinya.

   ```html
   <h2>Contoh description list</h2>
   <dl>
     <dt>Kopi</dt>
     <dd>Minuman pahit</dd>
     <dt>Susu</dt>
     <dd>Minuman manis</dd>
   </dl>
   ```

   Ilustrasi:

   ![image3](https://user-images.githubusercontent.com/33245436/191102126-5b3afdbd-6873-4e7e-a947-0b385bd7a9c7.png)

### Tag Table

Jika ingin membuat sebuah tabel pada website, maka kita dapat menggunakan tag `<table>`. Kemudian untuk membuat baris tabel kita dapat menggunakan tag `<tr>` (table row), lalu untuk membuat judul pada tabel kita dapat menggunakan tag `<th>` (table header), dan untuk isi dari tabel kita dapat menggunakan tag `<td>` (table data).

```html
<table>
  <tr>
    <th>No</th>
    <th>Nama</th>
  </tr>
  <tr>
    <td>1</td>
    <td>Ani</td>
  </tr>
  <tr>
    <td>2</td>
    <td>Boge</td>
  </tr>
</table>
```

Ilustrasi:

![image4](https://user-images.githubusercontent.com/68275535/130475305-df78906b-d4ff-4e4a-82c4-ce1befc797c5.png)

### Tag Form & Input

Jika kita ingin membuat suatu form dalam website maka kita dapat menggunakan tag `<form>` yang mana tag tersebut adalah wadah untuk berbagai jenis elemen input seperti: `fields`, `checkboxes`, `radio buttons`, `submit buttons`, dan masih banyak lainnya.

Atribut dari `<form>` yaitu:

1. Action <br/>
   Atribut yang mendefinisikan aksi yang akan dilakukan ketika formulir dikirimkan. Biasanya data formulir dikirim ke file di server ketika pengguna mengklik tombol kirim.

   Nilai dari atribut ini berupa URL. Contoh: `/simpan.php`.

2. Target <br/>
   Menentukkan tempat dari respon yang diterima setelah mengirim form.

   ![image5](https://user-images.githubusercontent.com/68275535/130475395-1778983d-d9cd-41a3-8126-3f2c4ae480c3.png)

3. Method <br/>
   Menentukkan metode HTTP yang digunakan oleh browser untuk mengirim data form.

   Nilainya berupa HTTP request method seperti `GET` apabila browser ingin mendapatkan data, kemudian terdapat request method `POST` apabila browser ingin mengirimkan data, dan masih banyak request method lainnya.

4. Autocomplete <br/>
   Menentukkan apakah kolom input dapat secara otomatis terisi atau tidak. Hal ini dilakukan secara otomatis (jika on) oleh browser dengan menampilkan tulisan yang sebelumnya pernah ditulis pada browser tersebut untuk menghindari penulisan berulang kali.

   Nilainya berupa `on` atau `off`.

Adapula elemen yang dapat digunakan untuk melengkapi sebuah form, diantaranya adalah sebagai berikut:

- `<button>`
- `<fieldset>`
- `<input>`
- `<label>`
- `<legend>`
- `<optgroup>`
- `<option>`
- `<select>`
- `<textarea>`

Adapun untuk input terdapat banyak jenisnya

- `<input type="text">`
- `<input type="password">`
- `<input type="number">`
- `<input type="email">`
- `<input type="radio">`
- `<input type="checkbox">`
- `<input type="file">`
- `<input type="hidden">`
- dan masih banyak lainnya

Contoh penggunaan tag `<form>` beserta inputnya

```html
<form action="#" method="post">
  <input type="text">
  <input type="password">
  <input type="radio" id="html" name="fav_language" value="HTML">
  <label for="html">HTML</label><br>
  <input type="radio" id="css" name="fav_language" value="CSS">
  <label for="css">CSS</label><br>
  <button type="submit">
</form>
```

Sangat banyak sekali atribut baik dari elemen yang dapat digunakan di dalam tag form ataupun atribut dari tag input itu sendiri. Maka untuk mempelajari lebih dalam bisa melalui https://www.w3schools.com/html/html_forms.asp

### Tag div & span

Tag `<div>` merupakan block-level elemen yakni elemen yang selalu dimulai dengan baris baru. Div dapat dikatakan pula sebagai container / wadah untuk elemen-elemen html. Pada tag ini kita dapat menggunakan atribut `style`, `class`, atau `id` untuk mempermudah styling dengan CSS yang akan kita pelajari pada materi selanjutnya.

```html
<div style="background-color:black;color:white;padding:20px;">
  <h2>London</h2>
  <p>
    London is the capital city of England. It is the most populous city in the
    United Kingdom, with a metropolitan area of over 13 million inhabitants.
  </p>
  <p>
    Standing on the River Thames, London has been a major settlement for two
    millennia, its history going back to its founding by the Romans, who named
    it Londinium.
  </p>
</div>
```

Ilustrasi:

![image6](https://user-images.githubusercontent.com/68275535/130475539-a8db8730-46e2-4996-8e1a-0829a163225e.png)

Tag <span> merupakan inline-level elemen yakni elemen yang tidak dimulai dengan baris baru. Sama seperti div, tag ini merupakan wadah untuk menandai bagian dari teks, atau bagian dari dokumen.

```html
<p>
  My mother has <span style="color: blue; font-weight: bold">blue</span>eyes and
  my father has
  <span style="color: darkolivegreen; font-weight: bold">dark green</span>
  eyes.
</p>
```

Ilustrasi:

![image7](https://user-images.githubusercontent.com/68275535/130475641-578b3af0-ee2a-449e-8758-f4ec1e223761.png)
  
## Referensi

- https://www.w3schools.com/
- http://dev.bertzzie.com/knowledge/desain-web-dasar/HTMLdanCSSDasar.html
- http://dev.bertzzie.com/knowledge/desain-web-dasar/Layout.html#
