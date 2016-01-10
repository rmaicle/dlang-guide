---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Strings
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

The following string identifiers are not reserved identifiers although they are globally and automatically defined and thus readily available without importing any modules.

| Symbol    | Description |
|-----------|-------------|
| string    | alias to an array of immutable (8-bit) character. <p>`alias dstring = immutable(char)[ ]`</p> |
| wstring   | alias to an array of immutable wide (16-bit) character. <p>`alias dstring = immutable(wchar)[ ]`</p> |
| dstring   | alias to an array of immutable double (32-bit) character. <p>`alias dstring = immutable(dchar)[ ]`</p> |

