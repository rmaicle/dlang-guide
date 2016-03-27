---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Enumerations
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

Enumerations are constants that are primarily designed to be grouped together.
The language allows the creation of enumerations that are also anonymous, which have no grouping name.
Enumerations can have an arbitrary number of members.
Enumerations that have only one member can be created as manifest constants.

##### Base Type

A _base type_ is the collective type of all members of an enumeration and an enumeration can only have one base type.
If no base type is specified, the base type is deduced from the value of first member.
If no base type is specified and the first member have no initializer then the default base type is assumed which is an `int` type.
A different base type may be explicitly specified.

##### Initialization

Members may or may not be initialized depending on its base type.

Enumerations with a numeric base type is not required to have its members explicitly initialized since they are automatically initialized by default.
The members of such an enumeration will be initialized starting with the base type `init` property which is zero (`0`).
The members of such an enumeration may be explicitly initialized with different values.
If a member is not initialized explicitly, it's value will be the next value of the previous member.

Enumerations that have a non-numeric base type must explicitly initialize each member.

It is an error to initialize members of an enumeration with different types.

A manifest constant is always default initialized if no initializer is specified.
The value of the `init` property of the type is used as the default initializer.

##### Sections
{% include reference_dlang_section_links.html %}
