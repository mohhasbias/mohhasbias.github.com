---
layout: post
title: "Membuat kapitalisasi otomatis menggunakan CSS"
date: 2013-05-18 21:33
comments: true
categories: CSS
---

pada CSS terdapat properti untuk membuat text otomatis menjadi Title Case, yaitu membuat awal huruf pada setiap kata menjadi huruf besar.
akan tetapi, properti tersebut tidak mengubah huruf lain menjadi kecil. Karenanya, perlu dikombinasi dengan perintah lain.

Sebagai contoh, jika menggunakan PHP, maka sebelum sebuah string ditampilkan, harus dikecilkan dulu menggunakan ```strtolower```. kemudian pada CSS-nya, kita aktifkan properti ```text-transform```, seperti berikut ini

{% codeblock lang:css %}
p {
	text-transform: capitalize;
}
{% endcodeblock %}
