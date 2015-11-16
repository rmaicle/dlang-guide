---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Preliminaries
section: Program Entry Point
excerpt: 
group: DLang
tags: [dlang, dguide, draft]
---

The entry point of a D program is `main()` function.
The main function has the following variations:

| Return Type | Function | Arguments | Syntax |
|-------------|----------|-----------|--------|
| void        | main     | none      | void main() |
| void        | main     | string[]  | void main(string[]) |
| int         | main     | none      | int main() |
| int         | main     | string[]  | int main(string[]) |

For the most part, only the simplest form of the program entry point function will be used.

{% highlight d linenos %}
{% include_relative entry_point.d %}
{% endhighlight %}

###### Compilation

Here is the most basic syntax for the reference compiler:

    dmd <source>

Here is an example how to use it assuming that the code above is saved in a filename `hello_world.d`.

{% highlight sh linenos %}
$ dmd hello_world.d             # compile
$ ./hello_world                 # run
Hello world!                    # program output
{% endhighlight %}

* _Line 1_: shows how to compile using the Digital Mars D compiler.
* _Line 2_: is how to run the executable D program.
* _Line 3_: is the actual output of the code above.
