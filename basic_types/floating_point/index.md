---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basic Types
section: Floating Point Types
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

Floating point types are numeric types that have a fractional part and, also like the integral types, represented with varying number of bits.
The term _floating point_ means there is no fixed number of digits before and after the decimal point; that is, the decimal point can float. [^fixed_point]

| Type     | Size (bytes) | Precision | Init         | Minimum                       | Maximum |
|----------|:------------:|:---------:|:------------:|-------------------------------|---------|
| float    |   4          |    6      |  float.nan   | -3.40282e+38                  | 3.40282e+38
| double   |   8          |   15      |  double.nan  | -1.79769e+308                 | 1.79769e+308
| real     |  16*         |   18      |  real.nan    | -1.18973e+4932                | 1.18973e+4932
| ifloat   |   4          |   32      |  ifloat.nan  | -3.40282e+38i                 | 3.40282e+38i
| idouble  |   8          |   64      |  idouble.nan | -1.79769e+308i                | 1.79769e+308i
| ireal    |  16          |           |  ireal.nan   | -1.18973e+4932i               | 1.18973e+4932i
| cfloat   |   8          |   32      |  cfloat.nan  | -3.40282e+38-3.40282e+38i     | 3.40282e+38+3.40282e+38i
| cdouble  |  16          |   64      |  cdouble.nan | -1.79769e+308-1.79769e+308i   | 1.79769e+308+1.79769e+308i
| creal    |  32          |           |  creal.nan   | -1.18973e+4932-1.18973e+4932i | 1.18973e+4932+1.18973e+4932i

The size of real is the largest floating point size implemented in hardware; 80-bits for x86 CPUs or the size of `double`, whichever is larger.

##### Sections
{% include reference_dlang_subsection_links.html %}

[^fixed_point]: Types that have a fixed number of digits before and after the decimal point is called _fixed-point_ representations.


{% comment %}
Precision is a concept that we come across in daily life but do not talk about
much. Precision is the number of digits that is used when specifying a value. For
example, when we say that the third of 100 is 33, the precision is 2 because 33 has
2 digits. When the value is specified more precisely as 33.33, then the precision is 4
digits.
The number of bits that each floating type has not only affects its maximum
value, but also its precision. The greater the number of bits, the more precise the
values are.
{% endcomment %}
