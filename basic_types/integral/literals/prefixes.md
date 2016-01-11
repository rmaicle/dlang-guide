---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basic Types
section: Integral Types
subsection: Integer Literals
subsubsection: Prefixes
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

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
