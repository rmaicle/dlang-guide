---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Type Properties
excerpt: D Programming Languages
group: DLang
tags: [dlang, dguide, draft]
---

Type Properties are read-only information about a built-in or user-defined type.
Property names are not reserved identifiers although user-defined properties may be defined.

The language defines the following syntax for using type properties:

    <source>.<property>

* __source__ - type or expression
* __property__ - one of the type properties


Type-specific properties are described in their respective sections along with more specific examples.

##### User-Defined Properties

User-defined properties can be created for user-defined types using Property Functions.
User-defined properties may not use `sizeof`, `alignof` and `mangleof` property names as members or methods of a structure, union, class or enumeration.

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
