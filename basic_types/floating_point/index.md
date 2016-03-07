---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basic Types
section: Floating Point Types
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

Floating point types are numeric types that have a fractional part.
The term _floating point_ means there is no fixed number of digits before and after the decimal point; that is, the decimal point is said to float. [^fixed_point]
Floating point types are also represented with varying number of bits.

The size of real is the largest floating point size implemented in hardware; 80-bits for x86 CPUs or the size of `double`, whichever is larger.

##### Sections
{% include reference_dlang_subsection_links.html %}

[^fixed_point]: Types that have a fixed number of digits before and after the decimal point is called _fixed-point_ representations.
