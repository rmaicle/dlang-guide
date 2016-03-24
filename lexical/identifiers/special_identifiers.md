---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Lexical
section: Identifiers
subsection: Special Identifiers
excerpt: 
group: DLang
tags: [dlang, dguide, draft]
---

Special identifiers are identifiers automatically defined by the compiler.
They are not reserved identifiers and thus compiler implementers may choose to define and use them differently.
These identifiers are globally defined and readily available for programmers to use.

| Symbol    | Description |
|-----------|-------------|
| string    | alias to an array of immutable (8-bit) character. |
| wstring   | alias to an array of immutable wide (16-bit) character. |
| dstring   | alias to an array of immutable double (32-bit) character. |
| &nbsp;    | |
| size_t    | alias to one of the unsigned integral basic types, and represents a type that is large enough to represent an offset into all addressable memory. |
| ptrdiff_t | alias to the signed type the same size as `size_t`. |

See the [__Strings__ chapter](/dlang-guide/strings.html) and [__integral Types__ section](dlang-guide/basic_types/integral.html).
