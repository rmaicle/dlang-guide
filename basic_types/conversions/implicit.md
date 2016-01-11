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
The following applies to implicit conversion of numeric types:

1. It is an error to implicitly convert an integral value to a narrower type.
    
    ~~~{d}
    int i = 0;
    byte b = i;     // Error: cannot implicitly convert expression (i) of type int to byte
    ~~~

2. It is an error to implicitly convert floating point values to an integral type.

    ~~~{d}
    double d = 0.0;
    byte b = d;     // Error: cannot implicitly convert expression (f) of type float to byte
    ~~~

3. Integral or floating point values are implicitly convertible to any floating point value.

    ~~~{d}
    ubyte b = 255;
	double d = b;
    float f = d;
    ~~~

4. It is an error to implicitly convert a complex floating point type to a non-complex floating point type.
5. It is an error to implicitly convert an imaginary floating point type to a float, double or real types.
6. It is an error to implicitly convert a float, double or real type to an imaginary floating point type.
