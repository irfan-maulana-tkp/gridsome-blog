---
title: Membuat blog keren dengan Gridsome
slug: membuat-blog-keren-dengan-gridsome
date: 2019-03-14
tags: ['Gridsome','JavaScript']
cover_image: ./images/logo-poster.png
canonical_url: false
published: true
description: Bagaimana memulai membuat Blog statis keren menggunakan Vue.js static site generator Gridsome dalam waktu yang singkat
---

## Mengenal Blog Statis

"Blog statis" merupakan blog yang kita buat tanpa menggunakan *backend*, sehingga bisa kita deploy dengan mudah pada berbagai static host seperti Github Pages, Netlify, Firebase dan lainnya. Blog statis ini biasanya menggunakan templat seperti *Markdown* yang akan *build* sesaat sebelum *deploy* untuk menghasilkan file statis HTML, CSS dan JavaScript.

## Apa itu Gridsome

![Gridsome Logo](./images/logo-poster.png)

[Gridsome ↗️](https://gridsome.org/) merupakan anak baru di ekosistem Vue.js yang mengkhususkan dirinya sebagai pembuat halaman statis (*static site generator*). Bila kalian pengguna React.js, tentu sudah tidak asing dengan yang namanya [Gatsby ↗️](https://www.gatsbyjs.org/) sebagai salah satu pembuat halaman statis terbaik saat ini. Nah, Gridsome sangat terinspirasi dari apa yang dikerjakan oleh Gatsby di ekosistem React.js.

Sudah bukan hal baru bahwa ekosistem di Vue belum sekuat dan sekomplit di React, namun saya pribadi selalu terkagum-kagum dengan mereka yang bersusah payah membuatkan alternatif bagi banyak hal hebat di React untuk Vue. Gridsome, seperti ingin mengekor pada kesuksesan Nuxt yang mencoba mengadopsi Next.js di React. Nuxt yang beberapa tahun lalu belum terdengar suaranya hari ini bahkan telah menjadi pilihan terbaik ketika akan membuat sebuah aplikasi diatas Vue.

**Mengapa Gridsome lebih baik dibandingkan Nuxt?**

Nuxt pada dasarnya diperuntukkan untuk membuat aplikasi web di Vue yang membutuhkan rendering di server, Nuxt lebih khusus sangat disiapkan untuk menangani berbagai kebutuhan kompleks yang biasanya muncul ketika membuat sebuah aplikasi web. Meskipun Nuxt mempunyai kemampuan untuk men-*generate* file statis yang bisa kita gunakan juga untuk membuat blog statis, namun sebenarnya ini merupakan fungsi yang *nice-to-have* bagi Nuxt.

Sementara Gridsome merupakan pemain yang punya spesialis di bagian ini. Gridsome sudah secara *default* memiliki fitur *generate* yang dipersenjatai dengan berbagai *built-in* fitur lain yang dibutuhkan ketika membuat blog statis seperti otomatis melakukan *code-splitting*, melakukan kompresi gambar, mendukung PWA secara penuh, dan tentunya sangat bersahabat dengan SEO. Kita juga bisa dengan mudah mengorganisasikan berkas konten kita dengan **Markdown** tanpa perlu tambahan konfigurasi apapun lagi. Bila kalian lihat di repository [Blog 2.0 ↗️](/blog-2-0-in-nuxtjs) yang saya buat dengan Nuxt tentu tau bahwa saya harus melakukan berbagai "kecurangan" untuk mengerjakan hal yang sama.

![How Gridsome Works](./images/how-it-works.gif)

## Membuat Blog dengan Gridsome

Membuat blog dengan Gridsome sekarang sangat dipermudah dengan adanya *starter template* yang menurut saya sudah cukup komplit untuk kebutuhan umum sebuah blog.

Gridsome membuat starter yakni [gridsome-starter-blog ↗️](https://github.com/gridsome/gridsome-starter-blog) yang bisa kalian gunakan dengan cepat dan mudah untuk pertama kali. Dengan menggunakan starter seperti ini akan mengurangi banyak beban di depan untuk melakukan banyak konfigurasi yang tentunya akan membingungkan bagi pemula seperti saya ini.

Berikut kurang lebih langkah-langkah untuk membuat blog dengan menggunakan starter template dari Gridsome ini:

**1. Install Gridsome CLI**

```bash
$ npm install --global @gridsome/cli
```

**2. Install `gridsome-starter-blog`**

```bash
$ gridsome create gridsome-blog https://github.com/gridsome/gridsome-starter-blog.git
```

**3. Menjalankan untuk development**

```bash
$ gridsome develop
```

**4. Men-*generate* berkas static**

```bash
$ gridsome build
```

> Kalian bisa lihat hasil membuat Blog dengan gridsome starter di repository https://github.com/mazipan/gridsome-blog ↗️](https://github.com/mazipan/gridsome-blog)

## Deploy ke Netlify

Untuk deploy Gridsome ke Netlify juga sangat mudah, bahkan Gridsome juga menyediakan dokumentasi resmi mengenai langkah-langkahnya di halaman [deploy-to-netlify ↗️](https://gridsome.org/docs/deploy-to-netlify), yang kurang lebih seperti berikut:

1. Buat halaman projek baru di Netlify
2. Tambahkan perintah `gridsome build` pada kolom *build command*
3. Dan tambahkan direktori `dist` pada kolom *publish directory*
4. Kalian bisa lihat hasilnya di [https://gridsome-blog.netlify.com/ ↗️](https://gridsome-blog.netlify.com/)

### Demikian artikel kali ini, semoga bermanfaat...
