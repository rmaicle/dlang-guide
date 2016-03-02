---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basic Types
section: Floating Point Types
subsection: Literals
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

A floating point literal is a series of consecutive characters that the compiler interprets as a floating point type.
Floating point literals apply to types `float`, `double` and `real`.
It cannot be applied to complex floating point types like `cfloat`, `cdouble` and `creal`.
A complex floating point value can be assembled from real and imaginary expressions during semantic analysis.

> It is an error if the literal exceeds the range of the type. It is not an error if the literal is rounded to fit into the significant digits of the type.

Floating point literals can have _affixes_ and can be written with _digit separators_.

| Affix       | Type   | Description |
|-------------|--------|-------------|
| `0x` / `0X` | prefix | Hexadecimal floating point literal |
| `p` / `P`   | prefix | Decimal exponent literal. Can be used with hexadecimal floating point literals only. |
| `f` / `F`   | suffix | Float type. |
| `L`         | suffix | Real type. |
| `i`         | suffix | Imaginary type. |

##### Prefix

A floating point literal can be written in decimal and hexadecimal format.

By default, floating point literals without a prefix is interpreted as a decimal floating point number.
To tell the compiler that a floating point literal is in hexadecimal format, it must be prefixed with `0x` or `0X` followed by a series of hexadecimal numbers.
A floating point exponent literal is prefixed with `p` or `P` and followed by a decimal number.
The floating point exponent literal can only be used used with a hexadecimal floating point literal.
The floating point exponent literal serves as the exponent of `2`.

A floating point literal cannot be written in binary format.

{% highlight d linenos %}
writeln(123);                   // 123
writeln(0x123);                 // 291
writeln(0x123p-5);              // 9.09375
{% endhighlight %}

##### Suffix

By default, floating point literals without a suffix is interpreted as a `double`.
An floating point literal can be written to specify that a literal is of type `float` or `real`.
To specify that a literal is of type `float`, the literal must be suffixed with `f` or `F`.
To specify that a literal is of type `real`, the literal must be suffixed with `L`.
It is an error to use the small letter to avoid misreading it for the numeric digit `1`.

To tell the compiler that a floating point literal is an _imaginary_ type, it must be suffixed with `i` (lowercase I).
It can be combined with the suffix `f`, `F` or `L`.

{% highlight d linenos %}
writeln(0x123p-5);              // double
writeln(0x123p-5f);             // float
writeln(0x123p-5L);             // real
{% endhighlight %}

Be careful when specifying a floating point literal in hexadecimal format like `0x123f` that you thought will be interpreted as a `float` because of the letter `f` at the end.
The literal is an integral type expressed in hexadecimal format.
To be sure, cast the literal; `float(0x123f)`.

##### Digit Separator

Digit separators can be embedded within floating point literals for readability.
The underscore character (`_`) is used as the digit separator.
It cannot be placed before the literal, since it will be interpreted as an _identifier_.
