---
layout: post
title: "Reverse scrolling in ubuntu"
date: 2014-02-15 19:22
comments: true
categories: 
---

Langkah-langkah untuk mengaktifkan reverse scrolling pada ubuntu:

<ol>
<li> Dapatkan id dari touchpad yang digunakan 

	{% codeblock %}	
	$ xinput list
	⎡ Virtual core pointer                    			id=2	[master pointer  (3)]
	⎜   ↳ Virtual core XTEST pointer              	id=4	[slave  pointer  (2)]
	⎜   ↳ ETPS/2 Elantech Touchpad                	id=12	[slave  pointer  (2)]
	⎣ Virtual core keyboard                   			id=3	[master keyboard (2)]
 			↳ Virtual core XTEST keyboard             	id=5	[slave  keyboard (3)]
	{% endcodeblock %}

	dari output tersebut dapat diperoleh dari touchpad yang ingin dimodif yaitu id=12
</li>

<li> Dapatkan properti yang mengatur tentang scrolling
	
	{% codeblock %}
	$ xinput list-props 12 | grep -i "scrolling distance"
		Synaptics Scrolling Distance (270):	74, 74
		Synaptics Circular Scrolling Distance (283):	0.100000
	{% endcodeblock %}

	yang mengatur arah scrolling adalah properti nomor 270.
</li>

<li> Ubah arah scrolling

	{% codeblock %}
	$ xinput set-prop 12 270 -74 -74
	{% endcodeblock %}
</li>

<li> Restart nautilus
	
	{% codeblock %}
	$ nautilus -q && nautilus -n &
	{% endcodeblock %}
</li>

<li> Enjoy
</li>
</ol>

Sumber:
[Fixing Natural Scrolling in Ubuntu](http://andym3.wordpress.com/2012/05/27/fixing-natural-scrolling-in-ubuntu-12-04/)
