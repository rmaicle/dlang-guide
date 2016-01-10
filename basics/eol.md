---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basics
section: End-of-Line Characters
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

End-of-line (EOL) characters are formatting control codes.
The following EOL characters are recognized by the compiler.

| Name              | Char    | Unicode         | ASCII           | Hexadecimal | Remark |
|-------------------|:-------:|:---------------:|:---------------:|:-----------:|--------|
| End of Line (EOL) |  \\n    | U+000A          | 10              | 0x0A        | Line Feed (LF) |
|                   |  \\r    | U+000D          | 13              | 0x0D        | Carriae Return (CR) |
|                   | \\r\\n  | U+000D + U+000A | 13 + 10         | 0x0D+0x0A   | CR+LF |
|                   |         | U+2028          |                 |             | Line Separator |
|                   |         | U+2029          |                 |             | Paragraph Separator |

Note that the EOF character is also considered as an EOL character.
