---
layout: post
title: "Enabling inverse scrolling in ubuntu"
date: 2014-02-16 09:09
comments: true
categories: 
---

berikut adalah shell script untuk me-reverse scrolling pada sebuah ```device_name```


{% codeblock natural_scrolling.sh %}
#!/bin/bash

device_name="ETPS/2 Elantech Touchpad"
id=`xinput list --id-only "$device_name"`

echo "Device ID: " $id

prop=`xinput list-props 12 | grep -m 1 -i "scrolling distance" | grep -o -e '[[:digit:]]\+'`

echo "Current Properti: " $prop

new_prop=`echo $prop | awk '{print $1, -$2, -$3'}`

echo "New Properti: " $new_prop

# apply new property setting
xinput set-prop $id $new_prop

{% endcodeblock %}
