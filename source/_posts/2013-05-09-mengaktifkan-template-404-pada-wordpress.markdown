---
layout: post
title: "mengaktifkan template 404 pada wordpress"
date: 2013-05-09 11:37
comments: true
categories: wordpress
---

beberapa hari ini berkutat dengan pembuatan website berbasis wordpress.
sangat menyenangkan karena wordpress merupakan framework berbasis template.
yang artinya, kalau ingin membuat website, ganti saja template default dengan template yang diinginkan.

salah satu contohnya adalah template untuk error 404. sebuah error yang salah satu kemunculannya karena user salah ketik URL.

secara teori, 404 merupakan jalan buntu pada sebuah website. di halaman ini perlu diberikan saran untuk user tentang apa yang perlu dilakukan. ada banyak contoh kreatif yang bisa jadi [sumber inspirasi](http://www.smashingmagazine.com/2009/01/29/404-error-pages-one-more-time/).

di wordpress, template yang bertanggung jawab untuk 404 adalah file ```404.php```.

secara default, template ini tidak akan aktif kalau kita tidak membuat file htaccess untuk mengaktifkannya. apapun perubahan yang kita lakukan pada file ```404.php``` tidak akan ngefek. yang muncul hanyalah 404 default bawaan web server. misalnya seperti ini kalau kita pakai apache.
{% img images/apache_404_default.gif %}

untuk bisa mengaktifkan tanpa harus membuat file htaccess, cukup ganti menu permalinks pada wordpress. ganti dengan opsi manapun selain default. sebagai contoh
{% img images/permalink_options.png %}


