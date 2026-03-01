# MINI PROJECT PEMOGRAMAN BERBASIS WEB (1) "PORTOFOLIO"

<img width="1897" height="862" alt="Screenshot 2026-02-28 211144" src="https://github.com/user-attachments/assets/20ea2249-5e3d-4d6a-8b5e-4770deec39d5" />

## Dibuat Oleh

Nama   : Aliyah Azzah Sekedang

NIM    : 2409116021

## 📌 Deskripsi Program
Website portfolio pribadi ini adalah website yang dirancang sebagai personal branding platform. Website ini menampilkan informasi mengenai profil, professional skills, pengalaman, project, dan sertifikat yang pernah diperoleh dalam satu halaman yang modern dan responsif. 

## 📌 Teknologi yang Digunakan
Website ini dibuat menggunakan beberapa teknologi berikut:
- HTML : untuk membuat struktur halaman website
- CSS : untuk mengatur tampilan dan desain
- Bootstrap : untuk membantu layout responsif dan komponen UI
- Vue.js (CDN) : untuk mengelola data dan membuat tampilan dinamis
- JavaScript : untuk logika program dan pengolahan data
- Google Fonts: untuk typography custom (Poppins, Pinyon Script, dll)

## 📂 Struktur Folder

<p align="center">
   <img src="https://github.com/user-attachments/assets/404f6c4e-254b-4de6-a808-268710100f98" width="200" style="border:2px solid #ddd; border-radius:10px;">
</p>

Penjelasan:
- index.html : file utama yang berisi struktur HTML dan script Vue
- style.css : file untuk custom styling
- assets/ : folder untuk menyimpan gambar seperti foto profil, project, dan sertifikat

## 📌 Tampilan Setiap Section Website

Website ini terdiri dari beberapa section utama:

### 1️⃣ Navbar
Navbar berada di bagian paling atas dan bersifat fixed sehingga letaknya akan tetap di atas saat halaman di-scroll.

<img width="1899" height="67" alt="Screenshot 2026-02-28 213912" src="https://github.com/user-attachments/assets/efa228e0-6455-4555-a635-b271620d780b" /><br>

Berisi:
- Nama pemilik portfolio
- Menu navigasi:
  - Home
  - About Me
  - Certificates
- Icon dari Bootstrap Icons
Navbar akan menjadi hamburger menu (3 garis) pada saat dibuka dengan tampilan layar kecil.

### 2️⃣ Hero Section
Menampilkan section pertama kali muncul saat website dibuka.

<img width="1919" height="1018" alt="Screenshot 2026-02-28 212149" src="https://github.com/user-attachments/assets/963c80ed-a9a2-4579-b0f7-1143212f72df" /><br>

Berisi:
- Judul “Welcome To My Portfolio”
- Role / Jabatan (diambil dari Vue.js)
- Background image full screen
- Card dengan efek shadow dan rounded corner
  
### 3️⃣ About Us Section
Menampilkan data diri saya dalam bentuk beberapa kolom.

<img width="1919" height="1018" alt="Screenshot 2026-02-28 212117" src="https://github.com/user-attachments/assets/09a155e6-c9f1-4447-af94-eb56da14593c" /><br>

Berisi:
- Sisi Kiri:
  - Foto identity card
  - Deskripsi diri
  - Informasi kontak

- Sisi Kanan:
  - Professional Skills (progress bar)
  - Experience (daftar pengalaman)
  Layout menggunakan Bootstrap Grid System.
    
### 4️⃣ Certificates Section
Section ini terdiri dari dua bagian:

***Recent Projects***

<img width="1915" height="1019" alt="Screenshot 2026-02-28 212726" src="https://github.com/user-attachments/assets/32018a9b-4224-4b7d-b384-c11d8a2b0624" />
<br>
  
***Certificates***

<img width="1917" height="1023" alt="Screenshot 2026-02-28 212657" src="https://github.com/user-attachments/assets/2416404e-ac25-487b-a05b-8316298b097a" />
<br>

Ditampilkan dalam bentuk card grid (3 kolom pada layar besar).

Setiap card berisi:
- Gambar
- Judul
- Tombol “View Details”

### 5️⃣ Footer

Footer sederhana di bagian bawah halaman dengan warna gradient hijau dan teks copyright.

<img width="1899" height="82" alt="Screenshot 2026-02-28 221956" src="https://github.com/user-attachments/assets/3157c900-0aa4-49a8-8165-dad6bd3aa63c" />



## 📌 Penjelasan Kode Setiap Section

**🔹 1. Head**
~~~ Javascript
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Seki Portfolio</title>

<link href="https://fonts.googleapis.com/css2?family=Pinyon+Script&family=Playball&family=Londrina+Solid&family=Great+Vibes&family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.css">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
<link rel="stylesheet" href="style.css">
</head>
<body>
 ~~~

Bagian <head> berfungsi untuk mengatur identitas dan konfigurasi dasar halaman website. Di dalamnya terdapat:

- <meta charset="UTF-8"> untuk mengatur format karakter agar mendukung berbagai simbol dan huruf.
- <meta name="viewport"> untuk memastikan tampilan website responsive di berbagai ukuran layar.
- <title>Seki Portfolio</title> untuk mengatur judul halaman yang tampil di tab browser.

Selain itu, pada bagian ini juga dilakukan import beberapa library dan styling eksternal seperti:

