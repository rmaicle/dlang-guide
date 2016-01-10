---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: DMD Compiler Reference
section: Information Options
excerpt: Reference compiler Digital Mars D
group: DLang
tags: [dlang, dguide, draft]
---


There are three command-line options to query informaton about the compiler; version, console command-line help and online command-line help.

The following is the output from the reference compiler querying for the version information under Linux 64-bit operating system.

~~~
$ dmd --version
DMD64 D Compiler v2.068
Copyright (c) 1999-2015 by Digital Mars written by Walter Bright
~~~

To see all options available on a console, execute the compiler with the _help_ argument.

~~~
dmd --help
~~~

The command-line option to display _help_ requires an internet connection.
This option links to the online command-line help for the host platform and requires opening the default browser program of your machine.

~~~
dmd -man
~~~
