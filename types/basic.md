---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Types
section: Basic Types
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

{% comment %}
###### Microsoft

[Fundamental Types](https://msdn.microsoft.com/en-us/library/cc953fe1.aspx)

Fundamental types in C++ are divided into three categories: integral, floating point, and void.
Integral types are capable of handling whole numbers.
Floating point types are capable of specifying values that may have fractional parts.

The void type describes an empty set of values.
No variable of type void can be specified — it is used primarily to declare functions that return no values or to declare generic pointers to untyped or arbitrarily typed data.
Any expression can be explicitly converted or cast to type void.
However, such expressions are restricted to the following uses: 
{% endcomment %}

Basic types define the fundamental data types of the language.
The fundamental data types can be grouped into five (5) categories:

* [Void Type](/dlang-guide/types/basic/void.html)
* [Boolean Type](/dlang-guide/types/basic/boolean.html)
* [Integral Type](/dlang-guide/types/basic/integral.html)
* [Floating Point Type](/dlang-guide/types/basic/floating_point.html)
* [Character Type](/dlang-guide/types/basic/character.html)

The language also defines some _special types_ which are derived from or aliases of the fundamental data types.