- Google Fonts untuk mempercantik typography.
- Bootstrap 5.3.3 untuk sistem grid dan komponen siap pakai.
- Bootstrap Icons dan Font Awesome untuk ikon.
- File CSS eksternal (style.css) untuk custom styling.<br>
 
**🔹 2. Vue App Container**
~~~ Javascript
<div id="app">
~~~

Kode ini adalah wadah utama aplikasi Vue. Semua section website berada di dalam div ini karena Vue akan mengontrol elemen dengan id="app".

Di bagian bawah file terdapat:

~~~ Javascript
const { createApp } = Vue

createApp({
  data() {
    return {
      name: "Aliyah Azzah Sekedang",
      role: "Graphic Designer",
      ...
    }
  }
}).mount('#app')
~~~

Kode ini berfungsi untuk membuat aplikasi Vue dan menyimpan semua data seperti nama, role, skill, pengalaman, project, dan sertifikat. Fungsi .mount('#app') menghubungkan Vue dengan elemen #app sehingga data dapat ditampilkan di HTML menggunakan tanda {{ }} dan directive seperti v-for.<br>

**🔹 3. Navbar**

~~~ Javascript
<nav class="navbar navbar-expand-lg fixed-top">
~~~

Penjelasan:
- navbar adalah komponen navigasi dari Bootstrap
- navbar-expand-lg : navbar akan berubah menjadi hamburger menu di layar kecil
- fixed-top : navbar selalu menempel di atas saat halaman di-scroll

Menu navigasi:
~~~ Javascript
<a class="nav-link" href="#home">Home</a>
<a class="nav-link" href="#about">About Me</a>
<a class="nav-link" href="#certificates">Certificates</a>
~~~

Atribut href="#about" membuat halaman otomatis scroll ke section yang memiliki id tersebut. Nama pada navbar ditampilkan menggunakan {{ name }}, artinya teks tersebut diambil dari data Vue, bukan ditulis langsung di HTML.<br>

**🔹 4. Hero Section (Home)**
~~~ Javascript
<section id="home" class="hero-section">
~~~

Penjelasan:
- id="home" : agar bisa diakses dari menu Home
- hero-section : class untuk styling background dan layout

Role ditampilkan menggunakan:
~~~ Javascript
<p class="hero-tagline">{{ role }}</p>
~~~

Tanda {{ role }} mengambil data dari Vue. Tata letak konten dibuat berada di tengah menggunakan class Bootstrap seperti d-flex dan justify-content-center, sedangkan tampilan background dan styling diatur melalui class hero-section pada file CSS.<br>

**🔹 5. About Me Section**
~~~ Javascript
<section id="about" class="about-section">
~~~

Penjelasan:
- id="home" : agar bisa diakses dari menu Home
- hero-section : class untuk styling background dan layout

Layout dibuat menggunakan sistem grid Bootstrap:
~~~ Javascript
<div class="row g-5">
<div class="col-lg-5">
<div class="col-lg-7">
~~~

Struktur ini membagi tampilan menjadi dua kolom pada layar besar dan otomatis menjadi satu kolom pada layar kecil agar tetap responsif.

Foto profil ditampilkan menggunakan:
~~~ Javascript
<img :src="profileImage">
~~~

Tanda :src menunjukkan bahwa sumber gambar diambil dari data Vue. Deskripsi dan email juga ditampilkan menggunakan {{ description }} dan {{ email }} sehingga teks berasal dari data JavaScript.

- ***Bagian Skills***
  ~~~ Javascript
  <div v-for="skill in skills" :key="skill.name">
  ~~~

  Kode ini digunakan untuk menampilkan daftar skill secara otomatis berdasarkan data pada array skills. Setiap skill akan diulang menggunakan v-for.

  Progress bar diatur menggunakan:
  ~~~ Javascript
  <div class="progress-bar"
     :style="{ width: skill.level + '%' }">
  ~~~

  Kode :style digunakan untuk mengatur lebar progress bar sesuai dengan nilai persentase yang ada pada data, sehingga jika nilai berubah, tampilan bar juga otomatis berubah.

- ***Bagian Experience***
~~~ Javascript
<li v-for="exp in experiences" :key="exp">
  {{ exp }}
</li>
~~~

Kode ini menampilkan daftar pengalaman berdasarkan isi array experiences. Vue akan mengulang elemen list sesuai jumlah data yang ada, sehingga jika data ditambahkan, daftar akan bertambah otomatis tanpa mengubah struktur HTML.<br>

**🔹 6. Recent Projects dan Certificates**
~~~ Javascript
<div class="col-md-4" v-for="project in projects" :key="project.title">
~~~

Penjelasan:
- col-md-4 : menampilkan 3 card dalam satu baris pada layar medium ke atas
- v-for : menampilkan project berdasarkan data array

Gambar dan judul ditampilkan menggunakan kode berikut:
~~~ Javascript
<img :src="project.image">
{{ project.title }}
~~~

Tombol detail menggunakan :href agar link mengikuti data yang ada di Vue. Struktur pada bagian certificates sama seperti project, hanya sumber datanya berasal dari array certificates, sehingga semua card ditampilkan secara dinamis dari data Vue.<br>

**🔹 9. Footer**
~~~ Javascript
<footer class="text-center py-4 footer">
~~~

Footer digunakan untuk menampilkan bagian paling bawah website. Class text-center membuat teks rata tengah dan py-4 memberikan padding atas dan bawah agar tampilannya lebih rapi. Styling warna dan tampilan tambahan diatur melalui class footer pada file CSS.

