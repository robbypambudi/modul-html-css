# Daftar Isi

- [Daftar Isi](#daftar-isi)
- [Persiapan](#persiapan)
- [CSS](#css)
  - [Sintaks](#sintaks)
  - [Cara Menggunakan CSS](#cara-menggunakan-css)
  - [Selector](#selector)
    - [Simple Selector](#simple-selector)
    - [Combinator Selector](#combinator-selector)
    - [Pseudo-class Selector](#pseudo-class-selector)
    - [Pseudo-element Selector](#pseudo-element-selector)
    - [Attribute Selector](#attribute-selector)
  - [Property dan Value](#property-dan-value)
    - [Colors](#colors)
    - [Box Model](#box-model)
  - [Specificity](#specificity)

# Persiapan

Sebelum memulai materi, terdapat beberapa hal yang perlu dipersiapkan:

1. Web Browser <br/>
   Contoh: Google Chrome (recommended), Mozilla Firefox, Microsoft Edge, atau Safari.
2. Text Editor <br/>
   Contoh: [Visual Studio Code](https://code.visualstudio.com/download) (recommended), Sublime Text, Atom, [Notepad++](https://notepad-plus-plus.org/downloads/v8.4.5/), atau Notepad.

# CSS

CSS (Cascading Style Sheets) adalah bahasa yang digunakan untuk mendeskripsikan style sebuah halaman web, agar web lebih bagus secara visual. Jika HTML adalah elemen-elemen yang membangun kerangka halaman web, CSS dipakai untuk mempercantik elemen tersebut. CSS dapat digunakan untuk beberapa halaman web sekaligus.

## Sintaks

![image1](https://user-images.githubusercontent.com/68275535/130475766-8e0e2807-ab77-4b15-adc2-74fd92719117.png)

**Selector** adalah elemen HTML yang ingin dipilih dan di-styling / dihias. Kemudian pada bagian **declaration** (dibuka dan ditutup dengan kurung kurawal) terdapat **property** yakni hal yang ingin diubah dan **value** yakni nilai property yang ingin digunakan dan diaplikasikan pada elemen dipilih.

## Cara Menggunakan CSS

Terdapat tiga cara menggunakan CSS, yaitu:

1. Inline <br/>
   Menulis CSS di dalam sebuah elemen HTML, pada atribut `style` suatu elemen HTML. Contoh di bawah, elemen `h1` dan `p` menggunakan CSS metode inline.

   ```html
   <!DOCTYPE html>
   <html>
     <body>
       <h1 style="color:blue;text-align:center;">This is a heading</h1>
       <p style="color:red;">This is a paragraph.</p>
     </body>
   </html>
   ```

Ilustrasi:

![image2](https://user-images.githubusercontent.com/33245436/191103212-0392b09e-fb33-49ad-8bf0-ac14e37b57d0.png)

2. Internal <br/>
   Menulis CSS langsung pada file HTML itu juga, namun perbedaannya dengan inline penulisan CSS ini diletakkan pada elemen `style`.

   ```html
   <!DOCTYPE html>
   <html>
     <head>
       <style>
         body {
           background-color: lightblue;
         }

         h1 {
           color: maroon;
           margin-left: 40px;
         }
       </style>
     </head>
     <body>
       <h1>This is a heading</h1>
       <p>This is a paragraph.</p>
     </body>
   </html>
   ```

Ilustrasi:

![image3](https://user-images.githubusercontent.com/33245436/191103797-69c7229a-4d2e-474c-920c-282740023083.png)

3. Eksternal <br/>
   Menulis CSS pada file terpisah berekstensi ‘.css’ dan dihubungkan pada HTML dengan elemen `link` seperti berikut.

   ```html
   <!DOCTYPE html>
   <html>
     <head>
       <link rel="stylesheet" href="style.css" />
     </head>
     <body>
       <h1>This is a heading</h1>
       <p>This is a paragraph.</p>
     </body>
   </html>
   ```

   Lalu pada file `style.css`, isinya sebagai berikut.

   ```css
   body {
     background-color: lightblue;
   }

   h1 {
     color: navy;
     margin-left: 20px;
   }
   ```

Ilustrasi:

![image4](https://user-images.githubusercontent.com/33245436/191104574-998e320a-7d73-4cfb-901c-24085ad2cb77.png)

## Selector

**Selector** adalah pemiliham elemen HTML yang ingin diberi style. Ada beberapa kategori selector:

### Simple Selector

1. Element Selector <br/>
   Pada contoh di bawah, selectornya adalah `p`. Maka semua elemen `p` akan terpengaruh oleh styling CSS tersebut.

   ```html
   <!DOCTYPE html>
   <html>
     <head>
       <style>
         p {
           text-align: center;
           color: red;
         }
       </style>
     </head>
     <body>
       <p>Semua paragraf akan terpengaruh dengan styling yang ada.</p>
       <p id="para1">Aku pun!</p>
       <p>Apalagi aku!</p>
     </body>
   </html>
   ```

Ilustrasi:

![image5](https://user-images.githubusercontent.com/33245436/191104950-0ab0d796-fd3f-4c9e-82b9-e8b4f889a838.png)

2. ID Selector <br/>
   Pada contoh di bawah, elemen dengan id `para1` akan terpengaruh styling CSS.

   ```html
   <!DOCTYPE html>
   <html>
     <head>
       <style>
         #para1 {
           text-align: center;
           color: red;
         }
       </style>
     </head>
     <body>
       <p id="para1">Hello World!</p>
       <p>Paragraf ini tidak terpengaruh dengan styling yang ada.</p>
     </body>
   </html>
   ```

Ilustrasi:

![image6](https://user-images.githubusercontent.com/33245436/191105116-ad4d8100-5dd2-46ba-b451-910e3d0e8574.png)

3. Class Selector <br/>
   Pada contoh di bawah, elemen dengan class `center` akan terpengaruh styling CSS.

   ```css
   .center {
     text-align: center;
     color: red;
   }
   ```

   Kamu juga bisa select elemen dan class tertentu. Pada contoh di bawah, hanya elemen p dengan class `center` yang akan terpengaruh styling CSS.

   ```css
   p.center {
     text-align: center;
     color: red;
   }
   ```

   ```html
   <!DOCTYPE html>
   <html>
     <head>
       <link rel="stylesheet" href="style.css" />
     </head>
     <body>
       <p class="center">Hello Again World!</p>
       <p>Paragraf ini tidak terpengaruh dengan styling yang ada.</p>
     </body>
   </html>
   ```

Ilustrasi:

![image7](https://user-images.githubusercontent.com/33245436/191105288-1a54c1c3-981e-47eb-9eed-7256a4ab3b61.png)

4. Universal Selector <br/>
   Dengan memakai \* , kita dapat men-select keseluruhan dokumen HTML.

   ```css
   * {
     text-align: center;
     color: blue;
   }
   ```

Ilustrasi:

![image8](https://user-images.githubusercontent.com/33245436/191105597-5036bf13-0441-4e28-ab88-4b5c0b4fc277.png)

5. Grouping Selector <br/>
   Dengan koma, kita bisa menggabungkan beberapa selector. Pada contoh dibawah, elemen `h1`, `h2`, dan `p` akan terpengaruh oleh CSS.

   ```css
   h1, h2, p {
     text-align: center;
     color: red;
   }
   ```

   ```html
   <!DOCTYPE html>
   <html>
     <head>
       <link rel="stylesheet" href="style.css" />
     </head>
     <body>
       <h1>This is a heading</h1>
       <h2>This is second heading</h2>
       <h3>This is third heading, I'm different!</h3>
       <p>This is a paragraph.</p>
     </body>
   </html>
   ```

Ilustrasi:

![image9](https://user-images.githubusercontent.com/33245436/191105950-c83f80d9-9e00-4b39-8a87-62c9e8fee206.png)

### Combinator Selector

Combinator selector menggunakan lebih dari 1 simple selector. Ada 4 jenis combinator selector.

1. Descendant Selector (spasi) <br/>
   Memilih suatu elemen di dalam elemen. Pada contoh di bawah, memilih semua `p` di dalam semua `div`.

   ```css
   div p {
     background-color: yellow;
   }
   ```

   ```html
   <!DOCTYPE html>
   <html>
     <head>
       <link rel="stylesheet" href="style.css" />
     </head>
     <body>
       <div>
         <p>Hello World!</p>
         <section>
           <p>Paragraf ini terdampak!</p>
         </section>
       </div>
     </body>
   </html>
   ```

Ilustrasi:

![image10](https://user-images.githubusercontent.com/33245436/191108283-c6de80bd-9fba-4353-9418-ad48a41cb5b5.png)

2. Child Selector (>) <br/>
   Memilih semua child / anak dari suatu elemen. Perbedaan child selector dengan descendant selector yakni child selector hanya mempengaruhi anak elemennya, tidak mempengaruhi cucunya atau anak dari anak elemen yang dipilih. Pada contoh di bawah, kita memilih semua elemen `p1` yang merupakan anak dari `div`.

   ```css
   div > p {
     background-color: yellow;
   }
   ```

   ```html
   <!DOCTYPE html>
   <html>
     <head>
       <link rel="stylesheet" href="style.css" />
     </head>
     <body>
       <div>
         <p>Hello World!</p>
         <section>
           <p>Paragraf ini tidak terpengaruh dengan styling yang ada.</p>
         </section>
         <p>Tapi ini terdampak.</p>
       </div>
     </body>
   </html>
   ```

Ilustrasi:

![image11](https://user-images.githubusercontent.com/33245436/191108508-b4b340f3-e30d-4992-b460-d43bf21fffb8.png)

3. Adjacent Sibling Selector (+) <br/>
   Untuk memilih suatu elemen yang tepat setelah satu elemen tersebut. Pada contoh di bawah, memilih semua elemen `p` yang terletak tepat setelah `div` bukan di dalamnya.

   ```css
   div + p {
     background-color: yellow;
   }
   ```

   ```html
   <!DOCTYPE html>
   <html>
     <head>
       <link rel="stylesheet" href="style.css" />
     </head>
     <body>
       <div>
        <p>Ini tidak terdampak.</p>
       </div>
       <p>Tapi ini terdampak.</p>
       <p>Sementara aku tidak terdampak.</p>
     </body>
   </html>
   ```

Ilustrasi:

![image12](https://user-images.githubusercontent.com/33245436/191109307-dcba9bb1-38c1-491c-bb2e-657ff2721de5.png)

4. General Sibling Selector (~) <br/>
   Untuk memilih elemen yang merupakan semua saudara selanjutnya suatu elemen. Pada contoh di bawah, kita akan memilih semua elemen `p` yang merupakan saudara selanjutnya dari elemen `div`

   ```css
   div ~ p {
     background-color: yellow;
   }
   ```

   ```html
   <!DOCTYPE html>
   <html>
     <head>
       <link rel="stylesheet" href="style.css" />
     </head>
     <body>
       <p>Hello World!</p>
       <div>
         <p>Paragraf ini tidak terpengaruh dengan styling yang ada.</p>
       </div>
       <p>Aku baru terdampak!</p>
       <p>Aku juga!</p>
     </body>
   </html>
   ```

Ilustrasi:

![image13](https://user-images.githubusercontent.com/33245436/191109113-f51d51a5-e684-4c89-98f8-0725a3232b2c.png)

### Pseudo-class Selector (:)

Pseudo-class dimanfaatkan untuk memilih suatu state / keadaan dari suatu elemen. Contohnya, saat elemen di-hover (ketika mouse berada di atas elemen) dan di-klik.

Contoh pseudo-class dapat dilihat pada pengaplikasiannya di elemen `a` berikut.

```css
/* link yang belum dibuka */
a:link {
  color: #ff0000;
}

/* link yang pernah dibuka */
a:visited {
  color: #00ff00;
}

/* mouse di atas link */
a:hover {
  color: #ff00ff;
}

/* link yang dipilih */
a:active {
  color: #0000ff;
}
```

Ilustrasi:

![image14](https://user-images.githubusercontent.com/33245436/191110093-a9700e60-ed18-43e6-9b59-f4f4150ef999.png)

![image15](https://user-images.githubusercontent.com/33245436/191110598-fbcff210-3e0d-4820-a6a2-b9afedf2d82f.png)

Pada contoh di bawah, kita akan memilih semua `p` yang merupakan anak pertama dari suatu elemen.

```css
p:first-child {
  color: blue;
}
```

```html
<!DOCTYPE html>
<html>
 <head>
   <link rel="stylesheet" href="style.css" />
 </head>
 <body>
   <div>
    <p>Hello World!</p>
    <p>Paragraf ini tidak terdampak.</p>
    <section>
      <p>Namun paragraf ini terdampak.</p>
    </section>
  </div>
  <p>Ini juga tidak terdampak.</p>
 </body>
</html>
```

Ilustrasi:

![image16](https://user-images.githubusercontent.com/33245436/191110843-c46e71d2-07cf-4e23-946c-51ea5c36641b.png)

### Pseudo-element Selector (::)

Pseudo-element digunakan untuk styling bagian tertentu dari sebuah elemen. Contohnya: styling huruf pertama, baris pertama dari suatu elemen, dan memasukkan sebuah konten sebelum atau sesudah suatu elemen.

1. ::first-line <br/>
   Untuk menambahkan style ke baris pertama sebuah elemen.

   ```css
   p::first-line {
     color: #ff0000;
     font-variant: small-caps;
   }
   ```

2. ::first-letter <br/>
   Untuk menambahkan style ke huruf pertama sebuah elemen

   ```css
   p::first-letter {
     color: #ff0000;
     font-size: xx-large;
   }
   ```

3. ::before <br/>
   Untuk insert sebuah content sebelum content di dalam sebuah elemen

   ```css
   h1::before {
     content: url(https://upload.wikimedia.org/wikipedia/commons/0/03/Smiley.jpg?20070707194955);
   }
   ```

Ilustrasi:

![image17](https://user-images.githubusercontent.com/33245436/191111658-f7aef3f9-8022-4c6f-9ddb-84aaa7a57e71.png)

### Attribute Selector

Untuk memilih elemen HTML yang mempunyai atribut tertentu. Berikut beberapa jenis attribute selector.

1. CSS \[attribute] Selector <br/>
   Pada contoh di bawah, akan memilih elemen `a` yang mempunyai atribut `target`. Atribut ini dipakai untuk menspesifikan apa yang akan terjadi jika elemen `a` di-klik.

   ```css
   a[target] {
     background-color: red;
   }
   ```

2. CSS \[attribute="value"] Selector <br/>
   Pada contoh di bawah, akan memilih elemen `a` yang mempunyai atribut `target` dan nilai “\_blank”

   ```css
   a[target="_blank"] {
     background-color: yellow;
   }
   ```

3. CSS \[attribute~="value"] Selector <br/>
   [attribute~="value"] selector digunakan untuk memilih elemen dengan nilai atribut mengandung suatu kata. Pada contoh di bawah, akan memilih elemen dengan atribut `title` dan nilai yang mengandung “flower”

   ```css
   [title~="flower"] {
     border: 5px solid blue;
   }
   ```

Ilustrasi:

![image18](https://user-images.githubusercontent.com/33245436/191112241-d8f5b893-eeec-47d5-9f3f-2206de17772c.png)

## Property dan Value

Ingat, apa itu property / properti dan value / nilai dengan melihat sintaks CSS di bawah ini.

![image19](https://user-images.githubusercontent.com/68275535/130475766-8e0e2807-ab77-4b15-adc2-74fd92719117.png)

CSS mempunyai beragam properti, di sini akan dijelaskan beberapa contoh untuk memahami dasarnya. Contoh properti di CSS, yaitu: Colors, Backgrounds, Borders, Margins, Padding, Height, Width, Outline, dan masih banyak lainnya.

### Colors

Nilai dari properti colors bisa berupa:

- nama warna (`red`, `green`, `black`, `violet`, dll)
- hex (`#ff0000` atau `#f00`)
- `rgb(255,0,0)`
- `rgb(100%,0%,0%)`

**Background Color**

```html
<h1 style="background-color:DodgerBlue;">Hello World</h1>
<p style="background-color:Tomato;">Lorem ipsum...</p>
```

Ilustrasi:

![image20](https://user-images.githubusercontent.com/68275535/130476063-e2c6effd-370c-440b-9e80-2906b48f5502.png)

**Text Color**

```html
<h1 style="color:Tomato;">Hello World</h1>
<p style="color:DodgerBlue;">Lorem ipsum...</p>
<p style="color:MediumSeaGreen;">Ut wisi enim...</p>
```

Ilustrasi:

![image21](https://user-images.githubusercontent.com/68275535/130476132-54e0010f-853f-4a84-a368-93caff0815f7.png)

### Box Model

Setiap elemen HTML dapat mempunyai properti Margin, Border, dan Padding. Gabungan dari margin, border, padding, dan content dinamakan Box Model. **Margin** adalah properti yang digunakan untuk mendefinisikan ruangan di sekeliling elemen, yang berada diluar border. Sedangkan **Padding** adalah properti yang digunakan untuk mendefinisikan ruangan di sekeliling elemen, yang berada di dalam border.

![image22](https://user-images.githubusercontent.com/68275535/130476218-d8c1b98d-1af8-4e64-ac0c-8a8186c9143a.png)

Contoh:

```css
p {
  margin: 25px 50px 75px 100px; /* top right bottom left */
  padding: 20px; /* Nilai dari semua sisi sama besar */
}
```

Selain dua properti diatas, CSS memiliki banyak properti dan cara menulis nilai yang beragam. Kalian dapat mempelajarinya lebih lanjut di https://www.w3schools.com/css/default.asp

## Specificity

CSS Specificity menentukan seberapa spesifik sebuah aturan pada CSS. Jika ada 2 atau lebih aturan pada sebuah elemen yang sama, maka aturan paling spesifik lah yang akan dipakai oleh browser.

Berikut hierarki atau urutan Specificity dari yang paling utama:

1. Inline styles
2. ID
3. Classes, attributes, dan pseudo-classes
4. Elements dan pseudo-elements

Jadi jika ada 2 style yang dituju pada elemen `a` seperti contoh di bawah, maka hierarki yang lebih tinggi yang akan menang (elemen `a` akan berwarna hijau)

```html
<div class="container">
  <div id="main">
    <p>
      <a href="#" id="id1" class="class1">Link</a>
    </p>
  </div>
</div>
```

```css
#id1 {
  color: green;
}

.class1 {
  color: yellow;
}
```

**Menghitung Specificity**

Specificity bisa dihitung skornya, dan yang lebih tinggi skornya maka dialah yang lebih kuat aturan CSS-nya. Cara menghitungnya: mulai dari 0; tambahkan 1000 untuk atribut `style`; tambahkan 100 untuk setiap `ID`; tambahkan 10 untuk setiap atribut, kelas, atau pseudo-class; tambahkan 1 untuk setiap nama elemen atau pseudo-element.

Contoh:

```
A: h1 { … }
B: #content h1 { … }
C: <div id="content"><h1 style="color: #ffffff">Heading</h1></div>
```

Specificity A adalah 1 (1 elemen)
Specificity B adalah 101 (1 ID, 1 elemen)
Specificity C adalah 1000 (inline styling)

Karena 1 < 101 < 1000, maka C mempunyai specificity yang paling besar, sehingga style itulah yang akan dipakai.

## Referensi

- https://www.w3schools.com/
- https://github.com/minons1/PelatihanSoftwareHouseHMTCITS/wiki/CSS
- http://dev.bertzzie.com/knowledge/desain-web-dasar/HTMLdanCSSDasar.html
- https://gawibowo.com/css-specificity.htm
