---
layout: post
title: "Deploy to heroku"
date: 2012-12-04 01:38
comments: true
categories: ["heroku", "Rails"]
---

setelah berhasil migrasi dari [sqlite3](http://www.sqlite.org) ke [postgresql](http://www.postgresql.org). selanjutnya adalah menginstall tools untuk deploy ke heroku.

ada 3 tools yang perlu diinstal. ke 3 tools ini biasa disebut dengan [heroku toolbelt](https://toolbelt.heroku.com). heroku sudah menyediakan packages untuk menginstall tools tersebut. tools tersebut terdiri dari [heroku cli](https://github.com/heroku/heroku), [foreman](https://github.com/ddollar/foreman), dan [git](http://git-scm.com).

sayangnya, git sudah terinstall sebelumnya. karena saya paranoid, saya menghindari menginstall toolbelt takut meng-overwrite git yang sudah terinstall. alhasil, saya pakai jalur lain. kebetulan, heroku dan foreman didistribusikan dalam bentuk gem. jadi untuk menginstall keduanya, cukup menggunakan perintah
``` bash 
gem install heroku
gem install foreman
```

stelah toolbelt terinstall, step umum untuk mendeploy adalah sebagai berikut.

langkah awal, membuat aplikasi pada heroku. aplikasi ini berfungsi sebagai tempat untuk deploy. perintahnya sebagai berikut
``` bash
heroku create
```
perintah ini akan menambahkan remote pada git dengan nama heroku. sehingga kode yang sudah di-commit di git, bisa di deploy dengan perintah
``` bash
git push heroku master
```
setelah di-deploy, hasilnya dapat dilihat di browser dengan menggunakan perintah
``` bash
heroku open
```
untuk keperluan debugging, beberapa perintah ini dapat digunakan
``` bash
heroku ps
```
perintah ini untuk melihat status aplikasi
``` bash
heroku logs
```
perintah in untuk melihat log

alhamdulillah sampai tahap ini lancar.
but, new challenge comes.
tantangan selanjutnya: rails asset pipelines
