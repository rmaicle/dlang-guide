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
EOL characters are primarily used for formatting source code and are ignored by the compiler.
The following table lists the EOL characters recognized and skipped by the compiler.

| Name                 | Char    | ASCII <br/> Decimal | ASCII <br/> Hexadecimal | Unicode         |
|----------------------|:-------:|:-------------------:|:-----------------------:|:---------------:|
| Line Feed (LF)       |  \\n    | 10                  | 0x0A                    | U+000A          |
| Carriage Return (CR) |  \\r    | 13                  | 0x0D                    | U+000D          |
| CR + LF              | \\r\\n  | 13 + 10             | 0x0D+0x0A               | U+000D + U+000A |
| Line Separator       |         |                     |                         | U+2028          |
| Paragraph Separator  |         |                     |                         | U+2029          |

Note that the EOF character is also considered as an EOL character.
