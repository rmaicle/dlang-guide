---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basic Types
section: Integral Types
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

Integral types are also known as integer types.
Integral types are _signed_ and _unsigned_ numeric types represented with varying number of bits.

_Signed_ types are types that can have negative and positive values.
Signed types are `byte`, `short`, `int` and `long`.
_Unsigned_ types have positive values starting from zero.
Unsigned types correspond to the signed types above with the prefix `u`; `ubyte`, `short`, `uint` and `ulong`.

| Type   | Size (bytes) | Size (bits) | Alignment (bytes) | Init | Minimum                    | Maximum                    |
|--------|:------------:|:-----------:|:-----------------:|:----:|---------------------------:|---------------------------:|
| byte   |   1          |    8        |  1                |  0   | -128                       | +127                       |
| ubyte  |   1          |    8        |  1                |  0   | 0                          | 255                        |
| short  |   2          |   16        |  2                |  0   | -32,768                    | 32,767                     |
| ushort |   2          |   16        |  2                |  0   | 0                          | 65,535                     |
| int    |   4          |   32        |  4                |  0   | -2,147,483,648             | 2,147,483,647              |
| uint   |   4          |   32        |  4                |  0   | 0                          | 4,294,967,295              |
| long   |   8          |   64        |  8                |  0L  | -9,223,372,036,854,775,808 | 9,223,372,036,854,775,807  |
| ulong  |   8          |   64        |  8                |  0UL | 0                          | 18,446,744,073,709,551,615 |
| cent   |              |             |                   |      |                            |                            |
| ucent  |              |             |                   |      |                            |                            |

Note that the integral types `cent` and `ucent` are reserved for future use.
The compiler will produce the following error in an attempt to use them:

    Error: cent and ucent types not implemented
    
##### Aliased Types

It is necessary to define some aliased integral types that are dependent on the computer architecture being used.
These are not reserved identifiers but are globally defined.

| Alias     | 32-bit Type | 64-bit Type |
|-----------|:-----------:|:-----------:|
| size_t    | uint        | ulong       |
| ptrdiff_t | int         | long        |

###### size_t

The `size_t` type is an alias to one of the unsigned integral basic types.
It represents a type that is large enough to represent an offset into all addressable memory on a given architecture.
In 32-bit machines, `size_t` is an alias to type `uint` and type `ulong` on 64-bit machines.

###### ptrdiff_t

The `ptrdiff_t` type is an alias to one of the signed integral basic types.
It is defined to be the same size as `size_t` on a given architecture.
In 32-bit machines, `ptrdiff_t` is an alias to type `int` and type `long` on 64-bit machines.

{% comment %}
| Symbol    | Description |
|-----------|-------------|
| size_t    | alias to one of the unsigned integral basic types, and represents a type that is large enough to represent an offset into all addressable memory. <ul><li><p>alias to `uint` on 32-bit machines</p><p>`alias size_t = uint`</p></li> <li><p>alias to `ulong` on 64-bit machines</p><p>`alias size_t = ulong`</p></li></ul> |
| ptrdiff_t | alias to the signed type the same size as `size_t`. <ul><li><p>alias to `int` on 32-bit machines</p><p>`alias size_t = int`</p></li> <li><p>alias to `long` on 64-bit machines</p><p>`alias size_t = long`</p></li></ul> |
{% endcomment %}

##### Sections
{% include reference_dlang_subsection_links.html %}

{% comment %}
{% gist ff36e876b11d79934ceb %}
<script src="https://gist.github.com/rmaicle/a28a0da2d18cc6ed31b5.js"></script>
{% endcomment %}
