---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Lexical
section: Identifiers
excerpt:
group: DLang
tags: [dlang, dguide, draft]
---

Language _identifiers_ are case sensitive and can be arbitrarily long but may not contain whitespace characters.
Identifiers can only start with an underscore, ASCII alphabet or a universal alphabet [^unialpha].
After the first character, an identifier can have any number and combinations of the characters mentioned above including digits.

| Name           | Char   | Unicode         | ASCII      | Hexadecimal | Remark |
|----------------|:------:|-----------------|------------|-------------|--------|
| Underscore     |  &#95; | U+005F          | 95         | 0x5F        | Horizontal Bar
| ASCII Alphabet |  A - Z | U+0041 - U+005A | 65  - 90   | 0x41 - 0x5A | Capital A to Z
|                |  a - z | U+0061 - U+007A | 97  - 122  | 0x61 - 0x7A | Small a to z
| ASCII Digit    |  0 - 9 | U+0030 - U+0039 | 48  - 57   | 0x30 - 0x39 | Digits 0 to 9

The following rules are also applied to identifiers as well:

* must not begin with a digit
* must not begin with a dollar `$` sign (dollar `$` sign is a symbol for string length)
* must not begin with a period `.` (period `.` is an operator)

Identifiers starting with two consecutive underscores (&#95;&#95;) are reserved.
The compiler may not produce an error now but it is not guaranteed since the language may define the same identifier in the future and will break your code.

Examples of language identifiers:

~~~
import              # module import keyword
string              # special identifier
__FILE__            # special token
__LINE__            # special token
~~~

The following are examples of valid user-defined identifiers.
Note that line 2 (`__test__`) is not an advisable user-defined identifier since it begins with a double underscore.

~~~
test__              # ends with double underscores
__test__            # not advised
test_20151101       # starts with an alphabet
_20151101           # starts with an underscore
~~~

The following are examples of invalid identifiers:

~~~
20151101            # cannot start with a digit
7eleven             # cannot start with a digit
$sign               # cannot start and use '$' character
.file               # cannot start and use '.' character
~~~

##### Sections

{% include reference_dlang_subsection_links.html %}



[^unialpha]: Universal Character Names for Identifiers as defined in the C99 standard, ISO/IEC 9899:1999(E) Appendix D.
