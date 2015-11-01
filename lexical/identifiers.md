---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Lexical
section: Identifiers
excerpt:
group: DLang
tags: [dlang, dlangref, draft]
---

_Identifiers_ are case sensitive and can be arbitrarily long.
_Identifiers_ can only start with an _underscore_, _ASCII alphabet_ or a _universal alphabet_ [^unialpha].
An identifier can have a _digit_ after the first character.

| Name          | Unicode         | ASCII              | Char   | Remark |
|---------------|-----------------|--------------------|:------:|--------|
| Underscore    | U+005F          | 95 0x5F            |  &#95; | Horizontal Bar |
| ASCI Alphabet | U+0041 - U+005A | 65 0x41 - 90 0x5A  |  A - Z | Capital A to Z |
|               | U+0061 - U+007A | 97 0x61 - 122 0x7A |  a - z | Small a to z |
| ASCI Digit    | U+0030 - U+0039 | 48 0x30 - 57 0x39  | 0 - 9  | Digit 0 to 9 |

Identifiers starting with two underscores (&#95;&#95;) are reserved.

[^unialpha]: Universal Character Names for Identifiers as defined in the C99 standard, ISO/IEC 9899:1999(E) Appendix D.
