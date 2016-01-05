---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Types
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

Computers store and manipulate data as _bits_.
A bit is the basic unit in computing.
It has only two values or binary values: 0 and 1.
To represent something more useful information in computing, the bit is composed to form bits of data.
The smallest data of addressable memory in computing is a _byte_, a sequence of 8 bits. [^8bits]

Programming languages define different data types represented as a series of bits with differing lengths.
This led to the development of _type system_ in programming languages.
In summary, type system is a set of rules governing data and constructs to make operations on these different types are valid, correct and safe.
Type system is a broad subject under active research.
Some topics will introduce the reader on how it is applied or used in the language.

##### Sections

{% include reference_dlang_section_links.html %}

[^8bits]: A byte was originally used to represent a single character of text in a computer. Back then, there was only 8-bit computers which means it can only store and process 8 bits of data at a time. Now, 64-bit computers are everywhere. It will not be long when 128-bit computers will be the new thing.