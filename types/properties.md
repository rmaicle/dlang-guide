---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Types
section: Properties
excerpt: D Programming Languages
group: DLang
tags: [dlang, dguide, draft]
---

Type properties are read-only information about a specific type.
Types have implicit properties tied to them.
The language formalizes these properties by providing syntax and keywords for their use instead of providing the same information through a library implementation.

{% comment %}
This approach has several advantages.
These properties aid programmers to maximize type safety and provide more convenience.
{% endcomment %}

The following table lists all properties that are common to all types.

| Property  | Description |
|-----------|-------------|
| init     | default initializer |
| sizeof   | size in bytes (equivalent to C's sizeof(type)) |
| alignof  | alignment size in bytes |
| mangleof | string representing the _mangled_ representation of the type |
| stringof | string representation of the type |

Thera are also some type-specific properties.
You can read them in detail in their respective sections.

##### Usage

The language defines the following syntax for using type properties:

    <type>.<property>

| Item     | Description |
|----------|-------------|
| type     | A type or an expression. [_Expressions_] are evaluated and have a resulting type. |
| property | One of the properties above. |

{% comment %}
http://dlang.org/expression.html
Expressions are used to compute values with a resulting type.
{% endcomment %}

Although, properties are functions, the language allows the exclusion of the parenthesis pair. [^property_attribute]
The exclusion of the parenthesis pair in no argument and single-argument functions are for convenience and to minimize operator pollution [^op_pollution] which aids in readability.

The built-in properties `sizeof`, `alignof`, and `mangleof` may not be declared as fields or methods in [`structs`], [`unions`], [`classes`] or [`enums`].

##### Examples

For examples, go to the specific sections: [`void`], [`boolean`], [`integral`], [`floating point`], [`characters`], [`special types`], [`structs`], [`unions`], [`classes`] or [`enums`].

[^property_attribute]: See Property Attribute.
[^op_pollution]: Consider the following code...

[_Expressions_]: /dlang-guide/expressions.html

[`void`]: /dlang-guide/types/void.html
[`boolean`]: /dlang-guide/types/boolean.html
[`integral`]: /dlang-guide/types/integral.html
[`floating point`]: /dlang-guide/types/floating_point.html
[`characters`]: /dlang-guide/types/character.html
[`special types`]: /dlang-guide/types/special.html
[`structs`]: /dlang-guide/structs_unions_classes.html
[`unions`]: /dlang-guide/structs_unions_classes.html
[`classes`]: /dlang-guide/structs_unions_classes.html
[`enums`]: /dlang-guide/enumerations.html
