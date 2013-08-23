---
layout: post
title: "Compile ActionScript 3 using MXMLC"
date: 2012-12-02 21:34
comments: true
categories: [ActionScript 3]
---

berikut adalah perintah terminal untuk meng-compile file actionscript 3
```bash
mxmlc -compiler.source-path=./src -static-link-runtime-shared-libraries=true -output bin/HelloAS3.swf src/Main.as
```

perintah ini dijalankan pada root folder dari project AS3
dimana folder source terletak pada "src"
kemudian hasil kompilasi terletak pada "bin"
