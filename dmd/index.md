---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: DMD Compiler Reference
excerpt: Reference compiler Digital Mars D
group: DLang
tags: [dlang, dguide, draft]
---

The D programming language reference compiler is __Digital Mars D__ commonly known by its acronym __DMD__.
It can be downloaded from http://dlang.org/download.html.
There are also other D compiler implementations like _GDC_ and _LDC_.
Links to the other implementations can be found in the download page above.

###### Filenames
Filenames are either treated as case sensitive or not depending on the platform you are in.
_Microsoft Windows_ filenames are case insensitive. _Linux_ and _Mac OS_ filenames are case sensitive.
However, it has been good practice not to rely on filename case sensitivity when dealing with multi-platform projects.
Passing multiple filenames to the compiler requires that they be separated by a space character.

###### Options
Options cannot be 'combined'.
Each option is specified and separated by a space character.
Options are case sensitive, meaning `-d` and `-D` are treated differently.
You can specify different options in any order.
If conflicting options are encountered, the last parsed option takes precedence (ex. dmd test.d -m32 -m64 builds test.d in 64-bit architecture).
Specifying the same option multiple times, as in the case of Import Path (`-Ipath`) option, will treat the search order of the paths as they are specified.

###### Reference Compiler Command-line Syntax

The Digital Mars Compiler has the following command-line syntax:

<div markdown='1' class='syntax'>

    dmd --version | --help | -man
    dmd source[, ...] [@cmdfile] [option[...]]
    
`source[, ...]`
: One or more D sources files separated by a comma character.

  The compiler recognizes D source files as files without extension and files with the `.d` extension.

_`@cmdfile`_
: A command file is a text file where the compiler reads _commands_ from and uses those commands to compile the specified D source file(s).

_`option[...]`_
: One or more _options_ passed to the compiler to perform specific actions.
</div>

##### Sections
{% include reference_dlang_section_links.html %}
