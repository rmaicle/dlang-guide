---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Preliminaries
section: Compilation
excerpt: 
group: DLang
tags: [dlang, dguide, draft]
---

Here is the most basic syntax on how to compile a D source file using the reference compiler:

    dmd <source> [source...]

Here is an example how to use it assuming that the _hello world_ program is in a file named `hello.d`.

{% highlight sh linenos %}
$ dmd hello.d                   # compile
$ ./hello                       # execute it
Hello world!                    # program output
$ _
{% endhighlight %}
