---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Lexical
section: Special Tokens
excerpt: Language special symbols
group: DLang
tags: [dlang, dlangref, draft]
---

Special tokens are language-defined read-only identifiers that are expanded into other tokens.
Like [_Reserved Identifiers_](reserved_identifiers.html) they cannot be redefined in any source file.
Attempt to assign values to them will result in an error.

{% comment %}
Explain/point to definition of instantiation
{% endcomment %}

| Token                               | Description |
|:-----------------------------------:|-------------|
| &#95;&#95;MODULE&#95;&#95;          | Expands to the module name at the point of instantiation. |
| &#95;&#95;FUNCTION&#95;&#95;        | Expands to the fully qualified name of the function at the point of instantiation. |
| &#95;&#95;PRETTY_FUNCTION&#95;&#95; | Similar to `__FUNCTION__`; also expands the function return type, its parameter types, and its attributes. |
| &#95;&#95;FILE&#95;&#95;            | Expands to the current source filename at the point of instantiation. |
| &#95;&#95;LINE&#95;&#95;            | Expands to the current line number at the point of instantiation. |
| &nbsp;                              | |
| &#95;&#95;DATE&#95;&#95;            | Converted to a date string literal in the format `mmm dd yyyy`. The value is the local system date of compilation. |
| &#95;&#95;TIME&#95;&#95;            | Converted to a time string literal in the format `hh:mm:ss`. The value is the local system time of compilation. |
| &#95;&#95;TIMESTAMP&#95;&#95;       | Converted to a date and time string literal in the format `www mmm dd hh:mm:ss yyyy`. The value is the local system date and time of compilation. |
| &nbsp;                              | |
| &#95;&#95;VENDOR&#95;&#95;          | Compiler vendor string literal. |
| &#95;&#95;VERSION&#95;&#95;         | Compiler version as a literal integer. |
| &nbsp;                              | |
| &#95;&#95;EOF&#95;&#95;             | Sets the scanner to the end of file. |
