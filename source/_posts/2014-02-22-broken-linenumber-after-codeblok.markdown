---
layout: post
title: "Broken linenumber after codeblok in Octopress"
date: 2014-02-22 06:17
comments: true
categories: 
---

beberapa hari nyoba pakai linenumber dan codeblock di octopress selalu tidak berhasil.
browsing-browsing sampai nyasar ke repo-nya [octopress][].
kesimpulannya, memang octopress belum support. masih mencari solusi yang clean (katanya [brandon imathis][codeblock_issue]).

Solusinya:
back to old working HTML

contoh:
jika menggunakan codeblock biasa:
{% codeblock %}
{% raw %}
1. bla bla bla
	{% codeblock %}
	...
	some code
	...
	{% endcodeblock %}

2. bla bla bla lagi
	{% codeblock %}
	...
	programming is fun
	...
	{% endcodeblock %}
{% endraw %}
{% endcodeblock %}

akan menghasilkan:  


1. bla bla bla
	{% codeblock %}
	...
	some code
	...
	{% endcodeblock %}

2. bla bla bla lagi
	{% codeblock %}
	...
	programming is fun
	...
	{% endcodeblock %}


maka numberingnya akan rusak.
untuk membetulkannya, back to html
{% codeblock %}
{% raw %}
<ol>
<li> bla bla bla
	{% codeblock %}
	...
	some code
	...
	{% endcodeblock %}
</li>
<li> bla bla bla lagi
	{% codeblock %}
	...
	programming is fun
	...
	{% endcodeblock %}
</li>
</ol>
{% endraw %}
{% endcodeblock %}

sehingga menghasilkan:  


<ol>
<li> bla bla bla
	{% codeblock %}
	...
	some code
	...
	{% endcodeblock %}
</li>
<li> bla bla bla lagi
	{% codeblock %}
	...
	programming is fun
	...
	{% endcodeblock %}
</li>
</ol>


[octopress]: https://github.com/imathis/octopress
[codeblock_issue]: https://github.com/imathis/octopress/pull/814
