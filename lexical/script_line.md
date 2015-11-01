---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: Lexical
section: Script Line
excerpt: Script execution
group: DLang
tags: [dlang, dlangref, draft]
---

The first source text character of an ASCII text file is the character at offset 0x00.
The first source text character of a Unicode text file is the character after the _file header_ or Unicode BOM.
If the first two source text characters are the `#` and `!` characters then the rest of the line is ignored.

| Name    | Unicode          | ASCII           | Char   |
|---------|------------------|-----------------|:------:|
| Shebang | U+0023 + U+0021  | 35+33 0x23+0x21 |  #!  |

The _shebang_ character sequence in Unix-like operating systems is generally used to run a command or an executable program.
In D, this can be used to run or execute a D compiler.

The _shebang_ interpreter/script directive syntax is:

    #!program [optional-arg]

The `program` must include the absolute path to an executable file.

Examples:

    #!/bin/dmd sample.d
