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

<div markdown='1' class='syntax'>

###### Basic Syntax

    dmd <source [...]>
    
where `source [...]` means one or more D source files.

</div>

The following _hello world_ source code is assumed to be in a D source file named `hello.d`.

{% highlight d linenos %}
import std.stdio;

void main() {
    writeln("Hello world!");
}
{% endhighlight %}

Now, to compile the `hello.d` file and execute it:

{% highlight bash session linenos %}
$ dmd hello.d                   # compile
$ ./hello                       # execute it
Hello world!                    # program output
$ _
{% endhighlight %}
