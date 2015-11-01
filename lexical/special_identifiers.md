---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Lexical
section: Special Identifiers
excerpt: 
group: DLang
tags: [dlang, dlangref, draft]
---

Special identifiers are identifiers that are automatically defined by the compiler.
These identifiers are not reserved identifiers and thus compiler implementers may redefine them for a compelling reason.
These identifiers are globally defined and readily available for programmers to use.

| Symbol      | Description |
|-------------|-------------|
| `string`    | alias to `immutable(char)[]` |
| `wstring`   | alias to `immutable(wchar)[]` |
| `dstring`   | alias to `immutable(dchar)[]` |
| &nbsp;      | |
| `size_t`    | |
| `ptrdiff_t` | |
