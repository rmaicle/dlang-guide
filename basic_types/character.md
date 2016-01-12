---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Basic Types
section: Character Types
excerpt: D Programming Language
group: DLang
tags: [dlang, dguide, draft]
---

| Type Name | Description |
|-----------|-------------|
| char      | unsigned 8 bits (UTF-8 code unit ) |
| wchar     | unsigned 16 bits (UTF-16 code unit) |
| dchar     | unsigned 32 bits (UTF-32 code unit) |

##### Literals

Escape sequences begin with a backslash character (`\`).

| Escape Sequence | Description |
|:---------------:|-------------|
| \n              | Add a new line character. This is the same as calling the `writeln` function. |
| \'              | Add a single quote character. |
| \"              | Add a double quote character. This is typically used to 'quote' something inside a string. Because strings are written inside double quotes, there must be a way to place a double quote inside the string without terminating or ending the string. This scenario will be shown in an example. |
| \\\             | Add a backslash character. Because escape sequences start with a backslash character, there must be a way to add a backslash character in a string. |

##### Properties

##### Promotion
