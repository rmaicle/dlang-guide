---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basic Types
section: Integral Types
subsection: Aliased Types
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

Integral aliased types are synonyms of basic integral types.
It is necessary to define some aliased integral types that are dependent on the computer architecture being used.
These are not reserved identifiers but are globally defined.

###### size_t

The `size_t` type is an alias to one of the unsigned integral basic types.
It represents a type that is large enough to represent an offset into all addressable memory on a given architecture.
In 32-bit machines, `size_t` is an alias to type `uint` and type `ulong` on 64-bit machines.

###### ptrdiff_t

The `ptrdiff_t` type is an alias to one of the signed integral basic types.
It is defined to be the same size as `size_t` on a given architecture.
In 32-bit machines, `ptrdiff_t` is an alias to type `int` and type `long` on 64-bit machines.

| Alias     | 32-bit system | 64-bit system |
|-----------|:-------------:|:-------------:|
| size_t    | uint          | ulong         |
| ptrdiff_t | int           | long          |
