---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: ASCII Characters
excerpt:
group: DLang
tags: [dlang, dguide, draft]
---

The _American Standard Code for Information Interchange (ASCII)_ is a character-encoding scheme which was developed from telegraphic codes promoted by Bell data services.
The first edition of the ASCII standard was published in 1963 and revisions went on until 1986.[^ascii_pub]
The ASCII character set was later incorporated into the _Unicode_ character set without changing their codes to allow backwards compatibility. [^ascii_unicode]

###### Control Codes

Control codes are control characters that are non-printable chararacters in a character set which does not represent a written symbol.
They are used to '_cause an effect_'.
ASCII control codes are carried over to the Unicode.

###### Printable Codes

TODO

##### Sections
{% include reference_dlang_section_links.html %}



[_ASCII_]: https://en.wikipedia.org/wiki/ASCII
[^ascii_pub]: [Wikipedia: ASCII, Publication](https://en.wikipedia.org/wiki/ASCII#Publication)
[^ascii_unicode]: [Wikipedia: ASCII, Unicode](https://en.wikipedia.org/wiki/ASCII#Unicode)