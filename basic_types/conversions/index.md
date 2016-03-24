---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basic Types
section: Conversions
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

Fundamental types may be implicitly and explicitly converted to another type.
Explicit conversion can be achieved by using the `cast` expression.

###### Wide and Narrow Types
The base terms _wide_ and _narrow_ are used to refer to the size (number of bits/bytes) of a certain type compared to another.
A wider type means a type that has more bits compared to another.
A narrower type means a type that has less bits compared to another.

###### Widening Conversion
Converts a value of a certain type to another that has more bits.
It is said to be a safe conversion because there is no loss of data.
Widening conversions are also sometimes called promotion.

###### Narrowing Conversion
Converts a value of a certain type to another that has less bits.
A narrowing conversion may therefore involve loss of data if the concerned bits cannot be represented in the destination type.
It is therefore not a safe operation when doing narrowing conversions although the language allows the conversion by using _type casts_.

##### Sections
{% include reference_dlang_subsection_links.html %}