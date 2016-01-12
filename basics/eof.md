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
The following table lists the EOF characters recognized by the compiler.

| Name             | Char    | ASCII <br/> Decimal | ASCII <br/> Hexadecimal | Unicode         |
|------------------|:-------:|:-------------------:|:-----------------------:|:---------------:|
| Null (NUL)       | \\0     | 00                  | 0x00                    | U+0000          |
| Substitute (SUB) |         | 26                  | 0x1A                    | U+001A          |

{% comment %}
https://latedev.wordpress.com/2012/12/04/all-about-eof/
{% endcomment %}
