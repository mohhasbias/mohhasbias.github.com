---
layout: post
title: "update grub menggunakan liveCD"
date: 2013-05-18 05:05
comments: true
categories: Linux
---

Baru saja kembali nguprek ubuntu setelah sekian lama ditinggal. Dan seperti biasa, saat main-main dual boot, bootloader-nya bermasalah.

Iseng-iseng ganti konfigurasi grub jadinya malah ilang grub-nya. Setiap kali booting, langsung masuk ke windows.

Alhamdulillah tidak terlalu panik, masih bisa tenang. Langsung kepikiran untuk pakai Live-CD

Berikut adalah langkah-langkah menggunakan Live CD untuk meng-update grub

1. Booting menggunakan Live CD, bisa pakai yang berbasis CD/DVD, bisa juga pakai USB. Saya pakai USB karena lappie-nya ga ada DVD drive-nya.
2. Setelah masuk Live CD, buka terminal. Saya pakai Ubuntu Live CD, sehingga bisa pakai perintah ```Ctrl + Alt + T``` untuk membuka terminal.
3. Mount partisi yang ingin di-update, contoh  
	```mount /dev/sda1 /mnt```
4. Mount file-file yang berhubungan dengan system/hardware menggunakan perintah berikut (sumber:[ubuntuforum/update-grub](http://ubuntuforums.org/showthread.php?t=2036730))   
	```for i in /dev /dev/pts /proc /sys /run; do sudo mount -B $i /mnt$i; done```
5. Aktifkan partisinya menggunakan chroot    
	```sudo chroot /mnt```
6. Edit konfigurasi grub kemudian jalankan perintah update-grub  
	```update-grub```
