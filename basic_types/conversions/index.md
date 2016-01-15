---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basic Types
section: Conversions
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

A _widening_ conversion converts a value of a certain type to another that has more bits.
It is said to be a safe conversion because there is no loss of data.
Widening conversions are also sometimes called promotion.

A _narrowing_ conversion converts a value of a certain type to another that has less bits.
A narrowing conversion may therefore involve loss of data if the concerned bits cannot be represented in the destination type.
It is therefore not a safe operation when doing narrowing conversions although the language allows the conversion by using _type casts_.

##### Sections
{% include reference_dlang_subsection_links.html %}