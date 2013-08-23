---
layout: post
title: "Bermain Objective-C di Ubuntu"
date: 2012-12-03 11:20
comments: true
categories: ["Objective-C"]
---

Objective-C adalah bahasa pemograman yang digunakan untuk membuat aplikasi di Mac.
Alat yang biasa digunakan adalah Xcode. Sayangnya Xcode hanya tersedia di Mac.

untuk bisa bermain Objective-C layaknya di Mac, diperlukan [GNUstep](http://gnustep.org).

contoh kode dalam Objective-C adalah sebagai berikut
``` objc
#import <Foundation/Foundation.h>

int main(int argc, const char *argv[])
{
	NSAutoreleasePool *pool = [[NSAutoreleasePool alloc] init];

	NSLog(@"Programming is fun!");

	[pool drain];
	return 0;
}
```

untuk mengubah kode tersebut menjadi sebuah executable file, ada tool yang perlu dinstall, yaitu libgnustep-base-dev.

untuk menginstalnya,
``` bash
sudo apt-get install libgnustep-base-dev
```
setelah menginstall tool tersebut, untuk menghasilkan executable file dapat menggunakan perintah compile berikut
``` bash
gcc -I /usr/include/GNUstep -lgnustep-base -fconstant-string-class=NSConstantString -o hello hello.m
```
dengan asumsi bahwa kode tersebut ditulis pada file hello.m dan file executablenya diberi nama hello.

kode diatas jika telah dijadikan executable, dapat di run sehingga menghasilkan output berikut
``` bash
$ ./hello
2012-09-08 11:04:48.092 hello[2467] Programming is fun!
```
Happy coding...
