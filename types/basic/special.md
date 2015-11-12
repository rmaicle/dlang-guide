---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Types
section: Basic Types
subsection: Special Types
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

 Special types are types derived from or aliases of the fundamental data types.
 See _Special Identifiers_.
 
| Symbol    | Description |
|-----------|-------------|
| string    | alias to an array of immutable (8-bit) character. <p>`alias dstring = immutable(char)[ ]`</p> |
| wstring   | alias to an array of immutable wide (16-bit) character. <p>`alias dstring = immutable(wchar)[ ]`</p> |
| dstring   | alias to an array of immutable double (32-bit) character. <p>`alias dstring = immutable(dchar)[ ]`</p> |
| &nbsp;    | |
| size_t    | alias to one of the unsigned integral basic types, and represents a type that is large enough to represent an offset into all addressable memory. <ul><li><p>alias to `uint` on 32-bit machines</p><p>`alias size_t = uint`</p></li> <li><p>alias to `ulong` on 64-bit machines</p><p>`alias size_t = ulong`</p></li></ul> |
| ptrdiff_t | alias to the signed type the same size as `size_t`. <ul><li><p>alias to `int` on 32-bit machines</p><p>`alias size_t = int`</p></li> <li><p>alias to `long` on 64-bit machines</p><p>`alias size_t = long`</p></li></ul> |

##### Properties

##### Promotion