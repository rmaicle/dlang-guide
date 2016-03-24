---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Lexical
section: Source File
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

Input source files are text files passed to and read by the compiler.
D supports the [_ASCII_] and [_Unicode_] text file formats and understands any Unicode character.

ASCII
: ASCII stands for _American Standard Code for Information Interchange_.
  It is a character-encoding scheme which was developed from telegraphic codes.
  The first edition of the ASCII standard was published in 1963 and revisions went on until 1986. [^ascii_pub]
  The ASCII character set was later incorporated into the Unicode character set without changing their codes to allow backwards compatibility. [^ascii_unicode]

Unicode
: Unicode is an industry standard for text encoding for the world's writing system.
  The most recent version is [Unicode 8.0](http://blog.unicode.org/2015/06/announcing-unicode-standard-version-80.html) as of November 2015.
  Unicode defines two mapping methods: the _Unicode Transformation Format_ (UTF) encodings, and the _Universal Character Set_ (UCS) encodings.
  There are other UTF encodings other than those mentioned here.

An ASCII text file is read starting with the first character in the file but not so with Unicode text files.
Because Unicode text files have different _character encodings_ [^charencode] and deals with different machine endianness [^endianness], Unicode text files have an identification system to to determine and read the files correctly.
This identification system is embedded in the first bytes of a text file and defined by Unicode as the _Byte Order Mark_ (BOM).
The compiler reads the BOM and converts the contents of the file to Unicode characters.

| Format           | BOM | Location |
|------------------|-----|----------|
| ASCII            | none (first character must be <= U+0000007F) | none |
| UTF &ndash; 8    | EF BB BF | first 3 bytes |
| UTF &ndash; 16BE | FE FF | first 2 bytes |
| UTF &ndash; 16LE | FF FE | first 2 bytes |
| UTF &ndash; 32BE | 00 00 FE FF | first 4 bytes |
| UTF &ndash; 32LE | FF FE 00 00 | first 4 bytes |

The first source text character of an ASCII text file is the character at offset 0x00 or at the first byte of the file.
The first source text character of a Unicode text file is the character after the _Byte Order Mark_ (BOM).

##### Sections
{% include reference_dlang_subsection_links.html %}

[^charencode]: Character encodings are a way to unify different character sets of the world's writing systems to facilitate the interchange of digital text.
[^endianness]: Machine endianness refers to the way a computer processor stores data. Technically, it is the way a computer processor stores the most significant _bits_. If the most significant bits are stored first then this is called the _Big-Endian_ (BE) and the other way would be _Little-Endian_ (LE). For more information go to [https://en.wikipedia.org/wiki/Endianness](https://en.wikipedia.org/wiki/Endianness).

[_ASCII_]: https://en.wikipedia.org/wiki/ASCII
[^ascii_pub]: [Wikipedia: ASCII, Publication](https://en.wikipedia.org/wiki/ASCII#Publication)
[^ascii_unicode]: [Wikipedia: ASCII, Unicode](https://en.wikipedia.org/wiki/ASCII#Unicode)

[_Unicode_]: https://en.wikipedia.org/wiki/Unicode
