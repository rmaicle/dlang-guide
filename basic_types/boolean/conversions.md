---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basic Types
section: Boolean Type
subsection: Conversions
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

A boolean type can be implicitly converted to any integral type; `true` is equal to one (1) and `false` is equal to zero (0).
A numeric literal zero (0) and one (1) is implicitly converted to a boolean type; one (1) is equal to `true` and zero (0) is equal to `false`.

| From  | To    |
|:-----:|:-----:|
| true  | 1     |
| false | 0     |
| 1     | true  |
| 0     | false |

> Casting an expression to bool means testing for 0 or !=0 for arithmetic types, and null or !=null for pointers or references. (&#167;6)
