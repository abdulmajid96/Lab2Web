# Praktikum 2: CSS Dasar
# Mata Kuliah Pemrograman WEB
```
Nama  : Abdul Majid
NIM   : 311810693
Kelas : TI.19.C.1
Universitas Pelita Bangsa
```
## Persiapan
Buka VSCode dan Browser lalu buat file HTML baru dengan nama lab2_css_dasar.html

## 1. Membuat Dokumen HTML
Buatlah dokumen HTML seperti berikut.
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Dasar</title>
</head>
<body>
    <header>
        <h1>CSS Internal dan <i>Inline CSS</i></h1>
    </header>
    <nav>
        <a href="lab2_css_dasar.html">CSS Dasar</a>
        <a href="lab2_css_eksternal.html">CSS Eksternal</a>
        <a href="lab1_tag_dasar.html">HTML Dasar</a>
    </nav>
    <!-- CSS ID Selector -->
    <div id="intro">
        <h1>Hello World</h1>
        <p>Kami sedang belajar HTML dan CSS dasar, pada mata kuliah <b>Pemrograman Web</b> di <i>Universitas Pelita Bangsa</i>. Pelajaran pertama yang kami dapat adalah membuat tampilan web sederhana dalam rangka mengenal tag-tag dasar HTML dan CSS.</p>
        <!-- CSS Class Selector -->
        <a class="button btn-primary" href="#intro">Informasi selengkapnya.</a>
    </div>
</body>
</html>
```
![01-dokumen-html](https://user-images.githubusercontent.com/81838946/114211745-37c39300-998b-11eb-8a7b-0ffee17e35b7.PNG)

## 2. Mendeklarasikan CSS Internal
Kemudian tambahkan deklarasi CSS internal seperti berikut pada bagian head dokumen.
```html
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Dasar</title>
    <style>
        body {
        font-family:'Open Sans', sans-serif;
        }
        header {
        min-height: 80px;
        border-bottom:1px solid #77CCEF;
        }
        h1 {
        font-size: 24px;
        color: #0F189F;
        text-align: center;
        padding: 20px 10px;
        }
        h1 i {
        color:#6d6a6b;
        }
        </style>
</head>
```
![02-CSS-Internal](https://user-images.githubusercontent.com/81838946/114212169-b7e9f880-998b-11eb-8552-24a83fd581a8.PNG)

## 3. Menambahkan Inline CSS
Kemudian tambahkan deklarasi inline CSS pada tag < p> seperti berikut.
```html
<p style="text-align: center; color: #ccd8e4;">
 ```
![03](https://user-images.githubusercontent.com/81838946/114213139-d69cbf00-998c-11eb-9a09-6c7fd806c87c.PNG)

 ## 4. Membuat CSS Eksternal
 Buatlah file baru dengan nama style_eksternal.css kemudian buatlah deklarasi CSS seperti berikut.
 ```css
 nav {
    background: #20A759;
    color:#fff;
    padding: 10px;
    }
nav a {
    color: #fff;
    text-decoration: none;
    padding:10px 20px;
    }
nav .active,
nav a:hover {
    background: #0B6B3A;
    }
 ```
![04-1](https://user-images.githubusercontent.com/81838946/114213591-5d519c00-998d-11eb-9dc3-2bab45a29036.PNG)

Kemudian tambahkan tag < link> untuk merujuk file css yang sudah dibuat pada bagian < head>
```html
<head>
  <!-- menyisipkan css eksternal -->
  <link rel="stylesheet" href="style_eksternal.css" type="text/css">
</head>
```
![04-2](https://user-images.githubusercontent.com/81838946/114213918-d94be400-998d-11eb-8620-d9f5969df5a4.PNG)

## 5. Menambahkan CSS Selector
Selanjutnya menambahkan CSS Selector menggunakan ID dan Class Selector. Pada file style_eksternal.css, tambahkan kode berikut.
```css
/* ID Selector */
#intro {
    background: #418fb1;
    border: 1px solid #099249;
    min-height: 100px;
    padding: 10px;
    }

#intro h1 {
    text-align: left;
    border: 0;
    color: #fff;
    }

/* Class Selector */
.button {
    padding: 15px 20px;
    background: #bebcbd;
    color: #fff;
    display: inline-block;
    margin: 10px;
    text-decoration: none;
    }

.btn-primary {
    background: #E42A42;
    }
```
![05](https://user-images.githubusercontent.com/81838946/114214498-8e7e9c00-998e-11eb-8ea0-2cdd14948784.PNG)

## JAWAB PERTANYAAN
1. Lakukan eksperimen dengan mengubah dan menambah properti dan nilai pada kode CSS dengan mengacu pada CSS Cheat Sheet yang diberikan pada file terpisah dari modul ini.

2. Apa perbedaan pendeklarasian CSS elemen h1 {...} dengan #intro h1 {...}? berikan penjelasannya!
```
Perbedaannya adalah pendeklarasian CSS emelen h1 {...} menggunakan selector tag HTML h1 dan dideklarasikan di CSS Internal. Sedangkan #intro h1 {...} dilakukan pengaturan menggunakan selector ID intro untuk tag h1 nya, sehingga untuk tag HTML h1 dapat dilakukan pengaturan yang berbeda.
```
3. Apabila ada deklarasi CSS secara internal, lalu ditambahkan CSS eksternal dan inline CSS pada elemen yang sama. Deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya!
```
Deklarasi yang akan ditampilkan pada browser adalah deklarasi secara inline CSS, karena deklarasinya digunakan untuk tag HTML tertentu atau secara langsung (khusus). 
Sebagai contoh saya melakukan percobaan deklarasi untuk tag HTML <p> dengan pengaturan style yang berbeda untuk mengetahui deklarasi mana yang akan terbaca.
```
```html
<!-- Internal CSS pada file lab2_css_dasar.html -->
        <style>
              p{
                text-align: left;
                color: #fff;
              }
        <style>
        
<!-- Eksternal CSS pada file style_eksternal.css -->
        /* Tag Selector */
        p{
          text-align: right;
          color: #E42A42;
        }
          
<!-- Inline CSS pada file lab2_css_dasar.html -->
        <p style="text-align: center; color: #ccd8e4;">
```
```
Hasilnya adalah deklarasi secara inline yang ditampilkan pada browser.
```          
![pertanyaan_no-3](https://user-images.githubusercontent.com/81838946/114219127-77db4380-9994-11eb-8d9e-721f53c1716c.PNG)

4. Pada sebuah elemen HTML terdapat ID dan Class, apabila masing-masing selector tersebut terdapat deklarasi CSS, maka deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya! ( < p id="paragraf-1" class="text-paragraf"> )
```
Deklarasi yang akan ditampilkan pada browser adalah deklarasi secara ID, karena deklarasi ID hanya akan bekerja pada satu elemen HTML saja. Sedangkan CLASS digunakan untuk penandaan pada banyak elemen HTML sekaligus.
Sebagai contoh saya melakukan percobaan deklarasi untuk tag HTML <p> dengan pengaturan style yang berbeda untuk mengetahui deklarasi mana yang akan terbaca.
```
```css
/* ID Selector */
#paragraf-1 {
    text-align: left;
    color: #fff;
}

/* Class Selector */
.text-paragraf {
    text-align: center;
    color: #E42A42;
}
```
```
Hasilnya adalah deklarasi menggunakan selector ID yang ditampilkan pada browser.
```
![pertanyaan_no-4](https://user-images.githubusercontent.com/81838946/114221282-50d24100-9997-11eb-94d6-470a5c45fbab.PNG)

