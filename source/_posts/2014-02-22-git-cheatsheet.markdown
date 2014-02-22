---
layout: post
title: "Git Cheatsheet"
date: 2014-02-22 05:55
comments: true
categories: 
---

berikut adalah beberapa contoh perintah git:

<ol>
<li> Show previously committed files
				{% codeblock %} 
				git diff --name-only HEAD^1
				{% endcodeblock %}
</li>

<li> Show short formatted log
				{% codeblock %}
				git log --oneline
				{% endcodeblock %}
</li>
</ol>
