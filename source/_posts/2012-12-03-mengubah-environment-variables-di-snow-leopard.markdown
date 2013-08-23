---
layout: post
title: "Mengubah environment variables di snow leopard"
date: 2012-12-03 10:58
comments: true
categories: ["OS X Administration"]
---

untuk mengubah environment variable yang berlaku untuk semua aplikasi osx:

1. buat/edit file "~/.MacOSX/environment.plist"
2. tambahkan environment variable yang diinginkan


applynya? belum tahu. mungkin bisa pakai logout trus login. bisa juga reboot.

untuk mengubah environment variable yang berlaku untuk semua aplikasi under bash
 
1. buat/edit file "~/.bash_profile"
2. tambahkan environment variable yang diinginkan menggunakan perintah export
3. apply perubahannya dengan menggunakan perintah
{% codeblock lang:bash %}
source ~/.bash_profile
{% endcodeblock %}
dengan perintah ini, tidak diperlukan reopening shell.
