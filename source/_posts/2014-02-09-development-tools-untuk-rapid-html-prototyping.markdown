---
layout: post
title: "Development tools untuk rapid html prototyping"
date: 2014-02-09 15:49
comments: true
categories: 
---

beberapa kombinasi tools yang dapat mempercepat proses pembuatan html prototype adalah

1. [Clay](http://lucuma.github.io/Clay/)
2. [Grunt](http://gruntjs.com/)

## Clay
Clay memiliki 2 perintah utama yaitu

{% codeblock lang:bash %}
clay run
{% endcodeblock %}

dan

{% codeblock lang:bash %}
clay build
{% endcodeblock %}

perintah ```clay run``` berguna untuk mengaktifkan http server. sehingga tanpa perlu menginstall xampp dkk, sudah bisa langsung mengakses ```http://localhost:8080``` untuk mem-preview halaman web yang telah dibuat.

sedangkan perintah ```clay build``` berfungsi untuk mengubah project yang ada menjadi html static murni yang bisa diakses tanpa memerlukan [Clay](http://lucuma.github.io/Clay).

## Grunt
Grunt berfungsi untuk otomasi kegiatan yang repetitive. salah satu fungsi utamanya adalah mengeksekusi perintah tertentu pada saat ada perubahan pada file. yang artinya setiap kali tombol save ditekan pada text editor, grunt dapat diperintah untuk menjalankan perintah tertentu.

beberapa skenario yang dapat diuntungkan oleh grunt, antara lain

1. reload browser ( [grunt-contrib-watch](https://github.com/gruntjs/grunt-contrib-watch) )
2. compile sass ([grunt-sass](https://github.com/sindresorhus/grunt-sass))
3. sinkronisasi browser ([grunt-browser-sync](https://github.com/shakyShane/grunt-browser-sync))

dan sepertinya banyak skenario yang lainnya. pada dasarnya, keberadaan grunt berfungsi sebagai otomasi proses software development dengan harapan meningkatnya produktifitas. jika penggunaan grunt membuat pekerjaan jadi lambat, berarti grunt termasuk overkill alias tidak diperlukan :D
