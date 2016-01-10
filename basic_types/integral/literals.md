---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basic Types
section: Integral Types
subsection: Integer Literals
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

Integer literals are a series of consecutive characters that the compiler interprets as an integral type.
Commonly, these integer literals are written in decimal format; uses the base 10 number system.
Integer literals may also be written in _binary_ or _hexadecimal_ formats.
The language does not recognize _octal_ literals.
Octal literals are specified using the `octal!` template from the library `std.conv` which works just like an actual octal literal.

##### Integer Literal Prefixes

To tell the compiler that an integer literal is in binary or hexadecimal format, integer literal _prefixes_ are used.
Binary literals are prefixed with a zero (`0`) and the letter `B` (upper or lower case) followed by the actual binary number.
Hexadecimal literals are prefixed with a zero (`0`) and the letter `X` (upper or lower case) followed by the actual hexadecimal number.

Note that it is an error to specify an integer literal in decimal format prefixed with a zero (`0`) character.
The zero prefix was used as an octal literal prefix like `0173` which is `123` in decimal.
This is now a legacy restriction which may later be removed.

{% highlight d linenos %}
writeln(123);                       // 123
writeln(0b1111011);                 // 123
writeln(0x7B);                      // 123

writeln(0123);                      // Error: octal literals 0123 are no longer supported,
                                    //        use std.conv.octal!123 instead
writeln(std.conv.octal!(173));      // 123
{% endhighlight %}

##### Integer Literal Suffixes

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

##### Digit Separator

Integer literals can also use digit separators for formatting and readability.
The underscore character (`_`) is used as digit separator and is ignored by the compiler.
The digit separator cannot be used as the first character of decimal integer literals.
The digit separator can be used with binary and hexadecimal integer literals.

The following code demonstrates the use of the integral literals.

{% highlight d linenos %}
writeln(_123456);                   // error
writeln(123_456UL);
writeln(123_456_UL);

writeln(0b_1000_0000UL);
writeln(0b_1000_0000_UL);

writeln(0x_80UL);
writeln(0x_80_UL);
{% endhighlight %}
