---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basic Types
section: Integral Types
subsection: Integral Promotion
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

Integer Promotion is the conversion of a type to an integer type.
All fundamental types that are lower than an `int` type is converted to an `int`.
The character type `dchar` is converted to an unsigned integer `uint`.

| From   | Bits | To   | Bits |
|--------|-----:|------|-----:|
| bool   |   8  | int  |  32  |
| byte   |   8  | int  |  32  |
| ubyte  |   8  | int  |  32  |
| short  |  16  | int  |  32  |
| ushort |  16  | int  |  32  |
| char   |   8  | int  |  32  |
| wchar  |  16  | int  |  32  |
| dchar  |  32  | uint |  32  |
