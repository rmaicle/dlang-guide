---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Lexical
excerpt: D Programming Language
group: DLang
tags: [dlang, dlangref, draft]
---

{% comment %}
Lexical scanning is the compilation phase that ...
What input?
What output?
{% endcomment %}

## Source Text

Input source files are text files passed to and read by the compiler.
D supports the [ASCII] and [Unicode] text file formats and understands any Unicode character.

An ASCII text file is read starting with the first character in the file but not so with an Unicode text files.
Because Unicode text files deal with different _character encodings_ [^charencode] and different machine endianness [^endianness], Unicode files must have an identification system.
That identification system is embedded in the text file and defined by Unicode as the _Byte Order Mark_ (BOM).
The BOM describes how the contents of the file is encoded.
The compiler reads the _BOM_ of the file and determines how to convert the rest of the characters in the file to Unicode characters and split them into tokens.

| Format   | BOM |
|----------|-----|
| ASCII    | none (first character must be <= U+0000007F) |
| UTF-8    | EF BB BF |
| UTF-16BE | FE FF |
| UTF-16LE | FF FE |
| UTF-32BE | 00 00 FE FF |
| UTF-32LE | FF FE 00 00 |

###### ASCII

ASCII or American Standard Code for Information Interchange is a character-encoding scheme which was developed from telegraphic codes promoted by Bell data services.
The first edition of the ASCII standard was published in 1963 and revisions went on until 1986.[^ascii_pub]
The ASCII character set was later incorporated into the Unicode character set without changing their codes to allow backwards compatibility. [^ascii_unicode]



[ASCII]: (https://en.wikipedia.org/wiki/ASCII)
[Unicode]: (https://en.wikipedia.org/wiki/Unicode)

[^charencode]: Character encodings are a way to unify different character sets of the world's writing systems to facilitate the interchange of digital text.
[^endianness]: Machine endianness refers to the way a computer processor stores data. Technically, it is the way a computer processor stores the most significant _bits_. If the most significant bits are stored first then this is called the _Big-Endian_ (BE) and the other way would be _Little-Endian_ (LE). For more information go to [https://en.wikipedia.org/wiki/Endianness](https://en.wikipedia.org/wiki/Endianness).

[^ascii_pub]: [Wikipedia: ASCII, Publication](https://en.wikipedia.org/wiki/ASCII#Publication)
[^ascii_unicode]: [Wikipedia: ASCII, Unicode](https://en.wikipedia.org/wiki/ASCII#Unicode)

###### Unicode

[_Unicode_](http://unicode.org/) is an industry standard for text encoding for the world's writing system.
The most recent version is [Unicode 8.0](http://blog.unicode.org/2015/06/announcing-unicode-standard-version-80.html) as of November 2015.
Unicode defines two mapping methods: the _Unicode Transformation Format_ (UTF) encodings, and the _Universal Character Set_ (UCS) encodings.
There are other UTF encodings other than those mentioned here.

## Token Separators

| Name              | Unicode         | ASCII           | Char | Remark |
|-------------------|:---------------:|:---------------:|:----:|--------|
| End of File (EOF) | U+0000          | 00 0x00         | \\0     | Null (NUL) |
|                   | U+001A          | 26 0x1A         |         | Substitute (SUB) |
| End of Line (EOL) | U+000A          | 10 0x0A         |  \\n    | Line Feed (LF) |
|                   | U+000D          | 13 0x0D         |  \\r    | Carriae Return (CR) |
|                   | U+000D + U+000A | 13+10 0x0D+0x0A | \\r\\n  | CR+LF |
|                   | U+2028          |                 |         | Line Separator |
|                   | U+2029          |                 |         | Paragraph Separator |
|                   |                 |                 |         | End of File (EOF) |
| Whitespace        | U+0009          | 09 0x09         |  \\t    | Horiontal tab (TAB) |
|                   | U+000B          | 11 0x0B         |  \\v    | Vertcal tab (VT) |
|                   | U+000C          | 12 0x0C         |  \\f    | New Page Form Feed (NP, FF) |
|                   | U+0020          | 32 0x20         | (space) | Space |

###### Backslash Line Splicing

Backslash line splicing is used in programming languages like C++ to join two lines when the line is getting horizontally long.
Line splicing was used as an aid to 'wrap' long source code lines and still be treated by the compiler as if it was a single line.
D does not recognize backslash line splicing but the language does not limit the number of characters of a source code line.


{% comment %}
https://latedev.wordpress.com/2012/12/04/all-about-eof/
{% endcomment %}

##### Sections

{% include reference_dlang_section_links.html %}
