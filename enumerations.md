---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Enumerations
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

Base Types
> The base type of an enum is the type it is based on:
> enum E : T { ... } // T is the base type of E

> If a enum has as a base type one of the types in the left column, it is converted to the type in the right column. (&#167;6)

##### Implicit Conversions

Implicit conversions are used to automatically convert types as required.
A enum can be implicitly converted to its base type, but going the other way requires an explicit conversion.
For example:

~~~
int i;
enum Foo { E }
Foo f;
i = f;          // OK
f = i;          // error

f = cast(Foo)i; // OK
f = 0;          // error
f = Foo.E;      // OK
~~~

If one or both of the operand types is an enum after undergoing the above conversions, the
result type is:

1. If the operands are the same type, the result will be the that type.
2. If one operand is an enum and the other is the base type of that enum, the result is the base type.
3. If the two operands are different enums, the result is the closest base type common to both.
   A base type being closer means there is a shorter sequence of conversions to base type to get there from the original type.