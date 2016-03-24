---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basic Types
section: Boolean Type
subsection: Properties
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

The following common [Type Properties] are defined for a boolean type:

* `alignof`     - alignment in bytes
* `mangleof`    - text representation
* `sizeof`      - size in bytes
* `stringof`    - string representation

As with other numeric types, the following Type Properties are defined for a boolean type:

* `init`        - initial value
* `max`         - largest value
* `min`         - smallest value

{% comment %}
The following table shows the boolean type property values.

| Type | sizeof | alignof | init  | min   | max  |
|------|:-------|:-------:|:-----:|:-----:|:-----|
| bool | 1      | 1       | false | false | true |
{% endcomment %}

##### Sections
{% include reference_dlang_subsubsection_links.html %}

[Type Properties]: /dlang-guide/properties/index.html