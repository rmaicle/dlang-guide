---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Preliminaries
section: Program Entry Point
excerpt: 
group: DLang
tags: [dlang, dguide, draft]
---

The entry point of a D program is the `main()` function.
It has the following variations:

| Syntax              | Description |
|---------------------|-------------|
| void main( )         | Return nothing (void) and accepting no parameters. |
| void main( string[ ] ) | Return nothing (void) and accepting zero or more string (string [ ]) parameters |
| int main( )          | Returning an integer and accepting no parameters |
| int main( string[ ] )  | Returning an integer and accepting zero or more string (string [ ]) parameters |

Function `main()` always returns a value even if the function variant used returns nothing as described above.

When the function used is defined to return nothing then the compiler injects code that automatically handles the return values.
If the program terminates without an error, it returns zero (0).
Otherwise it returns one (1).
If the programmer tries to return a value from inside the `main()` function that is defined to return nothing then an error occurs.

When the `main()` function used is defined to return an integer then it is the responsibility of the programmer to specify the actual values to be returned to the program's environment.
If the programmer did not or forgot to return a value then an error occurs.

For the most part, only the simplest form of the program entry point will be used.

{% highlight d linenos %}
{% include_relative entry_point.d %}
{% endhighlight %}

###### Compilation

Here is the most basic syntax to compile a D source file using the reference compiler:

    dmd <source> [source...]

Here is an example how to use it assuming that the program code above is in a file named `hello.d`.

{% highlight sh linenos %}
$ dmd hello.d                   # compile
$ ./hello                       # execute it
Hello world!                    # program output
{% endhighlight %}

