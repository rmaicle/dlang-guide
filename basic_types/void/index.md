---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basic Types
section: Void Type
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

The `void` type is described to mean that a type is _no type_.
It is somewhat akin to the decimal number zero which is a number but have no value.

Variables cannot be of type `void` although the language allows arrays of type `void`.
(See [Array](/array.html) chapter).
The `void` type is also used as function return type.
A `void` function return type tells the compiler that a function does not return a value or that it returns a `void` type.
The use of `void` in this scenario is necessary as function syntex declaration requires that a function specify the type of value it returns.

{% highlight d %}
void main() { }
{% endhighlight %}

A void type does not have a literal.

##### Sections
{% include reference_dlang_subsection_links.html %}
