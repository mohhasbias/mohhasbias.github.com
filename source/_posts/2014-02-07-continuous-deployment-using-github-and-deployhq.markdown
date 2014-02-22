---
layout: post
title: "Continuous Deployment using Github and DeployHQ"
date: 2014-02-07 09:07
comments: true
categories: 
---

Berikut adalah langkah-langkah untuk menerapkan continuous deployment (automatic deployment) menggunakan Github dan DeployHQ

1. Siapkan repo yang ingin dideploy pada Github
2. Tambahkan project baru pada deployHQ dengan memilih repo bertipe github
3. Setelah login berhasil, pilih repo yang diinginkan dari daftar repo yang ada
4. Gunakan menu deploy now untuk menguji kerja deployHQ
5. Jika berhasil, aktifkan auto deploy dengan meng-copy github hook dari server setting
6. Pada repo di Github, aktifkan service hooks untuk deployHQ dengan meng-paste github hook sebelumnya
7. Enjoy
