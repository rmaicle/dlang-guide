---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Type Properties
section: mangleof Property
excerpt: D Programming Languages
group: DLang
tags: [dlang, dguide, draft]
---

Name mangling is a technique used to provide type metadata that is used by the compiler for different situations.
One is to distinguish between same identifier names that are defined in different contexts.
Another is about _Application Binary Interface_ (ABI) which partly uses name mangling to allow compiled libraries to inter-operate with another library or program that is compiled with a different compiler.

{% comment %}
Does D define a standard name mangling scheme?
{% endcomment %}
 
The `mangleof` property is a compiler-defined string representation of types.
They are not defined by the language.
Using the `mangleof` property is the same as using the `stringof` property.
