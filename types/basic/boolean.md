---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Types
section: Basic Types
subsection: Boolean Type
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

The boolean type is a type that holds only the values `true` or `false`.
A boolean type storage is equivalent to an unsigned byte (`ubyte`).

{% comment %}
| Type Name | Description | Values |
|-----------|-------------|--------|
| bool      | unsigned 8-bits | `true` or `false` |
{% endcomment %}

##### Conversion

A boolean type can be implicitly converted to any integral type; `true` is equal to one (1) and `false` is equal to zero (0).
A numeric literal zero (0) and one (1) is implicitly converted to a boolean type; one (1) is equal to `true` and zero (0) is equal to `false`.

| From  | To    |
|:-----:|:-----:|
| true  | 1     |
| false | 0     |
| 1     | true  |
| 0     | false |

> Casting an expression to bool means testing for 0 or !=0 for arithmetic types, and null or !=null for pointers or references. (&#167;6)

##### Operations

Allowed operations on boolean types are:

| Operator     | Description |
|:------------:|-------------|
| &            | bitwise AND |
| &#124;       | bitwise OR  |
| ^            | bitwise XOR |
| &=           | bitwise AND then assign |
| &#124;=      | bitwise OR then assign  |
| ^=           | bitwise XOR then assign |
| !            | Negation    |
| &&           | Logical AND |
| &#124;&#124; | Logical OR  |
| ? :          | Conditional operator |

