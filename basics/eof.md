---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basics
section: End-of-File Characters
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

End-of-file (EOF) characters are formatting control codes.
Although it is possible, one way or another, for a file to contain characters after the EOF characters, the compiler only interprets characters until the first EOF character.
The compiler recognizes the following EOF characters.

| Name              | Char    | Unicode         | ASCII           | Hexadecimal | Remark |
|-------------------|:-------:|:---------------:|:---------------:|:-----------:|--------|
| End of File (EOF) | \\0     | U+0000          | 00              | 0x00        | Null (NUL) |
|                   |         | U+001A          | 26              | 0x1A        | Substitute (SUB) |

{% comment %}
https://latedev.wordpress.com/2012/12/04/all-about-eof/
{% endcomment %}
