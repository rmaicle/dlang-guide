---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basic Types
section: Conversions
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

Base Types
The base type of an enum is the type it is based on:
enum E : T { ... } // T is the base type of E

* Implicit Conversions

Implicit conversions are used to automatically convert types as required.
A enum can be implicitly converted to its base type, but going the other way requires an explicit
conversion.
For example:
int i;
enum Foo { E }
Foo f;
i = f;          // OK
f = i;          // error

f = cast(Foo)i; // OK
f = 0;          // error
f = Foo.E;      // OK

* Arithmetic Conversions

The usual arithmetic conversions convert operands of binary operators to a common type. The
operands must already be of arithmetic types. The following rules are applied in order, looking at
the base type:
1. If either operand is real, the other operand is converted to real.
2. Else if either operand is double, the other operand is converted to double.
3. Else if either operand is float, the other operand is converted to float.
4. Else the integer promotions are done on each operand, followed by:
    a) If both are the same type, no more conversions are done.
    b) If both are signed or both are unsigned, the smaller type is converted to the larger.
    c) If the signed type is larger than the unsigned type, the unsigned type is converted to the signed type.
    d) The signed type is converted to the unsigned type.
    
If one or both of the operand types is an enum after undergoing the above conversions, the
result type is:
1. If the operands are the same type, the result will be the that type.
2. If one operand is an enum and the other is the base type of that enum, the result is the base type.
3. If the two operands are different enums, the result is the closest base type common to both.
   A base type being closer means there is a shorter sequence of conversions to base type to get there from the original type.

Integer values cannot be implicitly converted to another type that cannot represent the integer
bit pattern after integral promotion. For example:

    ubyte u1 = cast(byte)-1;        // error, -1 cannot be represented in a ubyte
    ushort u2 = cast(short)-1;      // error, -1 cannot be represented in a ushort
    uint u3 = cast(int)-1;          // ok, -1 can be represented in a uint
    ulong u4 = cast(long)-1;        // ok, -1 can be represented in a ulong

Floating point types cannot be implicitly converted to integral types.

Complex floating point types cannot be implicitly converted to non-complex floating point types.

Imaginary floating point types cannot be implicitly converted to float, double, or real types.
Float, double, or real types cannot be implicitly converted to imaginary floating point types.
