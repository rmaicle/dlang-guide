---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Types
section: Basic Types
subsection: Void Type
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

The `void` type is described as a type that has no type.
Variables cannot be of type void.
One of its uses is to tell the compiler that a function does not return a value or tha it returns a `void` type.

Properties

The following are properties are available for the `void` type:

* __stringof__ - string representation of the built-in type or the user-defined name of a user-defined type
* __mangleof__ - string representing the _mangled_ representation of the type

The following code demonstrates the use of the `void` type properties.

{% highlight d linenos %}
import std.stdio;

void main() {
    writeln(typeof(main).stringof);     // void()
    writeln(typeof(main).mangleof);     // FZv
}
{% endhighlight %}
