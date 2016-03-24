---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Type Properties
excerpt: D Programming Languages
group: DLang
tags: [dlang, dguide, draft]
---

The language have two categories of Type Properties.

* Read-only Properties that are used to query information about a type.
* Function-like Properties that perform a pre-defined operation on a type.

Properties are not reserved identifiers and user-defined properties may be defined.

The language defines the following syntax for using Type Properties:

<div markdown='1' class='syntax'>

Type Property Syntax

    <source>.<property>

`source`
: Source can be a _type_ or an _expression_.
  To evaluate source as an expression, it must be enclosed within parenthesis.

`property`
: built-in Type Properties or a user-defined type property.
  See list of all [built-in Type Properties](/dlang-guide/properties/alphabetical.html).

</div>


Type-specific properties are described in their respective sections along with more specific examples.

##### Sections
{% include reference_dlang_section_links.html %}
