---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basic Types
section: Integral Types
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

Integral types are also known as integer types.
Integral types are _signed_ and _unsigned_ numeric types represented with varying number of bits.

_Signed_ types are types that can have negative and positive values.
Signed types are `byte`, `short`, `int` and `long`.
_Unsigned_ types have positive values starting from zero.
Unsigned types correspond to the signed types above with the prefix `u`; `ubyte`, `short`, `uint` and `ulong`.

Integral types `cent` and `ucent` are reserved for future use.
The compiler will produce an error in an attempt to use them.

##### Sections
{% include reference_dlang_subsection_links.html %}

{% comment %}
{% gist ff36e876b11d79934ceb %}
<script src="https://gist.github.com/rmaicle/a28a0da2d18cc6ed31b5.js"></script>
{% endcomment %}
