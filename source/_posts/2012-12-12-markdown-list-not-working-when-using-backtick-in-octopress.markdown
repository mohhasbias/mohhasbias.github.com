---
layout: post
title: "Markdown list not working when using Backtick in Octopress"
date: 2012-12-12 05:32
comments: true
categories: [Misc]
---

Beberapa hari ini, mulai migrasi dari wordpress ke octopress.  
First impressionnya mantab.

Hanya saja, seperti biasa, selalu ada masalah

Yang menarik, pembuatannya postnya tidak menggunakan HTML melainkan Markdown
konsepnya, sebuah tool yang mengubah plain text menjadi HTML.

Salah satu yang saya pakai adalah ordered list.  
Caranya [seperti berikut](http://daringfireball.net/projects/markdown/syntax#list).  
Pada file markdown, cukup ditulis sebagai berikut
{% codeblock %}
1. Bird
2. McHale
3. Parish
{% endcodeblock %}
Maka oleh Markdown akan di convert menjadi
{% codeblock lang:html %}
<ol>
<li>Bird</li>
<li>McHale</li>
<li>Parish</li>
</ol>
{% endcodeblock %}

Sederhana.

Disisi lain, octopress menyediakan tool untuk highlight code.
Toolnya ada dua, yaitu [backtick](http://octopress.org/docs/plugins/backtick-codeblock/) dan [codeblock](http://octopress.org/docs/plugins/codeblock/).  
Yang menjadi masalah, saat markdown list digunakan bersamaan dengan backtick. Efeknya, markdown list-nya ga jalan.  
Solusinya, penggunaan backtick diganti dengan codeblock.
