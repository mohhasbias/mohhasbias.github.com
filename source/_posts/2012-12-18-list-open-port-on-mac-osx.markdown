---
layout: post
title: "list open port on mac osx"
date: 2012-12-18 12:39
comments: true
categories: [Misc]
---

untuk melihat current user opened port:
``` bash
lsof -i -P | grep -i "listen"
```

untuk melihat keseluruhan system:
``` bash
sudo lsof -i -P | grep -i "listen"
```

[referensi](http://od-eon.com/blogs/calvin/list-open-ports-mac-os-x/)
