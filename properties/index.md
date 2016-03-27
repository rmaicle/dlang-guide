---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Type Properties
excerpt: D Programming Languages
group: DLang
tags: [dlang, dguide, draft]
---

Every type has an associated built-in information regarding itself.
These built-in type information are exposed or made available by the language to the progammer as _type properties_.
Type properties are usually queried to return the corresponding information but there are a few that perform operations.
Type properties are not reserved identifiers and user-defined properties may be created for user-defined types as discussed in the [User-Defined Properties section](/dlang-guide/properties/user_defined.html).

The language defines the following syntax for using type properties:

<div markdown='1' class='syntax'>

Type Property Syntax

    <source>.<property>

`source`
: Source can be a _type_ or an _expression_.
  To evaluate source as an expression, it must be enclosed within parenthesis.

`property`
: built-in or user-defined type property.
  See list of all [built-in type properties](/dlang-guide/properties/alphabetical.html).

</div>

Type-specific properties are described in their respective sections along with more specific examples.

##### Sections
{% include reference_dlang_section_links.html %}
