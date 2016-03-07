---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basic Types
section: Integral Types
subsection: Literals
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

An integer literal is a series of consecutive characters that the compiler interprets as an integral type.
Integer literals are applicable only for types that are 32-bits in size or greater.
It cannot be applied to integer types that are less than 32-bits like `byte`, `ubyte`, `short` and `ushort`.

Integer literals can have _affixes_ and written with _digit separators_.

| Affix        | Type   | Description |
|--------------|--------|-------------|
| `0b` or `0B` | prefix | Binary integer literal |
| `0x` or `0X` | prefix | Hexadecimal integer literal |
| `u` or `U`   | suffix | Unsigned integer literal. Can be used with binary, decimal, hexadecimal literals and the `L` suffix. |
| `L`          | suffix | Long integer literal. Can be used with binary, decimal, hexadecimal literals and the `u` and `U` suffix. |

##### Prefix

An integer literal can be written in binary, decimal and hexadecimal format.

By default, integer literals without a prefix is interpreted as a decimal number.
Decimal integer literals cannot start with a `0` because a zero prefix was primarily used as an octal integer literal.
This is now a legacy restriction and the compiler will complain if you try to prefix a decimal integer literal with a zero.

To tell the compiler that an integer literal is in binary or hexadecimal format, integer literal _prefixes_ are used.
Binary integer literals are prefixed with `0b` or `0B` then followed by a series of binary numbers.
Hexadecimal integer literals are prefixed with `0x` or `0X` then followed by a series of hexadecimal numbers.

{% highlight d linenos %}
writeln(123);                       // 123
writeln(0b1111011);                 // 123
writeln(0x7B);                      // 123

writeln(0123);                      // Error: octal literals 0123 are no longer supported,
                                    //        use std.conv.octal!123 instead
writeln(std.conv.octal!(173));      // 123
{% endhighlight %}

##### Suffix

An integer literal can be written to specify a _signed_ or _unsigned_ integer type using a suffix.
It can also be written to specify that an integer literal is greater than 32-bits or a _long_ type.
An integer literal without a suffix is interpreted as a _signed_ type.
It can be an `integer` or `long` depending on which is the smallest type that can hold the value.
It means that if the literal value can fit in a 32-bit integer type then it will be a 32-bit integer type.
Otherwise, it will be a 64-bit size.
If the value exceeds the minimum or maximum possible value of the largest type, an `integer overflow` error occurs at compiler time.

To tell the compiler that an integer literal is an unsigned type, the literal is suffixed with `u` or `U`.
Note that the compiler will interpret the literal as either a 32-bit type or higher depending on the value of the literal.
To tell the compiler that an integer literal is a 64-bit type, the suffix `L` is used.
It is an error to use the small letter to avoid misreading it for the numeric digit `1`.
The suffixes can be combined to tell the compiler that an integer literal is an unsigned 64-bit type; `uL`, `UL`, `Lu` or `LU`.

{% highlight d linenos %}
writeln(2147483647);                // int maximum
writeln(2147483648);                // long
writeln(9223372036854775807);       // long maximum
writeln(9223372036854775808);       // integer overflow; can't fit in 64-bit signed type

writeln(4294967295U);               // uint maximum
writeln(4294967296U);               // ulong
writeln(18446744073709551615U);     // ulong maximum
writeln(18446744073709551616U);     // integer overflow; can't fit in 64-bit unsigned type

writeln(123L)                       // 64-bit signed type

writeln(123uL)                      // 64-bit unsigned type
writeln(123UL)                      // 64-bit unsigned type
writeln(123Lu)                      // 64-bit unsigned type
writeln(123LU)                      // 64-bit unsigned type
{% endhighlight %}

##### Digit Separator

Digit separators can be embedded within integer literals for readability.
The underscore character (`_`) is used as the digit separator.
It cannot be placed before the literal, since it will be interpreted as an _identifier_.

{% highlight d linenos %}
writeln(1_123L);                    // 123
writeln(1_123_L);                   // 123
writeln(0x1_123_L);                 // 4387
writeln(_1_123L);                   // Error: undefined identifier '_1_123L'
{% endhighlight %}
