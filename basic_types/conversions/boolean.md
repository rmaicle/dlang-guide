---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basic Types
section: Conversions
subsection: Boolean Conversions
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

A boolean type can be implicitly converted to an integral type; `true` is equal to one (1) and `false` is equal to zero (0).

The [integer literals] zero (0) and one (1) are implicitly converted to a boolean type; one (1) is equal to `true` and zero (0) is equal to `false`.
Any other integer literals or integral values cannot be implicitly converted to a boolean.

| From  | To    |
|:-----:|:-----:|
| true  | 1     |
| false | 0     |
| 1     | true  |
| 0     | false |

> Casting an expression to bool means testing for 0 or !=0 for arithmetic types, and null or !=null for pointers or references. (&#167;6)

[integer literals]: /dlang-guide/basic_types/integral/literals.html
