---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Preliminaries
section: Compilers
subsection: Compiling
excerpt: 
group: DLang
tags: [dlang, dguide, draft]
---

This section discusses how to compile a D source code with the reference compiler (DMD) using the command line.
Here is the most basic syntax to on how to compile a D source code file:

<div markdown='1' class='syntax'>

###### Basic Syntax

    dmd <source [...]>
    
where `source [...]` means one or more D source files.

</div>

The following _hello world_ program is assumed to be in a D source code file named `hello.d`.

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
