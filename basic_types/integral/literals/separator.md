---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basic Types
section: Integral Types
subsection: Integer Literals
subsubsection: Digit Separator
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

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
