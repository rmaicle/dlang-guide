---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basic Types
section: Integral Types
subsection: Integer Literals
subsubsection: Suffixes
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

Integer literal suffixes are used to specify that an integer literal is of a certain integer type.
These suffixes are used only to specify types that are 32-bit integers or higher.
It cannot be used to specify literals for data types `byte`, `ubyte`, `short` and `ushort`.

Integer literals that are not suffixed can be any of the 32-bit (or higher) signed types.
The specific signed type is the smallest type that can hold the value.
If the value is greater than the minimum or maximum possible value of the largest type, an `integer overflow` error occurs at compiler time.

{% highlight d linenos %}
writeln(2147483647);                // int maximum
writeln(2147483648);                // long
writeln(9223372036854775807);       // long maximum
writeln(9223372036854775808);       // integer overflow
{% endhighlight %}

__Unsigned integer literals__ are suffixed with the letter `U` (upper or lower case) and can be any of the 32-bit (or higher) unsigned types.
The specific unsigned type is the smallest type that can hold the value.
If the value is greater than then maximum possible value of the largest type, an `integer overflow` error occurs at compile time.

{% highlight d linenos %}
writeln(4294967295U);               // uint maximum
writeln(4294967296U);               // ulong
writeln(18446744073709551615U);     // ulong maximum
writeln(18446744073709551616U);     // integer overflow
{% endhighlight %}

__Signed integer literals__ that are suffixed with the letter `L` (upper case only) is of type `long`.
It is an error to use the small letter `L`.

{% highlight d linenos %}
writeln(123L)                       // long
{% endhighlight %}

An unsigned 64-bit integer literal or `ulong` is suffixed with the combination of the unsigned and signed suffixes.

{% highlight d linenos %}
writeln(123UL)                      // ulong
writeln(123uL)                      // ulong
writeln(123LU)                      // ulong
writeln(123Lu)                      // ulong
{% endhighlight %}
