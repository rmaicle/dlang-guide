---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basic Types
section: Boolean Type
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

The boolean type is a type that holds only _true_ and _false_ values.
A boolean type storage is equivalent to an unsigned byte (`ubyte`).

{% comment %}
| Type Name | Description | Values |
|-----------|-------------|--------|
| bool      | unsigned 8-bits | `true` or `false` |
{% endcomment %}

| Size (bytes)  | Size (bits)     | Alignment (bytes) | Init  | Minimum | Maximum |
|:-------------:|:---------------:|:-----------------:|:-----:|:-------:|:-------:|
| unsigned byte | unsigned 8-bits |  1                | false | false   | true    |

##### Sections
{% include reference_dlang_subsection_links.html %}
