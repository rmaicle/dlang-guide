---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basic Types
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

Computers store and manipulate data as _bits_.
A bit is the basic unit in computing.
It only have two values, zero and one, which is why they are called _binary_ values.
To represent something more useful information in computing, the bit is composed to form a series or consecutive bits of data.
The smallest data of addressable memory in computing is a _byte_, which is a sequence of 8 bits. [^8bits]

Programming languages define different data types represented as a series of bits with differing lengths.
This led to the development of _type system_ in programming languages.
In summary, type system is a set of rules governing data and constructs to make operations on these different types valid, correct and safe.
Type system is a broad subject under active research.
Some topics will introduce the reader on how it is applied or used in the language.

The Basic types define the fundamental data types of the language; __void__, __boolean__, __integral__, __floating point__, and __character__ types.
__Integral__ and __floating point__ types are collectively called _numeric_ or _arithmetic_ types.
The language also defines some __special types__ which are derived from or aliases of fundamental data types.

##### Wide and Narrow Types

The base terms _wide_ and _narrow_ are used to refer to the size (number of bits/bytes) of a certain type compared to another.
A wider type means a type that has more bits compared to another.
A narrower type means a type that has less bits compared to another.

##### Type Conversions

Fundamental types may be implicitly and explicitly converted to another type.
Explicit conversion can be achieved by using the `cast` expression.
This is discussed in the _Basic Types : Conversions Section_.

##### Sections
{% include reference_dlang_section_links.html %}



[^8bits]: A byte was originally used to represent a single character of text in a computer. Back then, there was only 8-bit computers which means it can only store and process 8 bits of data at a time. Now, 64-bit computers are everywhere. It will not be long when 128-bit computers will be the new thing.
