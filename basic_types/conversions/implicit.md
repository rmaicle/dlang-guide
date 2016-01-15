---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basic Types
section: Conversions
subsection: Implicit Conversions
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

Implicit conversions are used to automatically convert types as required.
It follows the widening conversion or promotion rule.
Which also means that integral and floating point types are implicitly convertible to a floating point type.

The following lists the type conversions considered as errors regarding implicit conversions:

1. Integral value to a narrower type.
2. Floating point values to an integral type.
3. Float, double or real type to an imaginary floating point type.
4. Float, double or real type to a complex floating point type.
5. Imaginary floating point type to a float, double or real types.
6. Complex floating point type to a non-complex floating point type.

{% highlight d %}
byte x = cast(int)1;        // allowed, literal 1 fits in a byte
byte y = cast(int)1000;     // error, literal 1000 does not fit in a byte

int i = 0;
byte b = i;                 // (1) int to byte
byte c = 0.0;               // (2) double to byte
idouble fi = 0.0;           // (3) double to imaginary double
cdouble fc = 0.0;           // (4) double to complex float
float f = 0.0Fi;            // (5) imaginary float to float

// Add example for item 6
{% endhighlight %}

