---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basic Types
section: Conversions
subsection: Arithmetic Conversions
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

The usual arithmetic conversions convert operands of binary operators to a common type. The
operands must already be of arithmetic types. The following rules are applied in order, looking at
the base type:

1. If either operand is real, the other operand is converted to real.
2. Else if either operand is double, the other operand is converted to double.
3. Else if either operand is float, the other operand is converted to float.
4. Else the integer promotions are done on each operand, followed by:

    a If both are the same type, no more conversions are done.
    b If both are signed or both are unsigned, the smaller type is converted to the larger.
    c If the signed type is larger than the unsigned type, the unsigned type is converted to the signed type.
    d The signed type is converted to the unsigned type.
