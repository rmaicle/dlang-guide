---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Type Properties
section: Alphabetical List
excerpt: D Programming Languages
group: DLang
tags: [dlang, dguide, draft]
---

The table below lists all Type Properties in alphabetical order.
The following legend is used in the Type Properties table below.

| Type   | Symbol | Description       |
|:------:|:------:|-------------------|
| enum   | n      | named enum        |
| arrays | s      | static array      |
| arrays | d      | dynamic array     |
| arrays | a      | associative array |
| struct | f      | struct field      |
| class  | f      | class field       |
| class  | i      | inner class       |

| Property          | boolean | integral | floating point | enum    | arrays    | struct  | class   |
|:------------------|:-------:|:--------:|:--------------:|:-------:|:---------:|:-------:|:-------:|
| &#95;&#95;monitor |         |          |                |         |           |         |   yes   |
| &#95;&#95;vptr    |         |          |                |         |           |         |   yes   |
| alignof           |         | yes      | yes            |         |           |   yes   |         |
| byKey()           |         |          |                |         |    (a)    |         |         |
| byValue()         |         |          |                |         |    (a)    |         |         |
| byKeyValue()      |         |          |                |         |    (a)    |         |         |
| classinfo         |         |          |                |         |           |         |   yes   |
| dig               |         |          | yes            |         |           |         |         |
| dup               |         |          |                |         |   (sda)   |         |         |
| epsilon           |         |          | yes            |         |           |         |         |
| get               |         |          |                |         |    (a)    |         |         |
| idup              |         |          |                |         |   (sda)   |         |         |
| im                |         |          | yes            |         |           |         |         |
| init              | yes     | yes      | yes            | yes     |           |         |         |
| infinity          |         |          | yes            |         |           |         |         |
| keys              |         |          |                |         |    (a)    |         |         |
| length            |         |          |                |         |   (sda)   |         |         |
| mangleof          | yes     | yes      | yes            | yes (n) |   (sda)   |   yes   |   yes   |
| mant_dig          |         |          | yes            |         |           |         |         |
| max               | yes     | yes      | yes            |     (n) |           |         |         |
| max_10_exp        |         |          | yes            |         |           |         |         |
| max_exp           |         |          | yes            |         |           |         |         |
| min               | yes     | yes      | yes            |     (n) |           |         |         |
| min_10_exp        |         |          | yes            |         |           |         |         |
| min_exp           |         |          | yes            |         |           |         |         |
| min_normal        |         |          | yes            |         |           |         |         |
| offsetof          |         |          |                |         |           |   (f)   |   (f)   |
| outer             |         |          |                |         |           |         |   (i)   |
| ptr               |         |          |                |         |   (sda)   |         |         |
| re                |         |          | yes            |         |           |         |         |
| rehash            |         |          |                |         |    (a)    |         |         |
| reverse           |         |          |                |         |   (sda)   |         |         |
| sizeof            |         | yes      | yes            |     (n) |           |   yes   |   yes   |
| sort              |         |          |                |         |   (sda)   |         |         |
| stringof          | yes     | yes      | yes            | yes (n) |   (sda)   |   yes   |   yes   |
| tupleof           |         |          |                |         |           |   yes   |   yes   |
| values            |         |          |                |         |    (a)    |         |         |

> The built-in properties `sizeof`, `alignof`, and `mangleof` may not be declared as fields or methods in `structs`, `unions`, `classes` or `enums`.
> (§ 19.Property Functions)

Type-specific properties are described in their respective sections along with more specific examples.

##### User-Defined Properties

User-defined properties can be created for user-defined types using Property Functions.



##### Sections
{% include reference_dlang_section_links.html %}



{% comment %}
=====================================================================================================


| Property          | boolean | integral | floating point | enum    | arrays    | struct  | class   |
|:-----------------:|:-------:|:--------:|:--------------:|:-------:|:---------:|:-------:|:-------:|
| mangleof          | yes     | yes      | yes            | yes (n) |   (sda)   |   yes   |   yes   |
| stringof          | yes     | yes      | yes            | yes (n) |   (sda)   |   yes   |   yes   |
| alignof           |         | yes      | yes            |         |           |   yes   |         |
| init              | yes     | yes      | yes            | yes     |           |         |         |
| sizeof            |         | yes      | yes            |     (n) |           |   yes   |         |
| min               | yes     | yes      | yes            |     (n) |           |         |         |
| max               | yes     | yes      | yes            |     (n) |           |         |         |
| infinity          |         |          | yes            |         |           |         |         |
| dig               |         |          | yes            |         |           |         |         |
| epsilon           |         |          | yes            |         |           |         |         |
| mant_dig          |         |          | yes            |         |           |         |         |
| max_10_exp        |         |          | yes            |         |           |         |         |
| max_exp           |         |          | yes            |         |           |         |         |
| min_10_exp        |         |          | yes            |         |           |         |         |
| min_exp           |         |          | yes            |         |           |         |         |
| min_normal        |         |          | yes            |         |           |         |         |
| re                |         |          | yes            |         |           |         |         |
| im                |         |          | yes            |         |           |         |         |
| length            |         |          |                |         |   (sda)   |         |         |
| ptr               |         |          |                |         |   (sda)   |         |         |
| dup               |         |          |                |         |   (sda)   |         |         |
| idup              |         |          |                |         |   (sda)   |         |         |
| reverse           |         |          |                |         |   (sda)   |         |         |
| sort              |         |          |                |         |   (sda)   |         |         |
| keys              |         |          |                |         |    (a)    |         |         |
| values            |         |          |                |         |    (a)    |         |         |
| rehash            |         |          |                |         |    (a)    |         |         |
| byKey()           |         |          |                |         |    (a)    |         |         |
| byValue()         |         |          |                |         |    (a)    |         |         |
| byKeyValue()      |         |          |                |         |    (a)    |         |         |
| get(key, default) |         |          |                |         |    (a)    |         |         |
| &#95;&#95;monitor |         |          |                |         |           |         |   yes   |
| &#95;&#95;vptr    |         |          |                |         |           |         |   yes   |
| classinfo         |         |          |                |         |           |         |   yes   |
| outer             |         |          |                |         |           |         |   (i)   |
| offsetof          |         |          |                |         |           |   (f)   |   (f)   |
| tupleof           |         |          |                |         |           |   yes   |   yes   |
{% endcomment %}
