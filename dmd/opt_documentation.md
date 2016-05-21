---
layout: reference_dlang
title: Guide to the D Programming Language
chapter: DMD Compiler Reference
section: Documentation Options
subsection: Generate Documentation Option
excerpt: Reference compiler Digital Mars D
group: DLang
tags: [dlang, dguide, draft]
---

###### Generate Documentation

<div markdown='1' class='syntax'>
    dmd files [...] -D
    dmd files [...] -Dd<path>
    dmd files [...] -Df<filename>

`-D`
: Generate documentation.

`-Dd<path>`
: Write documentation output to the specified path.

`-Df<filename>`
: Write documentation output to the specified filename.
  The filename must not have a path.
  To specify the path, use `-Dd<path>`.
</div>
