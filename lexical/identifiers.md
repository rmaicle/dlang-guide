---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Lexical
section: Identifiers
excerpt:
group: DLang
tags: [dlang, dguide, draft]
---

Language _identifiers_ are case sensitive, can be arbitrarily long but may not contain whitespace characters.
Identifiers can only start with an underscore, ASCII alphabet or a universal alphabet [^unialpha].
After the first character, an identifier can have any number or combinations of the characters mentioned above including digits.

| Name          | Unicode         | ASCII              | Char   | Remark |
|---------------|-----------------|--------------------|:------:|--------|
| Underscore    | U+005F          | 95 0x5F            |  &#95; | Horizontal Bar |
| ASCI Alphabet | U+0041 - U+005A | 65 0x41 - 90 0x5A  |  A - Z | Capital A to Z |
|               | U+0061 - U+007A | 97 0x61 - 122 0x7A |  a - z | Small a to z |
| ASCI Digit    | U+0030 - U+0039 | 48 0x30 - 57 0x39  | 0 - 9  | Digit 0 to 9 |

Identifiers starting with two underscores (&#95;&#95;) are reserved.

###### Valid Identifiers

{% highlight d linenos %}
import              // module import keyword
string              // special identifier
__FILE__            // special token
__LINE__            // special token
test_20151101       // user-defined identifier
_20151101           // user-deined identifier
{% endhighlight %}

###### Invalid Identifiers

{% highlight d linenos %}
20151101            // cannot start with a digit
7eleven             // cannot start with a digit
$sign               // cannot start and use '$' character
.file               // cannot start and use '.' character
{% endhighlight %}



[^unialpha]: Universal Character Names for Identifiers as defined in the C99 standard, ISO/IEC 9899:1999(E) Appendix D.
