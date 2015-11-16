---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Preliminaries
section: Compilers
excerpt: Getting a D programming language compiler
group: DLang
tags: [dlang, dguide, draft]
---

The D language have 3 official compilers available.
For more in-depth information about the availability of these compilers, please visit http://wiki.dlang.org/Compilers.

###### Digital Mars D

The Digital Mars D compiler (http://dlang.org/) is the reference compiler for the D programming language.
This is the compiler created by Walter Bright from the 1990s when he called it the _Mars_ programming language.

The reference compiler is available on different platforms; Microsoft Windows, Linux and OS X.
It is officially available to some Linux distribution like Ubuntu/Debian, Fedora/CentOS, openSUSE and FreeBSD.
For other Linux distributions, please check their repositories for the availability of D language compilers.

###### GDC

GDC (http://gdcproject.org/) is a GPL implementation of the D compiler which integrates the open source D front end with GCC.
It was originally started by David Friedman in 2004 until 2007.
Development is now under Iain Buclaw.

GDC have official packages available for Arch Linux, Debian, and Ubuntu.
There are also binaries for 32/64-bit Linux for x86 and ARM, and Microsoft Windows for x86.

###### LDC

LDC (http://wiki.dlang.org/LDC) is an open source D compiler that relies on the LLVM core libraries for code generation.
LDC is still in the works.
As of November 2015, LDC project status reports that LDC works fine on most x86/x86-64 Unix-like systems, OS X 10.7+, Solaris and most BSD flavors.

Please check the site for further development.

{% comment %}
I am using version 2.069.0 of the reference compiler on 64-bit Manjaro, a Arch-based Linux distribution.
The reference compiler and GDC are available in the Manjaro repositories for download and installation.

| Compiler | Link |
|:--------:|-------------|
| <p>_Digital Mars D_ compiler is the reference compiler for the D programming language. This is the compiler created by Walter Bright from the 1990s when he called it the _Mars_ programming language.</p> <p>The reference compiler is available on different platforms; Microsoft Windows, Linux and OS X. It is officially available to some Linux distribution like Ubuntu/Debian, Fedora/CentOS, openSUSE and FreeBSD. For other Linux distributions, please check their repositories for the availability of D language compilers.</p> | <p>http://dlang.org/</p> |
| <p>_GDC_ is a GPL implementation of the D compiler which integrates the open source D front end with GCC. It was originally started by David Friedman in 2004 until 2007. Development is now under Iain Buclaw.</p> <p>GDC have official packages available for Arch Linux, Debian, and Ubuntu. There are also binaries for 32/64-bit Linux for x86 and ARM, and Microsoft Windows for x86.</p> | <p>http://gdcproject.org/</p> |
| <p>_LDC_ is an open source D compiler that relies on the LLVM core libraries for code generation. LDC is still in the works. As of November 2015, LDC project status reports that LDC works fine on most x86/x86-64 Unix-like systems, OS X 10.7+, Solaris and most BSD flavors.</p> <p>Please check the site for further development.</p> | <p>http://wiki.dlang.org/LDC.</p> |

* _Digital Mars D_ compiler (DMD) is the reference compiler for the D programming language. http://dlang.org/.
* _LDC_ is an open source LLVM-based D compiler. http://wiki.dlang.org/LDC.
* _GDC_ is a GPL implementation of the D compiler which integrates the open source D front end with GCC.
It was originally started by David Friedman in 2004 until 2007.
It is now under Iain Buclaw.
http://gdcproject.org/.
{% endcomment %}

##### DMD Linux Installation

##### DMD Windows Installation


[^DMD]: http://dlang.org/
[^LDC]: http://wiki.dlang.org/LDC
[^GDC]: http://gdcproject.org/
