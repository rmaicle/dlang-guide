---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Structures
section: Properties
subsection: init Property
excerpt: D Programming Languages
group: DLang
tags: [dlang, dguide, draft]
---

The value of the `init` property of a structure produces the default initialized structure.
All structure members are initialized via their default initializer or via explicit initialization.

{% highlight d linenos %}
struct S {
    int a;                                  // default initialization
    int b = 7;                              // explicit initialization
}

void main() {
    writeln(S.init);                        // S(0, 7)
}
{% endhighlight %}

The output of the `writeln` function is a built-in formatted output.
The values inside the parenthesis are the values of the structure members; member variable `a` and `b`.
Zero is the value of the first structure member `a` and seven is the value of the second structure member b`.

##### TODO Nested Structs

When is `init` not usable?
