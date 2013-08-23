---
layout: post
title: "cara memperbaiki windows 7 (BOOTMGR is MISSING)"
date: 2013-05-17 20:45
comments: true
categories: ["Windows 7"]
---

Jika anda mencoba linux semisal ubuntu, seringkali anda menginstall-nya di partisi lain yang biasa disebut dengan [dual boot](http://en.wikipedia.org/wiki/Multi_boot). Dalam dunia dual boot, kemungkinan besar anda akan tersandung ke masalah boot manager.

salah satu contoh masalahnya seperti ini, ketika komputer dihidupkan dan hendak booting ke windows 7, muncul tampilan berikut

{% img /images/bootmgr_error.png %}

cara membetulkannya sebagai berikut:

1. booting menggunakan installer windows
2. kemudian pilih menu "Repair your computer"
3. kemudian pilih menu "Use recovery tools that ... (bla bla bla)". klik Next
4. Pada tampilan ini, pilih menu "Startup Repair"

	{% img /images/system_recovery_tools.png %}

5. Tunggu prosesnya berjalan

	{% img /images/startup_repair.png %}

6. Jika proses berhasil, tekan Finish untuk merestart komputer.
7. Jika berhasil maka setelah restart anda akan mendapatkan kembali windows anda. Tanpa harus install ulang.

sumber: [How to fix the "Bootmgr is missing"](http://www.sevenforums.com/tutorials/104341-bootmgr-missing-fix.html)
