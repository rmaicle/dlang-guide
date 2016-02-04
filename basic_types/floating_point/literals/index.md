---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basic Types
section: Floating Point Types
subsection: Literals
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

Floating point literals are a series of consecutive characters that the compiler interprets as a floating point type.
Floating point literals can be in decimal or hexadecimal formats.
Floating point literals can have suffixes which tell the compiler what category of floating point group it belongs to.
Floating point literals uses the same digit separators as integer literals.

> It is an error if the literal exceeds the range of the type. It is not an error if the literal is rounded to fit into the significant digits of the type.

> Complex literals are not tokens, but are assembled from real and imaginary expressions during semantic analysis:
>
>     4.5 + 6.2i      // complex number (phased out)

##### Sections
{% include reference_dlang_subsubsection_links.html %}
