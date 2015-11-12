---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Types
section: Basic Types
subsection: Floating Point Types
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

Floating point types are numeric types that have a fractional part and, also like the integral types, represented with varying number of bits.
The term _floating point_ means there is no fixed number of digits before and after the decimal point; that is, the decimal point can float. [^fixed_point]


| Type Name | Description |
|-----------|-------------|
| float     | 32-bit floating point |
| double    | 64-bit floating point |
| real      | largest size implemented in hardware |
| ifloat    | imaginary float |
| idouble   | imaginary double |
| ireal     | imaginary real |
| cfloat    | complex number of two float values |
| cdouble   | complex double |
| creal     | complex real |

##### Literals

##### Properties

##### Promotion

[^fixed_point]: Types that have a fixed number of digits before and after the decimal point is called _fixed-point_ representations.