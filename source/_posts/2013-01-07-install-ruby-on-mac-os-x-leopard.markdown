---
layout: post
title: "install ruby on Mac OS X Leopard"
date: 2013-01-07 13:46
comments: true
categories: ["Ruby", "Rails"]
---

1. install brew
	- [install brew](http://mxcl.github.com/homebrew/)
	- install git using brew
```
brew install git
```
2. install rvm
	- [install rvm and ruby](https://rvm.io/)
3. install ruby and manage gemset using rvm
	- install ruby using rvm
```
rvm install ruby 1.9.3
```
	- getting list of supported rubies
```
rvm list known
```
	- use installed rubies
```
rvm use ruby1.9.3
```
	- create gemset
```
rvm gemset create gemset-name
```
	- use gemset
```
rvm gemset use gemset-name
```
	- shorthand
```
rvm use ruby@gemset
```
